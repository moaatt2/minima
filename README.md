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

### RSS Feed

This layout generates an atom feed that is inteded to replace the jekyll-feed addon. All that you need to do is have a page with the `rss_feed` layout and a permalink ending in `.xml`

**Optional Post Front Matter Variables:**

* **image_path:** A relative path to the folder containing images for the post.
* **main_image:** The file name of the image in the folder referenced in `image_path` you want to represent the post. This will be treated as the thumbnail and main content image in the feed.
* **main_image_width:** A specified width to use for the `main image` in the feed.
* **main_image_height:** A specified height to use for the `main image` in the feed.


**Optional Config Variables:**

* **feed.max_posts:** You can specify a maximum number of posts that will appear in your feed, if no number is set it defaults to all posts.
* **feed.icon:** You can specify a relative link to the image you want to be used as the icon in the feed if not specified no icon will be included.
* **feed.logo:** You can specify a relative link to the image you want to be used as the logo in the feed if not specified no logo will be included.
* **feed.path:** The relative path to the feed, this is used to create a link in the `head` of each page to enable automated discovery this link will not be generated if this is left blank.
* **feed.url:** The host domain (without baseurl) of the website. This was included as I found that `site.url` doesn't work properly on github pages.
 