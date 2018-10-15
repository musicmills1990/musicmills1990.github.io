---
layout: post
title:      "My First CLI Gem Portfolio Project"
date:       2018-10-15 14:39:26 -0400
permalink:  my_first_cli_gem_portfolio_project
---


The process of understanding this project was a huge hurdle in this course (I'm submitting for review so I'm not completely done yet). There is so much that you don't experience in full until you reach this first final project: setting up a file structure on your own, continually using github and actually seeing why a repo is so important, messing around with gemspec files, understanding development dependecies and other "ignore it for now" aspects of how the guts of a program works, and no rspec tests to help push you in a specific direction. 

I spent a ton of time watching the video lectures and trying to code-along to understand how to make something happen. For the longest time I couldn't use my console because there was something I had missed sitting in my gemspec file that kept me from using Nokogiri within my program (until I eventually found it from watching another video about file structure, understanding 'require' and 'require-relative' more fully, and bundler). Overall I found it difficult to be stuck on a problem logistically and having to take more time to watch more videos or filter through overstack while recognizing that the bigger problem lay ahead:  I still wasn't understanding the relationship between information being scraped and how it could become information within an object. 

Sometimes for something to really solidify in your brain, you need to do things the long way. I started to see why having objects is useful when I had all these local variables saved in replit to try and keep track of the information I was scraping and organize it so my CLI interface could use it eventually. It finally made sense when I said to myself, "I need 5 of this thing. Each of those 5 things need to have info A, info B, and info C." And I realized **that's an object instance and it's attributes**. It might sound simple to others, but being told how that works and really understanding why you need it was pivotal for me in this project. 

Finally, using the memoization tool ||= to only scrape the site *once*  and then save the HTML as a class instance variable, like this: 

def self.doc
@doc ||= Nokogiri::HTML(open"https://musicthegathering.com"))
end

allowed me to call self.doc in my scrape methods while only asking the server for one HTTP request (I was getting a lot of "HTTP error 429: Too-many-requests" error because my scrapers were scraping every time I called @doc, and I guess the server I was working with didn't like it).

Overall I am proud of my project but I would love it to be fancier than it is. Part of knocking down milestones is being proud of what you accomplished while seeing what you will be able to do with more experience, time and knowledge. 


