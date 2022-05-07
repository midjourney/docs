# Usage docs

### Commands

Commands are functions of the Midjourney bot to be typed in any bot channel or thread

`/imagine` Creates an image from text (4 images in 50 seconds)

`/info` Shows information about your profile

`/invite` Generates an invite link and send it to your DM that you can send someone to join the server. It will give them some credits to try out the bot.

`/ideas` Give some random ideas for prompts

`/word` Queries a dictionary of pre-rendered images for words you type (type ! To get a random set of words)

`/style` Queries a dictionary of pre-rendered images for a style you type. Available options will appear as an autocomplete list above the text area (type ! to get a random style)

`/help` Displays bot options for handy reference

`/subscribe` Get a link to the subscription page

`/fast` and `/relax` Toggles between "fast" and "relax" mode. In fast mode, if you are out of credits, your jobs will be incrementally billed. In relax mode, your jobs do not cost credits, but take longer to generate.

`/private` and `/public` Toggles between "private" and "public" mode. In private mode, your jobs are only visible to you. In public mode, your jobs are visible to everyone in the gallery. Access to private mode costs extra 20$ per month.

### Emoji responses

✉️ — Sends an image to your DMs with the seed # and job ID. If the result was a grid, it will send each individual image.

⭐️ — Marks image as "favorite". This shows in a separate feed on the web gallery and sends the image to the #favorites channel.

❌ — Cancels or deletes a generation at any time. It is also removed from the web gallery.

### Parameters

Parameters are bot options that change how the images will be generated

`--w` Width of image. Works better as multiple of 64 (or 128 for `--hd`)

`--h` Height of image. Works better as multiple of 64 (or 128 for `--hd`)

`--seed` Sets the random seed, which can sometimes help keep things more steady / reproducible between generations

`--no` Negative prompting (`--no plants` would try to remove plants)

`--video` Saves a progress video, which is sent to you in the ✉️-triggered DM

`--iw` Sets image prompt weight

`--fast` Faster images, less consistency

`--vibe` Uses old algorithm (more vibes, more abstract, sometimes better for macro or textures)

`--vibefast` Faster version of the old algorithm 

`--hd` Uses a different algorithm that’s potentially better for larger images, but with less consistent composition. Best for abstract and landscape prompts.

**Size shortcuts**

`--wallpaper`: `--w 1920 --h 1024 --hd`

`--sl`: `--w 320 --h 256`

`--ml`: `--w 448 --h 320`

`--ll`: `--w 768 --h 512 --hd`

`--sp`: `--w 256 --h 320`

`--mp`: `--w 320 --h 448`

`--lp`: `--w 512 --h 768 --hd`

### Image prompting

Add one or more image URLs to your prompt and it will use those images as visual inspiration. You can mix words with images or just have images alone.

**Note**: This is *not* the same as building on top of (or "initializing" from) an input image. Midjourney does not currently offer the ability to use an init image.

`--iw` — Adjusts the weight of the image URLs vs the text (0.5 weights images half and 2 weighs images twice as much)

**Note**: There is currently no way to apply different weights to different image prompts. This will be addressed in the future.

### Advanced text weights

You can suffix any part of the prompt with `::0.5` to give that part a weight of 0.5. If the weight is not specified, it defaults to 1.

Some examples:
- `/imagine hot dog::1 food::-1` — This sends a text prompt of `hot dog` with the weight 1 and `food` of weight -1
- `/imagine hot dog::0.5 animal::-0.75` — Sends `hot dog` of weight 0.5 and `animal` of negative 0.75
- `/imagine hot dog:: food::-1 animal` — Sends `hot dog` of weight 1, `food` of weight -1 and `animal` of weight 1

Watch out for prompts such as `/imagine hot dog animal::-1`, as this will send the prompt of `hot dog animal` with weight -1.

**Note**: The `--no` command is equivalent to using weight -0.5.

### Preferences

`/prefer suffix <text>` — This will automatically append this suffix after all prompts you submit. Leave empty to reset.

**Note:** Only --options are currently officially supported as values for the suffix option, not just any regular text.

`/prefer auto_dm True` — Jobs will be automatically DMed to you. Set False to turn this off.

`/prefer option set <name> <value>` — This creates a personal option, which then translates to specified value when you invoke it by prepending it with --. Only you can use this option. For example, `/prefer option set mine --hd --w 512` creates an option called "mine" that translates to `--hd --w 512`. So you can use `/imagine rubber ducks are awesome --mine`, and it will be the exact same as if you did `/imagine rubber ducks are awesome --hd --w 512`. Leave the value field empty to delete an option.

`/prefer option list` — This will list your currently set personal options. You may keep a maximum of 20 personal options.

#### Deprecated

`--hq` `--newclip` `--nostretch` `--beta` `/pixels`
