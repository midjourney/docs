# User Manual

Please make sure you are familiar with the content guidelines and are aware of what is public content in the community. You can find more detail in [Content and Moderation](content-and-moderation-policy.md). This document does not cover everything in the #rules, #faq, #announcements, #status channels, so make sure you check those out!

That said, enjoy creating beautiful images! In this page:

* [User Manual](user-manual.md#user-manual)
  * [Basic Commands in Bot Channels](user-manual.md#basic-commands-in-bot-channels)
  * [Parameters to "/imagine"](user-manual.md#parameters-to-imagine)
  * [Emoji Reactions to Generation Output](user-manual.md#emoji-responses-to-generation-output)
  * [Image Prompting with URL](user-manual.md#image-prompting-with-url)
  * [Advanced Text Weights](user-manual.md#advanced-text-weights)
  * [Discord Prompt Preferences](user-manual.md#discord-prompt-preferences)
  * [Deprecated: May Want To Avoid](user-manual.md#deprecated-may-want-to-avoid)

### Basic Commands in Bot Channels

Commands are functions of the Midjourney bot that can be typed in any bot channel or thread under a bot channel. A bot channel is a channel under the "Image Generation" section on the Discord server.

`/imagine` Creates an image from text (4 images in 50 seconds)

`/info` Shows information about your profile

`/invite` Generates an invite link and send it to your DM that you can send someone to join the server. It will give them some credits to try out the bot.

`/ideas` Give some random ideas for prompt

`/help` Displays bot options for handy reference

`/subscribe` Get a link to the subscription page

`/fast` and `/relax` Toggles between "fast" and "relax" mode. In fast mode, if you are out of credits, your jobs will be incrementally billed. In relax mode, your jobs do not cost credits, but take longer to generate.

`/private` and `/public` Toggles between "private" and "public" mode. In private mode, your jobs are only visible to you. **In public mode, your jobs are visible to everyone in the gallery, even if you are creating them in a thread or a DM.** Access to private mode costs extra 20$ per month.

You can find more documentation on using these in our [FAQs](FAQs.md).

### Parameters to "/imagine"

Parameters are bot options that change how the images will be generated. For instance, a full imagine command might contain several things, like an image URL, some weights, other switches:

`/imagine prompt: http://myimageonline.jpg A forest spirit at night --iw 0.2 --no trees --hd`

`--w` Width of image. Works better as multiple of 64 (or 128 for `--hd`)

`--h` Height of image. Works better as multiple of 64 (or 128 for `--hd`)

`--seed` Sets the random seed, which can sometimes help keep things more steady / reproducible between generations. Any positive integer (e.g., 2, 534, 345554).

`--no` Negative prompting (`--no plants` would try to remove plants)

`--video` Saves a progress video, which is sent to you in the ✉️-triggered DM

`--iw` Sets image prompt weight

`--fast` Faster images, less consistency

`--vibe` Uses old algorithm (more vibes, more abstract, sometimes better for macro or textures)

`--vibefast` Faster version of the old algorithm

`--hd` Uses a different algorithm that’s potentially better for larger images, but with less consistent composition. Best for abstract and landscape prompts.

`--stop` Stop the generation at an earlier percentage. Must be between 10-100

`--uplight` Use "light" upscaler for subsequent upscales. Results are then closer to the original image (less detail added during upscale)

`--sameseed` Sets the same seed across all images of the resulting grid

`--aspect` Sets a desired aspect ratio, instead of manually setting height and width with `--h` and `--w`. Try `--aspect 16:9` for example, to get a 16:9 aspect ratio (\~448x256). (Shortcut `--ar`.)

**Size shortcuts**

`--wallpaper`: `--w 1920 --h 1024 --hd`

`--sl`: `--w 320 --h 256`

`--ml`: `--w 448 --h 320`

`--ll`: `--w 768 --h 512 --hd`

`--sp`: `--w 256 --h 320`

`--mp`: `--w 320 --h 448`

`--lp`: `--w 512 --h 768 --hd`

### Emoji Reactions to Generation Output

"React" to a generation with various emojis to trigger actions from the bot.

![how to add a reaction emoji](.gitbook/assets/reaction\_editing.gif)

✉️ The envelope emoji reaction sends an image to your DMs with the seed # and job ID. If the result was a grid, it will send each individual image. You may have to hunt for this emoji by typing "envelope" in your emoji list.

⭐️ Marks image as "favorite". This shows in a separate feed on the web gallery and sends the image to the #favorites channel.

❌ Cancels or deletes a generation at any time. It is also removed from the web gallery. Please help us by removing content you accidentally generated that is in violation of our PG-13 content guidelines (see [Content and Moderation](content-and-moderation\_policy.md)).

### Image Prompting with URL

Add one or more image URLs to your prompt and it will use those images as visual inspiration. You can mix words with images or just have images alone. See [Image Prompt Questions](FAQs.md#image-prompt-questions) for more info.

**Note**: This is _not_ the same as building on top of (or "initializing" from) an input image. Midjourney does not currently offer the ability to use an init image, due to concerns about community public content.

`--iw` — Adjusts the weight of the image URLs vs the text (0.5 weights images half and 2 weighs images twice as much)

**Note**: There is currently no way to apply different weights to different image prompts. This will be addressed in the future.

### Advanced Text Weights

You can suffix any part of the prompt with `::0.5` to give that part a weight of 0.5. If the weight is not specified, it defaults to 1. See also [Text Prompt Questions](FAQs.md#text-prompt-questions).

Some examples:

* `/imagine hot dog::1 food::-1` — This sends a text prompt of `hot dog` with the weight 1 and `food` of weight -1
* `/imagine hot dog::0.5 animal::-0.75` — Sends `hot dog` of weight 0.5 and `animal` of negative 0.75
* `/imagine hot dog:: food::-1 animal` — Sends `hot dog` of weight 1, `food` of weight -1 and `animal` of weight 1

Watch out for prompts such as `/imagine hot dog animal::-1`, as this will send the prompt of `hot dog animal` with weight -1.

**Note**: The `--no` command is equivalent to using weight -0.5.

### Discord Prompt Preferences

`/prefer suffix <text>` — This will automatically append this suffix after all prompts you submit. Leave empty to reset.

**Note:** Only --options are currently officially supported as values for the suffix option, not just any regular text.

`/prefer auto_dm True` — Jobs will be automatically DMed to you. Set False to turn this off.

`/prefer option set <name> <value>` — This creates a personal option, which then translates to specified value when you invoke it by prepending it with --. Only you can use this option. For example, `/prefer option set mine --hd --w 512` creates an option called "mine" that translates to `--hd --w 512`. So you can use `/imagine rubber ducks are awesome --mine`, and it will be the exact same as if you did `/imagine rubber ducks are awesome --hd --w 512`. Leave the value field empty to delete an option.

`/prefer option list` — This will list your currently set personal options. You may keep a maximum of 20 personal options.

### Deprecated: May Want To Avoid

`--hq` `--newclip` `--nostretch` `--beta` `/pixels`\
``
