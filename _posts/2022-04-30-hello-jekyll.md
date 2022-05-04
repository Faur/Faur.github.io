---
layout: post
mathjax: True

title:      "Hello Jekyll!"
permalink:  "hello_jekyll"  # Ensure the link doesn't change
date:       0001-01-01 # Post date # If permalink isn't set
excerpt:    "Simple demonstration of Jekyll and how I setup my blog."
---
> {{ page.excerpt }}
<!-- SHOULD BE IN THE TOP OF EACH POST-->
<!-- TODO: put this into the headder -->

## Why Jekyll

This is my blog. It uses [Jekyll](http://jekyllrb.com/) and almost entirely copies the setup of [Andrej Karpathy's blog](https://github.com/karpathy/karpathy.github.io), which it self is very close to the vanilla Jekyll setup. I.e. don't expect anything fancy.

I chose Jekyll because it is light weight (to use and load), I can reasonably understand what is going on, and once setup it is very quick to write posts using markdown and basic HTML.

YouTube videos, like this one explaining Jekyll, can be embedded with a little HTML like this one:

<!-- EMBED YOUTUBE -->
<div class="imgcap" style="text-align:center;">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/iWowJBRMtpc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    <div class="thecap" > You can embedd YouTube videos by copying the `iframe` from YouTube (-> Share -> Embed)
    </div>
</div>

## Posting and folder structure

Posts are in files on the format: `/_posts/YYYY-MM-DD-NAME-OF-POST.md`. This date is the date that work on the post began.

The `permalink` variable should be set to `NAME-OF-POST`, same as in the file name, and assests should be in a folder: `/assets/NAME-OF-POST/`

The `date` variable should be set to the publish date.

## Code Formating
This is `inline code` and this is a sample code block (supports syntax highlighting): 

``` py
import numpy as np
def foo(x):
    for i in range(x):
        print(i)

foo(5)

# this is not code, this is a comment
```

I like to put the output of code in a separate code block inside a block quote, like so:
> ```
> 0
> 1
> 2
> 3
> 4
> ```


## Math Formatting
Inline math is not made wiht $, it is made with `\\(` `\\)` like this:
\\(\nabla_{W} \log p(y=UP \mid x)  \frac{1}{2} \\)
its strange.

Fancy math is made with `$$` and supports `align` environments like this:
$$
\begin{align}
\nabla_{\theta} E_x[f(x)] &= \nabla_{\theta} \sum_x p(x) f(x) & \text{definition of expectation} \\
& = \sum_x \nabla_{\theta} p(x) f(x) & \text{swap sum and gradient} \\
& = \sum_x p(x) \frac{\nabla_{\theta} p(x)}{p(x)} f(x) & \text{both multiply and divide by } p(x) \\
& = \sum_x p(x) \nabla_{\theta} \log p(x) f(x) & \text{use the fact that } \nabla_{\theta} \log(z) = \frac{1}{z} \nabla_{\theta} z \\
& = E_x[f(x) \nabla_{\theta} \log p(x) ] & \text{definition of expectation}
\end{align}
$$


## Images
<!-- EMBED 1x IMAGE -->
<div class="imgcap">
    <img src="/assets/hello-jekyll/2001 Space Odessey.jpg">
    <div class="thecap" >Image caption. In here you use HTML, not mark down for formatting, e.g. <b>to make bold</b>, and <a href="https://htmlcheatsheet.com/">hyperlinks are made like this</a>
    </div>
</div>


<!-- EMBED 2x IMAGE -->
<div class="imgcap">
<div style="display:inline-block">
    <img src="/assets/hello-jekyll/SpaceX 1128775.png" height="220">
</div>
<div style="display:inline-block; margin-left: 20px;">
    <img src="/assets/hello-jekyll/SpaceX13.jpg" height="220">
</div>
<div class="thecap" style="text-align:justify;">Two images can also be set side-by-side, but you might have to play with the height manually...</div>
</div>


## Text Formatting
Jekyll supports basic formatting such as _italic_ and **bold**. And remember ~~the world is flat.~~
Subscript not supported: H~2~O, and superscript not supported: X^2^.
Emoji's also not supported :joy:


### Footnotes
This is a text with a footnote[^1], that also has a second footnote [^10], the numbers are managed automatically, you can reffer to the same note [^1].

[^1]: And here is the definition.
[^10]: the definition continues.


Horizontal lines are made with `---`

---

### Lists

Bulleted lists
* Top level
    * second 
    * level
        * third
        * level
* Top level

Numbered lists
1. Item one
   1. sub item one
   2. sub item two
   3. sub item three
2. Item two
   1. sub item one
   2. sub item two
   3. sub item three

Task lists
- [x]  Write the press release
- [ ]  Update the website
- [ ]  Contact the media


### Blockquotes
> A sample blockquote.
>
> >Nested blockquotes are
> >also possible.
>
> ## Headers work too
> This is the outer quote again.



<!-- TODO: Put this in the footer -->
<!-- END EACH POST WITH THIS -->
<br><br>

___