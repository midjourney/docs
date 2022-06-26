---
description: An illustrated Guide to /imagine parameters
---

# Imagine Parameters

### Basic Structure

Parameters are bot options that change how the images will be generated. For instance, a full imagine command might contain several things, like an image URL, some weights, other switches. \
\
`/imagine` commands should follow the below order if you use them all:

![/imagine prompt: https://example/tulip.jpg  a field of tulips in the style of Mary Blair --no farms --iw .5 --ar 3:2](.gitbook/assets/ImagineStructure.jpg)



### Sizes

`--w` Width of image. Works better as multiple of 64 (or 128 for `--hd`)

`--h` Height of image. Works better as multiple of 64 (or 128 for `--hd`)

`--w` and `--h` values above 512 are unstable and may cause errors.

![](<.gitbook/assets/image (9).png>) /imagine: prompt **an abstract field of flowers**

![](<.gitbook/assets/image (26).png>) /imagine prompt: **an abstract field of flowers --w 448**



`--aspect`  or `--ar` Sets a desired aspect ratio, instead of manually setting height and width with `--h` and `--w`. &#x20;

Try `--aspect 16:9` for example, to get a 16:9 aspect ratio (\~448x256).

<img src=".gitbook/assets/image (3).png" alt="" data-size="original"> /imagine prompt: **an abstract field of flowers --ar 16:9**



#### Size Shortcuts

`--wallpaper`: `--w 1920 --h 1024 --hd`

`--sl`: `--w 320 --h 256`

`--ml`: `--w 448 --h 320`

`--ll`: `--w 768 --h 512 --hd`

`--sp`: `--w 256 --h 320`

`--mp`: `--w 320 --h 448`

`--lp`: `--w 512 --h 768 --hd`

### Algorithm Modifiers

`--fast` Faster images, less consistency.

![](<.gitbook/assets/image (2).png>)/imagine prompt: **an abstract field of flowers --fast**

``

`--vibe` Uses old algorithm (more vibes, more abstract, sometimes better for macro or textures).

![](<.gitbook/assets/image (12).png>) /imagine prompt: **an abstract field of flowers --vibe**



`--vibefast` Faster version of the old algorithm.

![](<.gitbook/assets/image (23).png>) /imagine prompt: **an abstract field of flowers --vibe fast**

``

`--hd` Uses a different algorithm that’s potentially better for larger images, but with less consistent composition. Best for abstract and landscape prompts.

![](<.gitbook/assets/image (24).png>)/imagine prompt: **an abstract field of flowers --hd**



### Prompt Modifiers

`--no` Negative prompting (e.g., `--no plants` would try to remove plants).  This is like giving it a weight of -0.5.

![](<.gitbook/assets/image (10).png>) /imagine prompt: **an abstract field of flowers --no blue**



### Detail Modifiers

`--stop` Stop the generation at an earlier percentage. Must be between 10-100.

![](<.gitbook/assets/image (8).png>) /imagine prompt: **an abstract field of flowers --stop 50**

****

`--uplight` Use "light" upscaler for subsequent upscales. Light results are closer to the original image with less detail added during upscale.



![](<.gitbook/assets/image (25).png>)![](<.gitbook/assets/image (20).png>)

Normal upscale (left) vs Light Upscale (right)



### Seeds

`--seed` Sets the random seed (an integer), which can sometimes help keep things more steady / reproducible between generations.

![](<.gitbook/assets/image (17).png>) ![](<.gitbook/assets/image (4).png>)

`/imagine prompt: an abstract field of flowers` run twice without a seed.



![](<.gitbook/assets/image (16).png>) ![](<.gitbook/assets/image (5).png>)

`/imagine prompt: an abstract field of flowers --seed 1234` run twice.&#x20;



`--sameseed <number>` Sets the same seed across all images of the resulting grid. \
The `sameseed` can be any positive integer.

![](<.gitbook/assets/image (15).png>) /imagine prompt: **an abstract field of flowers** **--sameseed 1234**

``

### `Progress Videos`

`--video` Saves a progress video. Video will be sent to you in DM by the bot (private message) after you react to the result with the ✉️ emoji.

![](<.gitbook/assets/image (11).png>)

### Image Prompting with URL

`--iw` Sets image prompt weight.  Use a decimal value up to 1 (full strength).

Add one or more image URLs to your prompt and it will use those images as visual inspiration. You can mix words with images or just have images alone. See [Image Prompt Questions](FAQs.md#image-prompt-questions) for more info.

**Note**: This is _not_ the same as building on top of (or "initializing" from) an input image. Midjourney does not currently offer the ability to use an "init" image as seen in some other tools, due to concerns about community public content.

`--iw` — Adjusts the weight of the image URLs vs the text. 0.25 is the default weight. As you increase it to 1, you increase the strength of the image. Experiment and see what you like.

**Note**: There is currently no way to apply different weights to different image prompts. This will be addressed in the future.

Example image prompt:

![](<.gitbook/assets/image (13).png>) Linked Image (this has a long url related to github, but pretend it is "https://example/dots.jpg")

Image prompt use with no `--iw` modifier, `--iw` .5 and `--iw` 1:

![ https://example/dots.jpg abstract field of flowers (left)
&#x20;https://example/dots.jpg abstract field of flowers --iw .5 (center)
&#x20;https://example/dots.jpg abstract field of flowers --iw 1 (right)](.gitbook/assets/MJ\_Imageweights.jpg)



``
