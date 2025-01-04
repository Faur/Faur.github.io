---
layout: post
mathjax: True

title:      "Blog: Templates!"
permalink:  "blog-templates"      # Ensure the link doesn't change
date:       2025-01-04          # Most recent date
excerpt:    "Living document with basic Jekyll templates."
---

> {{ page.excerpt }}
<!-- SHOULD BE IN THE TOP OF EACH POST-->
<!-- TODO: put this into the headder -->

## Writing and formatting posts

### Text Formatting
Jekyll supports basic formatting such as
*  _italic_ 
* **bold**
* ~~Strikethrough~~

Jekyll doesn't support
1. Subscript: H~2~O
1. Superscript: X^2^
1. Emojis: :joy:

#### Math Formatting
Inline math is made with `\\(` `\\)` like this:
\\(\nabla_{W} \log p(y=UP \mid x)  \frac{1}{2} \\)
its strange.

is not made wiht $, it 

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


### Images
<!-- EMBED 1x IMAGE -->
<div class="imgcap">
    <img src="/assets/hello-jekyll/2001 Space Odessey.jpg">
    <div class="thecap">
        Image caption. In here you use HTML, not mark down for formatting, e.g. <b>to make bold</b>, and <a href="https://htmlcheatsheet.com/">hyperlinks are made like this</a>
    </div>
</div>

<!-- EASY COPY FORMAT:
<div class="imgcap">
    <img src="/assets/XXX">
    <div class="thecap">
        XXX
    </div>
</div>
-->

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


### Embed Youtube videos 
YouTube videos, like this one explaining Jekyll, can be embedded with a little HTML like this one:

<!-- EMBED YOUTUBE -->
<div class="imgcap" style="text-align:center;">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/iWowJBRMtpc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    <div class="thecap" > You can embedd YouTube videos by copying the `iframe` from YouTube.com (-> Share -> Embed)
    </div>
</div>


### Comments
You can make [comments in the markdown file that aren't complied](https://stackoverflow.com/questions/4823468/comments-in-markdown), and there are several options
* `[//]: # COMMENT` should be the most portable comment. It must be on a separate line following a blank line.
* `<!-- COMMENT -->` allows for multi-line and inline comments. <!-- HERE! -->

[//]: # This is a comment that won't show up on the web

<!-- This is also a comment.
This is a comment that won't show up in the 
-->

### Footnotes
Footnotes are made with `[^XXX]` in the text and `[^XXX]: ` on a separate line with the note. `XXX` can be any key that you want [^footer3].
This is a text with a footnote[^1], that also has a second footnote [^10].
Numbering the footnotes is automatic and incrementing.
You can reffer to the same footnote more than once [^1].

[^1]: here is the definition.
[^10]: And another definition.
[^footer3]: Like this.

Horizontal lines are made with `---`

---

### Code Formating
This is `inline code` and this is a sample code block (supports syntax highlighting): 

``` py
import numpy as np
def foo(x):
    # this is not code, this is a comment
    for i in range(x):
        print(i)
foo(5)

```

I like to put the output of code in a separate code block inside a block quote, like so:
> ```
> 0
> 1
> 2
> 3
> 4
> ```

You can also make codeblocks by indenting with 4 spaces, but then you don't get syntax highlighing.



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