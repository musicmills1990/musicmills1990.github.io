---
layout: post
title:      "Rails + JavaScript Project: What's "this"?!"
date:       2019-05-17 13:38:46 -0400
permalink:  rails_javascript_project_whats_this
---


![](https://media.giphy.com/media/VUdLlDsKlQi5i/giphy.gif)

This project was yet another moment of the darkened map unlocking further. You learn that Rails is actually a more helpful framework for the backend, and that dynamic web applications use JavaScript for smooth UX (which I'm sure will get abstracted away with frontend frameworks...I haven't looked ahead but based on the learning patterns here at Flatiron that would be my best guess). Understanding the parts of the machine that is an AJAX call, from receiving HTML or JSON data, serializing data and the tools like activerecord serializer, reorienting your controllers to receive this new data, to wiping clean and repainting the DOM was a surprisingly large conceptual undertaking. Once the concepts became clear, and the steps of implementing an AJAX call/fetch request for data are understood and repeatable, the quantity of work was very manageable.

As I began to understand the process of the AJAX call as it pertains to my project, I found that I was frequently asking myself, "what is 'this'?", because understanding *what* data you have available becomes super important in your attempt to manipulate it. I started by using console.log before moving past a step I fully understood, then opened up my dev tools console and experimented with the in-scope data (I used debugger and devtools breakpoints later in the project as I became more accustomed to them). Besides giving me a clue as to what should come next in my code, understanding what "this", "data", or "response" were allowed me to create a mental picture of exaclty *what is happening under the hood*. Considering this is likely the predessor project for using a framework, I felt satisfied that I was painting a conceptual picture of how the parts of the machine work together to make the magic of AJAX, when for so long I felt lost in JavaScript during this unit.

This project was also a good opportunity to understand the asynchronous nature of JavaScript, as I spent a lot of time trying to understand why one clickHandler needs to be called above another. Finally, the moment when I realized that it would be **actually more convenient** to create a class Constructor for my comment data and create a prototype function for it to repaint the DOM was a big breakthrough for me, since the usefulness of constructor functions were lost on me up until that point. I had already created constructor and prototype functions for another class while following Cernan's "fetch" pattern from a study group video, which took care of the requirement. I planned on doing the comment submission form without a class constructor, so it was first time I independently recognized that it could make things easier. 

Although it felt strange to not build a new conceptual piece from the ground up for this project, I enjoyed taking an app that I was already invested creatively and added some JavaScript to improve UX and application speed.



