---
layout: post
title:      "MTG Challenge:  Interactive Fan Site Rails Project"
date:       2019-02-06 00:42:37 +0000
permalink:  mtg_challenge_interactive_fan_site_rails_project
---


This project was beastly. From pushing to move through a large amount of rails material relatively quickly, to finally arriving at a project that needed to encapsulate over a dozen different specifications, I was highly nervous about the idea of creating a fully functional rails app from scratch. I took some time to think about the kind of project I wanted to design, when I had the idea of building a much more advanced version of my CLI gem project: something that can further propogate my band's brand and merchadising concept.

One of the biggest challenges with this project was accepting that if the conceptual design was to work AND I was were to finish all of requirements, it would be a complex rails app that would go pretty far beyond the minimum requirements of the project. I wanted a User to be able to create a profile and award themself any amount of currency called "Music Mana" that could be spent by creating Teams of musicians from different bands, discovering what songs the Team's musicians knew collectively, and virtually "perform" the song of their choice to gain XP in multiple categories. The XP would allow a user to "Level Up" from Novice, to Apprentice, Traveling Bard, Master, and finally "Ultimate Music The Gathering Master". In order to acheive this, I needed a User, Team, Character, and Song, with two join models CharacterSong and CharacterTeam, since both Team & Character, and Character & Song were many-to-many relationship. I also needed a join model called "Perform" so that a User's Team could Perform a Song. Finally in order to created a healthy and unincumbered nested route, I created a Comment model nested under Character, so that Users can comment about their favorite characters.  The model relationships can be depicted as such:
![](https://docs.google.com/drawings/d/1Zf2dCCivE7D1VWiXGl6ZyGAAdM6MiYSuqvE2fDCf5u8/edit?usp=sharing)
(alt: image of model relationships)

The most challenging hurdle was understanding my parent/child relationships. The key element in getting my comments to work successfully with my characters pages, as well as my  saving teams to the team index page, was the key line:
```
def create
    @character = Character.find_by(id: params[:character_id])
    @comment = Comment.new(comment_params)
   >>>> @comment.character = @character <<<<
    if @comment.save

def create
    if logged_in?
      @team = Team.new(team_params)
     >>>> @team.user = @current_user <<<<
      if @team.save
```

where even though the relationship belongs_to/has_many is set up in the macro, it needs to be stated that the @comment.character/ @team.user needs to be assigned to @character / @current_user, otherwise rails will still reject the assignment and it won't populate the instance variable, so you get all kinds of interestingly unhelpful error messages in your browser. Once I was able to iron this understanding out in office hours, it was  more or less smooth sailing for the rest of the project. 

The light at the end of the tunnel (though still quite far away) appeared after I successfully built out the many-to-many relationships, moving slowly and rubby-duck programming to be sure I understood what I wanted the program to do and what each line I was adding meant to me. Once I had full access to Character.songs and Song.characters, I was able to implement "the code I wish I had" fairly quickly. 

A spent a lot of time in my rails console to figure out some important instance methods I needed for the Team model, and I felt really proud of myself for being able to figure out how to write these custom methods from scratch. They are vinegary and need to be refactored, but I'm very proud of it's functionality.

I still have a problem with my OmniAuth through facebook, but I feel confident that I can debug it fairly quickly.

Overall I had a great time struggling with this project and it was greatly rewarding.
