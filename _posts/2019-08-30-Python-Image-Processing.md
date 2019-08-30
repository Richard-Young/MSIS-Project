---
layout: post
title: "Python Image Processing"
categories: MSIS Project
author: "Richard Young"
meta: "UA Little Rock"
excerpt: "I experienced a steep learning curve this week as I digested Chapters 1 - 6..."
---

This was a busy week. I experienced a steep learning curve this week as I digested Chapters 1 - 6 of _Practical Python and OpenCV, 4th Edition_. Since the author himself indicates these chapters provide the foundational skill set necessary for continuing his methodology for image processing, I made it my mission to complete this segment before writing this post.

To visually demonstrate a few techniques I learned throughout the week, I will be using this image of a spider, shown below. I chose an image of a spider as a teaser for my intended title of the completed moviebarcode generator. I’m not ready to release the title yet, but keep following this blog and you will find out.

<figure>
  <img src="/MSIS-Project/assets/imgs/spider-original.jpg" alt="Friendly Spider Image">
  <figcaption>(Photo by <a href="https://unsplash.com/@ekamelev?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText" target="_blank">Егор Камелев</a> on <a href="https://unsplash.com/search/photos/spider?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText" target="_blank">Unsplash</a>)</figcaption>
</figure>


**Disclaimer** Respecting the wishes of the author, no code snippets will be posted. However, I will be sharing notable topics and reflections of what I have encountered so far.

After this week, I see images in a very granular manner. I have known that when screens display images, they do so by the correct combination of pixels being activated. However, I never would have guessed that I would be able to programatically effect these pixels at such a granular level. My eyes have been opened thanks to the powerful duo I will introduce below, NumPy and OpenCV.

## NumPy
NumPy is a numerical processing library that can be used to convert an image into a usable matrix that can then be manipulated. This NumPy matrix creates a coordinate-plane of pixels that can then be navigated and edited.

Some of the notable techniques the book demonstrates is that NumPy can be quickly used to retrieve image pixel values (such as RGB values), crop images areas of interest, and perform arithmetic functions on the images. For example, the image below has been brightened by a value of 50 using simple addition to affect every pixel value of the original image. 

<img src="/MSIS-Project/assets/imgs/spider-brightened.jpg" alt="Spider Image Brightened">

## OpenCV
OpenCV leverages NumPy and then provides a toolset of image processing functions. OpenCV is commonly used for real-time image processing, object detection, and machine learning.

I learned that OpenCV can be used to:
- Convert image file types
- Draw visual indicators and shapes
- Resize images and maintain correct aspect ratio
- Create image mask clippings
- Perform image transformations (such as translations, rotations, and scaling)
- Split and merge image color channels
- Convert images to new color spaces

I will now quickly demonstrate a couple examples of what I have practiced using OpenCV.

The image below features a green box that I drew using OpenCV. Although I did this manually using NumPy’s coordinate plane, in future chapters I will learn how to draw these boxes programmatically as a way to indicate which region of the image the computer is processing.

<img src="/MSIS-Project/assets/imgs/spider-green-box.jpg" alt="Spider Image with Green Rectangle on Face">

I was also able to use OpenCV to create a masking that separated individual RGB color values. The images below show what each RGB color value looks like without the other two channels.

<img src="/MSIS-Project/assets/imgs/spider-red.jpg" alt="Spider Image only show Red Channel">
<img src="/MSIS-Project/assets/imgs/spider-green.jpg" alt="Spider Image only show Green Channel">
<img src="/MSIS-Project/assets/imgs/spider-blue.jpg" alt="Spider Image only show Blue Channel">

The last notable takeaway I want to mention is how easy it is to use OpenCV to effect different color spaces. Although all of the examples have been geared towards the RGB color space, the author has provided content to show how easy it is to represent images in other color spaces, such as HSL and CIELAB. For example, the image below shows what the picture looks like in the CIELAB color space (a color space that attempts to represent how humans interpret color).

<img src="/MSIS-Project/assets/imgs/spider-lab.jpg" alt="Spider Image represented in CIELAB color space">

## Going Forward
I am now over halfway done with the book, and the next stage will be to begin real-time analyses of the images, starting with creating histograms using the images’ color ranges. By next week I would like to try to finish the book and begin implementing this research into my MSIS project.

## References
Rosebrock, Adrian. _Practical Python and OpenCV, 4th Edition_. 4th version, 4th ed., PyImageSearch.com, 2019, _PyImageSearch_, www.pyimagesearch.com/practical-python-opencv/.






