# Usage docs

### Commands

Commands are functions of the Midjourney bot to be typed in any bot channel or thread

`/imagine` — Creates an image from text (4 images in 50 seconds)

`/ideas` — Give some random ideas for prompts

`/word` — Queries a dictionary of pre-rendered images for words you type (type ! To get a random set of words)

`/style` — Queries a dictionary of pre-rendered images for a style you type (type ! to get a random style, type !query to search for things similar to that query)

`/help` — Displays bot options for handy reference

`/gift credits` — See how many credits you have left to use or to give. You don't need credits for yourself once you subscribe. (this will be removed in near future)

`/gift user [user] [amount]` — Give credits to a specifc user (this will be removed in near future)

`/invite` — Generates an invite link and send it to your DM that you can send someone to join the server. It will give them 25 credits out of your total

`/subscribe` — Subscribe to the 30 days plan

### Parameters

Parameters are bot options that change how the images will be generated

`--vibe` — Uses old algorithm (more vibes, more abstract, sometimes better for macro or textures)

`--fast` — Faster images, less consistency

`--vibefast` — Faster version of the old algorithm 

`--h` — Height of image. Works better as multiple of 64

`--w` — Width of image. Works better as multiple of 64

`--seed` — Sets the random seed, which can sometimes help keep things more steady between generations

`--no` — Negative prompting (`--no plants` would try to remove plants)

`--video` — Saves a progress video, which is sent to you in the :envelope: reaction is triggered DM

`--hd` — Uses a different algorithm that’s potentially better for abstract and landscape prompts.

**Size shortcuts**

`--wallpaper`: `--w 1920 --h 1024 --hd`

`--sl`: `--w 320 --h 256`

`--ml`: `--w 448 --h 320`

`--ll`: `--w 768 --h 512 --hd`

`--sp`: `--w 256 --h 320`

`--mp`: `--w 320 --h 448`

`--lp`: `--w 512 --h 768 --hd`

#### Deprecated

`--hq` —

`--newclip` —

`--stretch` —

`--beta` —

`/pixels` — Like `/imagine` but it returned pixel art

### Image prompting

Add one more more image URLs to your prompt and it will use those images as visual inspiration. You can mix words with images or just have images alone.

`--iw` — Adjusts the weight of the image URLs vs the text (0.5 weights images half and 2 weighs images twice as much)

#### Advanced image weights

You can set weights individually for each image url in the prompt, just include a `--iw` # for each image in the same order they show up at the beginning of the prompt.

An example which weights the second image higher than the first:

```
https://s.mj.run/6zsj7L https://s.mj.run/gWenzZ --iw 0.25 --iw 0.75 --w 384
```

### Advanced text weights

You can suffix any part of the prompt with `::0.5` to give that part a weight of 0.5. If the weight is not specified, it defaults to 1. Some examples: `/imagine hot dog::1 food::-1` - This sends a text prompt of `hot dog` with the weight 1 and `food` of weight -1 `/imagine hot dog::0.5 animal::-0.75` - Sends `hot dog` of weight 0.5 and `animal` of negative 0.75 `/imagine hot dog:: food::-1 animal::` - Sends `hot dog` of weight 1, `food` of weight -1 and `animal` of weight 1 (unspecified weights default to 1)

Watch out for prompts such as `/imagine hot dog animal::-1`, as this will send the prompt of `hot dog animal` with weight -1.

Note, negative weights are VERY strong. ex: `—no pants` \~= `pants::-0.5`

Another gotcha is if the sum of all the prompts sum to 0, you get random junk responses.

### Emoji responses

✉️ — Sends an image to your DMs with job and seed IDs plus image prompt (:envelope: reaction)

⭐️ — Sends an image to the #favorites channel

❌ — Cancels or deletes a generation at any time. Also removes it from the web gallery

### Preferences

`/prefer suffix <text>` This will automatically append this suffix after all prompts you submit. Leave empty to reset.

`/prefer auto_dm` Jobs will be automatically DMed to you.

`/prefer option set <name> <value>` This creates a personal option, which then translates to specified value when you invoke it by prepending it with --. Only you can use this option. For example, `/prefer option set mine --hd --w 512` creates an option called "mine" that translates to `--hd --w 512`. So you can use `/imagine rubber ducks are awesome --mine`, and it will be the exact same as if you did `/imagine rubber ducks are awesome --hd --w 512`. Leave the value field empty to delete an option. **NOTE:** Only --options are valid values for the suffix option right now, not just any regular text.

`/prefer option list` This will list your currently set personal options. You may keep a maximum of 20 personal options.
