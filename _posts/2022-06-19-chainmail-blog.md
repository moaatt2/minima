---
layout: post
title:  "Chainmail Blog"
categories: chainmail blog web-design
permalink: '/projects/chainmail_blog'
type: project
status: ongoing
---

### Origins and Inspiration

In [this repository](https://github.com/moaatt2/test-blog), I maintain [a chainmail blog](https://moaatt2.github.io/test-blog/)(pictured below), where every week I post about a different chainmail weave or other chainmail related topics. I first made the blog as I had heard that GitHub offered free web hosting using GitHub Pages, and I had always been interested in having a website of my own. After following the instructions in the GitHub Pages documentation, I successfully set up the website and published my first post. Unfortunately, the blog sat idle for a while because I couldn't find a steady stream of content to write about. I later learned my first chainmail weave in August of that year. Then, in December, I was first exposed to the wide variety of existing weaves. After observing the vast multitude of weaves, I realized I could feature a new weave each week, providing a steady stream of content and a path to honing my chainmail skills. 

![tech stack diagram]({{ site.baseurl }}/assets/images/projects/2022-06-19-chainmail-blog/blog_screenshot.png)

### Technical Overview

Due to this being my first website made using GitHub Pages, it is simple. The blog is a static website generated from markdown files by Jekyll running via GitHub actions, using one of the offered basic themes(Hacker). This simple design allows for easy modification and addition of content to the blog. However, because the repository only contains markdown files, it cannot be built locally. Due to this, you can only see the changes rendered as a website when they are made live. Sadly, this makes it impractical to incorporate branches into the workflow. Below is a tech stack diagram for the current state of the blog:

![tech stack diagram]({{ site.baseurl }}/assets/images/projects/2022-06-19-chainmail-blog/tech_stack_diagram.png)

### Future Plans

I plan to update the chainmail blog to support local building and viewing so that branching is feasible and I can improve my workflow. Thanks to creating this website, I have learned a great deal about using Jekyll locally. I aim to use this knowledge to set a foundation for the Chainmail blog and learn more so I can customize it further.
