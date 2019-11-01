---
layout: post
title: "Final Recap - Project Chromaweaver"
categories: MSIS Project
author: "Richard Young"
meta: "UA Little Rock"
excerpt: "Project Summary? Where to begin..."
---

I am thrilled to say that I am ending this week and my final blog post with a functional Django application that I can demo in my final project presentation, which will be next Friday (November 8, 2019). At this point, I have satisfied the agreed-upon project deliverables that I outlined in my [Project Proposal](https://richard-young.github.io/MSIS-Project/msis/project/2019/08/16/Project-Proposal-Accepted.html) post, listed below:

- Python code development for automated moviebarcode generation that can be performed on Youtube videos
- A standalone Django app that generates moviebarcodes and can be integrated into the YoutubeTracker application

This week I went full-cycle regarding the knowledge I have gained at UA Little Rock. I was able to leverage many of the skills that I have accumulated during my time as a researcher and student to produce a Django prototype application for generating moviebarcodes. I wore many hats this week as I designed high-fidelity mockups and worked with both front-end and back-end development. By no means is this application a finalized product, but since my time at UA Little Rock has exposed me to many different pockets of knowledge, I am confident I can pull from this resource pool moving forward in order to continue to improve this project.

In order to wrap up this prototype, I worked on the following big items this week:
- Designed additional high-fidelity mockups
- Pulled relevant content from test applications into a new, cleaner application
- Combined different Django pages to provide a more streamlined user experience
- Cleaned up my Django project’s code structure
- Developed HTML5 and CSS elements to fit high-fidelity mockups

Back in the following blog post, [Resource Gathering - Practical Python and OpenCV - Part 2](https://richard-young.github.io/MSIS-Project/msis/project/2019/08/30/Resource-Gathering-Practical-Python-and-OpenCV-Part-Two.html), I teased that the image of a spider used in the examples was hinting at the application’s title, but I said I wouldn’t be releasing this title until later. Since this is my final blog post, I think it’s safe to say that “later” has arrived. I am titling this project Chromaweaver. My inspiration behind this name was imagining a spider weaving together the colors of the moviebarcodes. Often, generated moviebarcodes result in images that are made up of a wide array of colored bars, or “strands”, that are aesthetically pleasing, and I think relating this image processing technique to the intricate process of a spider weaving its web is a suitable analogy.

To demonstrate Chromaweaver’s current state, I have created the following GIFs to provide animated views of my final deliverable in action:

This first GIF presents Chromaweaver’s main objective: to use Django to generate a moviebarcode from a Youtube video. As seen below, I provide a Youtube video ID to begin the generation process, and if the generation is successful, the user will be redirected to a detailed page that shows both the moviebarcode and the video it pertains to. Since this moviebarcode and its relevant information is stored in Django, when the user goes back to the homepage, the new moviebarcode is included in the list of other generated moviebarcodes.

<figure>
  <img src="{{ "/assets/imgs/chromaweaver_generating_barcode.gif" | relative_url }}" alt="Screenshot of generating moviebarcode with Chromaweaver">
  <figcaption>(Screenshot of generating moviebarcode with Chromaweaver)</figcaption>
</figure>

This second GIF demonstrates the process of exploring a list of moviebarcodes. A user is able to scroll through the moviebarcodes and select a video by clicking its title link.

<figure>
  <img src="{{ "/assets/imgs/chromaweaver_index_exploring.gif" | relative_url }}" alt="Screenshot of exploring Chromaweaver home page">
  <figcaption>(Screenshot of exploring Chromaweaver home page)</figcaption>
</figure>

In this final GIF, I show the detailed Youtube video page in its current state. At this time, the user has the ability to watch the video and either use the Youtube video controls or the moviebarcode image above to select a point of time in the video. I think this feature is an interesting user experience component because a user can quickly look at a moviebarcode and from color alone can select areas of interest. The current time of the video being played is indicated above the moviebarcode by a moving bar. In this case, however, because there are so many frames in the video shown below, the size of the bar is very small. I have an idea for how to improve the visibility of this tracker for longer videos, but for now I feel this display is sufficient for demonstrating this application’s functionality.

<figure>
  <img src="{{ "/assets/imgs/chromaweaver_detail_exploring.gif" | relative_url }}" alt="Screenshot of exploring Chromaweaver detail page">
  <figcaption>(Screenshot of exploring Chromaweaver detail page)</figcaption>
</figure>

## Going Forward
In order for Chromaweaver to be a finalized product, it will need a laundry list of improvements. This project so far is the result of my own efforts, but there is only so much I can do by myself, so I am especially looking forward to bringing in other members of [COSMOS](http://cosmos.ualr.edu/){:target="_blank"} to begin collaborations regarding Chromaweaver.

I am also excited about exploring additional applications in the field of Image Processing, including histogram analysis to return related videos based on their moviebarcodes, a subject I discussed in my previous [Histogram Analysis](https://richard-young.github.io/MSIS-Project/msis/project/2019/09/13/Histogram-Analysis.html) post.

## Resources
This project’s accomplishments would not have been possible if it were not for the dedicated content producers that take very complicated topics and break them down into bite-sized pieces, allowing me to digest them in such a short span of time. I want to extend special thanks to the publishers of the following content:

Image Processing Development:
- Adrian Rosebrock and Dave Hoffman for support and various articles mentioned at [pyimagesearch.com](https://www.pyimagesearch.com){:target="_blank"}

Django Development:
- Pretty Printed for [Django Tutorials](https://www.youtube.com/watch?v=QVX-etwgvJ8&list=PLXmMXHVSvS-DQfOsQdXkzEZyD0Vei7PKf){:target="_blank"}
- The Dumbfounds for [Django 2 Tutorial: Build A Budget Application](https://www.youtube.com/watch?v=en4fg1F1gRs&list=PLbpAWbHbi5rNUuLTzreCl1g212G7qgzpR){:target="_blank"}
- Vitor Freitas for [Model Forms - Django File Upload Tutorial](https://www.youtube.com/watch?v=Zx09vcYq1oc&list=PLLxk3TkuAYnpm24Ma1XenNeq1oxxRcYFT){:target="_blank"}
- Max Goodridge for [How to Save Data Input through Form Using a Django Model Form (Django Tutorial)](https://www.youtube.com/watch?v=qwE9TFNub84&t){:target="_blank"}

HTML/CSS Development:
- Danny Markov for [How to Control YouTube's Video Player with JavaScript](https://tutorialzine.com/2015/08/how-to-control-youtubes-video-player-with-javascript){:target="_blank"}
- Daniel Stern for [Styling Cross-Browser Compatible Range Inputs with CSS](https://css-tricks.com/styling-cross-browser-compatible-range-inputs-css/){:target="_blank"}
- Skillthrive for [Navbar CSS Tutorial: 3 Ways to Create a Navigation Bar with Flexbox](https://www.youtube.com/watch?v=PwWHL3RyQgk&t){:target="_blank"} 
- W3schools for [How TO - Collapse](https://www.w3schools.com/howto/howto_js_collapsible.asp){:target="_blank"}







