---
layout: post
title: "Histogram Analysis"
categories: MSIS Project
author: "Richard Young"
meta: "UA Little Rock"
excerpt: "This week I compared generated histograms for similarities..."
---

Once again, using PyImageSearch articles as my guide, this week I worked on the following:
- I generated histograms from the moviebarcodes I created last semester
- I compared these generated histograms for [similarities](https://www.pyimagesearch.com/2014/07/14/3-ways-compare-histograms-using-opencv-python/){:target="_blank"} 
- I began development on an [image search engine](https://www.pyimagesearch.com/2014/12/01/complete-guide-building-image-search-engine-python-opencv/){:target="_blank"} that returns similar moviebarcodes

## Comparing Histograms
I am using histograms for this project simply as a comparison method for moviebarcodes. The histograms act as a kind of “middleman” for the comparison process, meaning I can determine the similarity of a list of moviebarcodes by determining the similarity of their histograms. Histograms are a great comparison tool for what I am working on because they compare color so well. Thankfully the moviebarcode technique I am using is purely based on color, with no texture or objects, so the moviebarcodes have been fairly straightforward to analyze.

This week I compared the moviebarcodes I generated last semester. I used four moviebarcodes of music videos from one of my favorite music artists to see if I could detect similarities between them. I also used a moviebarcode from a Jurassic Park trailer as somewhat of a “control” to see how it compared to the four moviebarcodes from the music artist. This is a rough comparison since my test group of movie barcodes is so small, but now I have several histogram comparison techniques that I can use for further optimization. Once I test these techniques and determine the best one to use for my project, I will be able to apply this method to a large list of movie barcodes.

For instance, the image below is the output of when the [OpenCV correlation comparison](https://docs.opencv.org/2.4/doc/tutorials/imgproc/histograms/histogram_comparison/histogram_comparison.html){:target="_blank"} is applied to the moviebarcodes:

<figure>
  <img src="{{ "/assets/imgs/results__correlation.jpg" | relative_url }}" alt="Moviebarcode Correlation Result Output">
  <figcaption>(Moviebarcode Correlation Result Output)</figcaption>
</figure>

The results above show the first moviebarcode (“Ok Go - Needing_Getting - Offical Video.png”) being used as the queried (orginal) image. This is why its value is 1.00. A value is then given to all the other images based on how correlated they are to the orginal image. A  higher value means the image is more similar to the orginal image. The results are then sorted based on how related they are to the orginal image. In this example, the  jurassic park trailer has the most difference in comparrison to the four videos from the same music artist.

## Going Forward
Next week, my wife and I will be flying out to begin our year-long adventure in Spain. With this said, there is a very slim possibility that I will have time to publish a post next week. However, I will be working toward wrapping up my first project deliverable of my MSIS project (Optimize moviebarcode generation development), which I aim to complete by September 22nd.
