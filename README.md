# Overview

I have created this fork of the [minima](https://github.com/jekyll/minima) Jekyll theme for use in my [chainmail blog](https://moaatt2.github.io/test-blog/) and later my [personal website](https://www.dakotamckay.dev/).


# How To Use

## Special Post Front Matter Variables

* families: A yaml list of the weave familes a post is part of. This is primarily used by the [Family Page](#list-families) and is only applicable for posts representing specific chainmail weaves.
* image_path: The relative path to the folder containing images for the post. I suggest using this in links to images in the post to allow you move the folder easily.
* main_image: The name of the file in the folder from the `image_path` to use as the main image for the post in the [RSS Feed](#rss-feed), and as the thumbnail image in all places where posts are listed.
* main_image_width: The width of the image to use for the `main_image` for the post in the [RSS Feed](#rss-feed).
* main_image_height: The heighty of the image to use for the `main_image` for the post in the [RSS Feed](#rss-feed).
* exclude_from_gallery: Set to any value if you wish to exclude this post from the [Gallery](#gallery).


## Custom Layouts

### Gallery

This layout creates a responsive grid of gallery cards for each post with a link to a folder containing at least 1 displayable image. 
Each gallery card contains a carousel with dots denoting the active image as well as the post release date, title(as a link) and the tags of the post.

**Optional Post Front Matter Variables:**

* exclude_from_gallery: Set to any value if you wish to exclude this post from the [Gallery](#gallery).


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


### List Families

This layout creates a way to view posts by weave family for posts that include values in the optional `families` variable. The page includes a cloud of clickable tags at the front where each one will take you to the list of posts in that family. Additionally, it can also be set up to display a list of weaves in just a single family when linked to.


**Optional Post Front Matter Variables:**

* families: A yaml list of the weave familes a post is part of. This is used to identify the weave families the post should be in the lists of.

**Special Front Matter Variables:**
* glossary: This has various effects based on which of the values below the variable is set to.
    * single_only: If set to this value it will attempt to find text from a provided `glossary.json` data file for the family to display with each family, but hide this data when viewed for all families (conditional on the value of `show_single`).
    * all_only: If set to this value it will attempt to find text from a provided `glossary.json` data file for the family to display with each family, but hide this data when viewed for a single family (conditional on the value of `show_single`).
    * non-nil: If set to any value other than `nil` it will attempt to find text from a provided `glossary.json` data file for the family to display with each family.
* show_single: If set to a truthy value it will enable a script that will hide the title, tag cloud, and lists for other families when the page is linked to with an anchor to one of the families.


## Custom Includes

### 3D Model

The purpose of this include is to add a 3D model to a page with full mobile and desktop support for rotating, zooming and panning to give users a very nice interactive element.

**Include Variables:**

* **model:** The only required variable, this expects a path to the file for the mdoel you want to display (in `.glb`) format.
* **canvas_id:** An optional variable that allows you to specify an id for the canvas to be used. This will be needed if you want to have more than 1 model on a page. This should be a string that is a valid name for html element's id value.
* **ignore_canvas:** An optional variable that allows you not include a canvas in the output of the include snippet. You can use this if you want more control over where the canvas should go. Do not set this variable to include the canvas.
* **is_secondary:** An optional variable that allows you to not include the javascript imports if you already have an includes that does on the page to avoid repeated imports. This should be used for the second/subsequent uses of the includes on a page. Do not set this variable to include the imports.
