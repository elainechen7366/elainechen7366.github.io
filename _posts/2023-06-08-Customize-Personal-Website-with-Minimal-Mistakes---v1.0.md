---
layout: single
title:  "Customize Personal Website with Minimal Mistakes Jekyll Theme - v1.0"
excerpt: "What I have done at tag v1.0"
header:
  teaser: assets/images/thumbnails/mm.png
date:   2023-06-08
toc: true
toc_label: "CHANGE LOG"
toc_icon: "columns"
toc_sticky: true
categories: blog
tags: Jekyll
---
<!-- #pic: a0002-->
This site is built with one of the popular Jekyll themes - [minimal-mistakes](https://mmistakes.github.io/minimal-mistakes/). Thanks to [Michael Rose](https://github.com/mmistakes) and all the other contributors for making and incremental improving this amazing theme which is well-structured not only in code but also in the look of the site. Also, they provide clear and adequate instructions on customizing the theme according to the theme's parameters and layout, such as this [configuration page](https://mmistakes.github.io/minimal-mistakes/docs/configuration/).

In this post, I manage to write down the changes I have made to this site at the tag v1.0 of [my github repo](https://github.com/elainechen7366/elainechen7366.github.io). Some might be mentioned in minimal-mistakes' instructions while some are not. If you consider to customize your website through minimal-mistakes, hope some tips in this article might help.

**Environment**\
Theme Base: Minimal Mistakes - 18e8966\
Ruby: 3.0.6\
Jekyll: 4.3.2
{: .notice}

**Test Page**\
[Website Style Test Post]({{ site.localeis }}{% link _posts/2023-06-08-Website-Style-Test-Post.md %})
{: .notice--primary}



## Added
### 1. Use Your Own Favicon
The very first step, upload your image to [Favicon generator](https://realfavicongenerator.net/). The generator will display how the logo looks like on different platforms. Scroll to the bottom of the page, and click button `Generate your Favicons and HTML code`.

Then download Favicon package and copy the HTML code.

![](https://live.staticflickr.com/65535/52959335268_8cae173fee_k.jpg)

Follow the steps listed in the above graph, extract the package under the root folder (the same layer as `_config.yml`), and paste the HTML code in the `_includes/head/custom.html`.

![](https://live.staticflickr.com/65535/52958899286_9fbf693c24_k.jpg)

Finally, run the local server and check if the icon showed on the tab.

![](https://live.staticflickr.com/65535/52958914586_3ade90a83a_h.jpg)

### 2. Create New Skin
- Create a new scss skin file under `_sass/minimal-mistakes/skins/`
- Modify the variable `minimal_mistakes_skin` in `_config.yml`
- Use the *Test Page* to check the display while teaking the skin file.

**Note:** For your information, I fine-tune my new skin color based on `_dirt.scss`. 
{: .notice--info}

### 3. Add New Social-Link Icon
What if I want to provide a new social-share link in author side bar that the minimal-mistakes didn't provide? I'll take [Kaggle](https://www.kaggle.com/) as an example here.

First, find the brand icon, I use [W3 schools](https://www.w3schools.com/icons/fontawesome5_icons_brands.asp). Then add icon setting into `_utilities.scss` and `_config.yml` respectively.

```scss
.fa-kaggle {
    color: $kaggle-color;
  }
```

```scss
- label: "Kaggle"
  icon: "fab fa-fw fa-kaggle"
  url: "https://www.kaggle.com/elainechen7366"
```

Last, add color setting of the brand icon into `_variables.scss`

```scss
$kaggle-color: #5bb2ff !default;
```



## Changed
### 1. Customize Typography
I have to admit that I devoted a significant amount of time on this part since I want to ensure I have a good reading experience on my site. Typography plays the most important role in this. The typography not only affects the reading experience, but also shows the style of a website. The default setting of the theme is generally suitable for most scenarios, but I hope to give a new look to my site. For example, I really love the style of [Michael's personal website](https://mademistakes.com/), creator of minimal-mistakes. So, from my perspective, the design principle of minimal-mistakes is to construct a theme that offers comprehensive functionality for websites while purposefully maintaining a neutral style. This approach provides users with abundant possibilities to craft a website according to their unique style.

Although choosing suitable fonts to my site is time-consuming, the steps to update a font are quite simple. We will use [Google Fonts API](https://developers.google.com/fonts/docs/getting_started#overview) to add fonts to our website. The script is

```html
<link href='https://fonts.googleapis.com/css?family=Font+Name' 
      rel='stylesheet' type='text/css'>
```

The first step is to choose fonts [here](https://www.w3schools.com/howto/howto_google_fonts.asp), and replace `Font+Name` in the link above with the font name you choose. For example

```html
<!-- ex: choose the font named "Abel" -->
<link href='https://fonts.googleapis.com/css?family=Abel' 
      rel='stylesheet' type='text/css'>
```

And then add the above script into `_includes/head/custom.html`.

Finally, insert the font name in the system typefaces block in `_variables.scss` presented as follows

```scss
$sans-serif: -apple-system, BlinkMacSystemFont, "Abel", "Roboto", "Segoe UI",
  "Helvetica Neue", "Lucida Grande", Arial, sans-serif !default;
```

**Note:** You can also use [Google Fonts](https://fonts.google.com/) to pick your favoriate font family. It provides font categories filter.
{: .notice--primary}
![](https://live.staticflickr.com/65535/52961167370_a50a3befb4_h.jpg")

### 2. Modify Bio Font Format
In `_sidebar.scss`, add `font-size` and `font-style` settings.
```scss
.author__bio {
  margin: 0;
  font-size: 0.9em;
  font-style: italic;

  @include breakpoint($large) {
    margin-top: 10px;
    margin-bottom: 20px;
  }
}
```
### 3. Thin Navigation Hover
If you want to make the underline thinner when hovering the navigation titles, you can try the following step:\
Find `.visible-links {}` in file `_navigation.scss`, and modify the syntax `height` in the hover label which represents the thickness of the underline while hovering on titles.



## Others
I also made some other changes like 
- Modify font size and font family on different blocks
- Modify previous/next button appearance

For the two modifications above, as they are still under deployment, I'll save explanation for the next article of this series. I know there will be a series of updates, since I am not satisfied with the appearance of the site yet. There are a lot of interesting tasks for me to explore! 