---
layout: post
title:      "React/Redux Portfolio Project: Bringing an Idea to Life"
date:       2019-07-23 22:12:02 +0000
permalink:  react_redux_portfolio_project_bringing_an_idea_to_life
---


This project was quite challenging but deeply rewarding. I had this tech business concept a couple months ago while talking to some fellow musicians about the troubles of breaking strings while performing, and described a concept of a monthly membership based string-replacement service. What I have loved about this program all the way through is that I can take an idea and create a prototype, which really changes an idea from a conceptual dream to the beginnings of developing a real business. When I finished the redux curriculum I was excited to build this project.

The casual nature of the project requirements page was unsettling in that it was asking us to do something we had never done before (or perhaps only in very sequestered pieces) - create a "backend Rails API" and use it to persist data to your react frontend interface. I wasn't sure where to begin with this (other than drawing out my models and their relationships) but Howard Devennish's live build video series was an excellent place to start. It helped me get some of the basic groundwork started, but way more importantly, it helped me understand the flow of information for the redux pattern. The fact that each time a new piece of information was added, you create an initial state in your store, and get ready to update the store and hold information from any forms in your program. Then to understand how the actions and action creators call reducers to declare exactly how the data is stored in redux becomes very clear. Even though the "how" and "why" were unclear and unclearer respectively at first, the fact that there are so many places to drop breakpoints and debuggers thoughout this info flow pattern makes it understandable. Once I felt I had seen enough group building/coding videos to try to add things in on my own, the excitement of being able to grab ANY piece of the redux store that I needed truly showed me how the organization of redux is so adventageous. I discovered this when I needed to user currentUser's information in a page that I hadn't originally built it for, and discovered through a quick google search that I could map multiple states to props in a component like so:
`
const mapStateToProps = (state) => {
  return {
    myGuitarForm: state.newGuitarForm,
    currentUser: state.currentUser
  }
}`

Most of all, this project taught me to read error messages coming from the front end or the back end carefully and efficiently, allowed me to majorly sharpen my debugging skills, and to slow things down and follow the flow of information calmly and mindfully when it's all becoming overwhelming, all while getting to know my own code much better and understanding each peice of it intimately. Although my project exceeds the requirements, I am excited to continue to develop more advance features to allow this potential startup concept to reach it's full potential.


