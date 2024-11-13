# Overview

I have created this fork of the [minima](https://github.com/jekyll/minima) Jekyll theme for use in my [chainmail blog](https://moaatt2.github.io/test-blog/) and later my [personal website](https://www.dakotamckay.dev/).


# How To Use

## Custom Layouts

### Gallery

This layout creates a responsive grid of gallery cards for each post with a link to a folder containing at least 1 displayable image. 
Each gallery card contains a carousel with dots denoting the active image as well as the post release date, title(as a link) and the tags of the post.


**Special Front Matter Variables:**

* show_tutorial: Whether or not to include pictures with the text `_tutorial_` in the gallery. The default behaviour is to not do so.
* show_progress: Whether or not to include pictures with the text `_step_` in the gallery. The default behaviour is to not do so.


**Requreiments:**

* Posts need to have an `image_path` front matter variable defined to be included.