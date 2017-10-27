+++
title = "Image with Hugo figure shortcode parameters set using ATTR_HTML"
tags = ["image"]
draft = false
+++

[Issue # 17](https://github.com/kaushalmodi/ox-hugo/issues/17)


## Setting `class` parameter {#setting-class-parameter}

{{<figure src="/images/org-mode-unicorn-logo.png" class="inset">}}

[Discussion](https://github.com/kaushalmodi/ox-hugo/issues/17#issuecomment-313627728)


## Setting `alt` parameter {#setting-alt-parameter}

[Reference](https://www.reddit.com/r/emacs/comments/71wy6n/orgmode_as_a_markup_language_does_make_sense_even/dnhqudn/)

{{<figure src="/images/org-mode-unicorn-logo.png" alt="Org-mode Unicorn Logo">}}


## Setting `title` parameter {#setting-title-parameter}

{{<figure src="/images/org-mode-unicorn-logo.png" title="Logo">}}


## Setting image caption {#setting-image-caption}

The image caption can be set in two ways.

1.  Using the Org `#+CAPTION` keyword
2.  Using `#+ATTR_HTML: :caption my caption`

The `#+CAPTION` is available will get the higher precedence. In the
below image, caption is set using that:

Some text before image.

{{<figure src="/images/org-mode-unicorn-logo.png" caption="A unicorn!">}}
Some more text, after image.

Below, the same caption is set using the `#+ATTR_HTML` method instead:

Some text before image.

{{<figure src="/images/org-mode-unicorn-logo.png" caption="A unicorn!">}}
Some more text, after image.


## Setting image size {#setting-image-size}


### Setting `:width` parameter {#setting-width-parameter}

The image [width](https://www.w3schools.com/tags/att_img_width.asp) can be specified in **pixels** using the `:width`
parameter. **The height of the image will be resized proportionally.**

Below image is shown 50 pixels wide.

{{<figure src="/images/org-mode-unicorn-logo.png" width="50">}}

Below image is shown 100 pixels wide.

{{<figure src="/images/org-mode-unicorn-logo.png" width="100">}}

Below image is shown with a width of 1000 pixels! Now the size of this
image is 200px × 200px. But the image will still show up in 1000px ×
1000px size, but obviously heavily pixelated!

{{<figure src="/images/org-mode-unicorn-logo.png" width="1000">}}


### Setting `:height` parameter {#setting-height-parameter}

**NOTE**: Support for specifying `height` parameter to the Hugo `figure`
 shortcut was only added recently in [hugo PR #4018](https://github.com/gohugoio/hugo/pull/4018). So setting this
 parameter will need **hugo v0.31** or newer.

---

The image [height](https://www.w3schools.com/tags/att_img_height.asp) can be specified in **pixels** using the `:height`
parameter. **The weight of the image will be resized proportionally.**

Below image is shown 50 pixels tall.

{{<figure src="/images/org-mode-unicorn-logo.png" height="50">}}

Below image is shown 100 pixels tall.

{{<figure src="/images/org-mode-unicorn-logo.png" height="100">}}

Below image is shown with a height of 1000 pixels! Now the size of
this image is 200px × 200px. But the image will still show up in
1000px × 1000px size, but obviously heavily pixelated!

{{<figure src="/images/org-mode-unicorn-logo.png" height="1000">}}


### Setting both `:width` and `:height` {#setting-both-width-and-height}

The **NOTE** above applies here too.. needs **hugo v0.31** or newer.

The figure sizes below are intentionally set _mis-proportionally_ just
for testing.

-   `:width 100 :height 200`

    {{<figure src="/images/org-mode-unicorn-logo.png" width="100" height="200">}}
-   `:width 200 :height 100`

    {{<figure src="/images/org-mode-unicorn-logo.png" width="200" height="100">}}


## Other {#other}

Similarly, `:link`, `:attr`, `:attrlink` parameters in `#+ATTR_HTML`
are also supported to set the corresponding parameter in the Hugo
`figure` shortcode.