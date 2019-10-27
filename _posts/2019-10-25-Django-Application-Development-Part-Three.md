---
layout: post
title: "Django Application Development - Part 3"
categories: MSIS Project
author: "Richard Young"
meta: "UA Little Rock"
excerpt: "Lots to do, so little time..."
---

I started this week optimistically, feeling I had plenty of time to finish development of my moviebarcode application. However, I have experienced difficulties when storing the dynamically generated JSON and PNG files into the Django model. The problem stems from a combination of Django’s reluctance to store local files and issues with where in the application Django processes the code to generate the files.

I have been utilizing Vitor Freita’s Youtube playlist, [Django 2.1 File Upload Tutorial](https://www.youtube.com/watch?v=Zx09vcYq1oc&list=PLLxk3TkuAYnpm24Ma1XenNeq1oxxRcYFT){:target="_blank"}, which is a great introduction to storing inputed files to a Django form field and then transferring those files into a Django model field. However, since I am generating the files and not inputting them into a form field, the model is returning incorrect paths. I have tried many troubleshooting methods to combat this problem, but so far I haven’t had any success. 

I am realizing that Django’s initial database is a bit more primitive than what I need, since the data I need to store is more complicated in nature. However, I have some ideas for this coming week to work around this problem.

## Going Forward
Next week, I will be submitting my final blog post for my MSIS project documentation. My project committee will then officially begin evaluating my progress throughout the course of this semester. Hopefully by next week I will have solved the problems discussed above and will be able to deliver a rough prototype.

## Post Update (October 27, 2019)
It's the weekend, and I wanted to provide an update that I have solved the problems discussed above. I can now successfully provide a Youtube Id to a Django form, Django will generate both a PNG and JSON file, and this generated data is stored correctly to my local Django database.

<figure>
<img src="{{ "/assets/imgs/barcode_generation_screenshot.gif" | relative_url }}" alt="Screenshot of generating moviebarcode data then and retrieving it with Django">
  <figcaption>(Screenshot of generating moviebarcode data then and retrieving it with Django)</figcaption>
</figure>

