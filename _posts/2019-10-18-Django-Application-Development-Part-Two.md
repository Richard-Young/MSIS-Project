---
layout: post
title: "Django Application Development - Part 2"
categories: MSIS Project
author: "Richard Young"
meta: "UA Little Rock"
excerpt: "Lots of moving pieces..."
---
It has been a fast, productive week resulting in the following developments: 
+ Django index template high-fidelity mockup
+ Django functionality for
  - searching the Youtube Data API 
  - storing and displaying Youtube Data
  - storing JSON and PNG files from dynamic barcode generation (In progress) 

## Mockup Design
Creating these mockups was a fun challenge because this was my first time designing a darktheme mockup. Having a darktheme will make this project’s design more consistent with our COSMOS application [YoutubeTracker](http://cosmos.ualr.edu/tools/youtubetracker/){:target="_blank"}.

<figure>
<img src="{{ "/assets/imgs/mockup_screenshot.jpg" | relative_url }}" alt="Screenshot of mockup design process using Affinity Designer">
  <figcaption>(Screenshot of mockup design process using Affinity Designer)</figcaption>
</figure>

Using a darktheme will also provide balance for the barcodes themselves as they tend to contain a wide variation of color that may clash with the application’s interface. If you are interested in how to begin designing a dark theme, I highly recommend starting with the [Google Material Design documentation](https://material.io/design/color/dark-theme.html){:target="_blank"}.

## Django Development
After this week, I am feeling much more confident in my existing knowledge or Django application development. I am currently able to use Django to search Youtube, store data, and dynamically display this information back to the user. 

In the screenshot below, I am using Django forms and the [Youtube Data API](https://developers.google.com/youtube/v3){:target="_blank"} to return public Youtube data based on a search query. I searched “animated spellbook,” which returned the first nine Yoube video that meets this search result. I intend to use this feature to allow users to quickly search for videos that exist publically on Youtube, verify it is indeed the video they want, and then generate a moviebarcode of this video.

<figure>
<img src="{{ "/assets/imgs/form_search_screenshot.jpg" | relative_url }}" alt="searching the Youtube Data API">
  <figcaption>(Screenshot of Django functionality for searching the Youtube Data API)</figcaption>
</figure>

In this second screenshot below I demonstrate that if I have a Youtube ID,I can process that ID using the [pafy Python library](https://pythonhosted.org/pafy/){:target="_blank"} and then display this data back to the user. Using a Youtube ID, pafy can return data associated with a video to the user. For example, below I have used three Youtube IDs and asked pafy to return titles of these videos, which are displayed under their respective IDs. Using pafy with Django, Youtube data can be captured by the pafy python library and then stored into a Django database. Once the data is stored into my local Django database, it is then dynamically displayed in the list items and sorted by title name, as shown below. 

<figure>
<img src="{{ "/assets/imgs/form_generation_screenshot.jpg" | relative_url }}" alt="storing and displaying Youtube Data">
  <figcaption>(Screenshot of Django functionality for storing and displaying Youtube Data)</figcaption>
</figure>

## Going forward
Next week, I will continue working on the Django Application, and I aim to have Django dynamically generate, store, and query moviebarcodes. If time allows, I will begin integrating more of the histogram analysis methods previously researched.


