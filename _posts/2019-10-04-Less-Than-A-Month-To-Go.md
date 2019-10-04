---
layout: post
title: "Less than a month to go"
categories: MSIS Project
author: "Richard Young"
meta: "UA Little Rock"
excerpt: "(Deliverable Updates) One step closer to wrapping up this project..."
---

I am pleased to say that this week I have completed a good chunk of my project with the following:
- Optimized previous semester’s Python code (completing the first project deliverable)
- Finished the OpenCV [image search engine](https://www.pyimagesearch.com/2014/12/01/complete-guide-building-image-search-engine-python-opencv/){:target="_blank"} tutorial
- Created low-fidelity mockups for the second project deliverable
- Diving deeper into Django development

This week, after continuing to encounter the same problems faced last week with Recep’s code, I decided to abandon this frustrating process and go ahead and take my project code from last semester and develop it on my own as originally intentioned. 

Leveraging the knowledge I have gained from my research this semester, it was surprisingly painless for me to accomplish what I had originally intended. The Python code now takes a list of URLs for Youtube IDs, streams the video (as opposed to downloading it locally), and then generates a JSON file and a PNG file of the video’s moviebarcode. Now that I can complete this process with a list, I can start generating more barcodes for image processing.

<figure>
<img src="{{ "/assets/imgs/generator_script_screenshot.jpg" | relative_url }}" alt="Screenshot of an moviebarcode being generated">
  <figcaption>(Screenshot of the barcode generation on <a href ="https://www.youtube.com/watch?v=nDLDCyUqBFI" target ="blank">Zee Bashew's (animated) Sending spell dnd5e</a>)</figcaption>
</figure>

## Deliverable Update
Last week, I mentioned a change in my project syllabus. This is due to Dr. Agarwal’s encouragement for me to explore the utility and applications of moviebarcodes, as opposed to simply the generation process. The reason I am mentioning this now is because it will affect the end-goal of my second project deliverable (“A standalone Django app that generates moviebarcodes and can be integrated into the YoutubeTracker application”).

I am really excited for this change. Now I can prioritize using the Django application to provide video content analysis by using moviebarcodes. This update will tie in nicely with the image processing tutorials I have covered so far.

## Going forward
Next week I will prioritize development of my Django application. My goal is to make the Python code I have now compatible with my Django application in order to accomplish my second project deliverable.


