# Frequently Asked Questions

* [Frequently Asked Questions (FAQs)](FAQs.md#frequently-asked-questions-faqs)
  * [General Questions](FAQs.md#general-questions)
  * [DMing the Bot (Direct Messaging)](FAQs.md#dming-the-bot-direct-messaging)
  * [Using Discord Channels](FAQs.md#using-discord-channels)
  * [Bot Commands](FAQs.md#bot-commands)
  * [Inviting Friends](FAQs.md#inviting-friends)
  * [Upscaling](FAQs.md#upscaling)
  * [Fast and Relaxed](FAQs.md#fast-and-relaxed)
  * [Seeds](FAQs.md#seeds)
  * [Web Gallery Use](FAQs.md#web-gallery-use)
  * [Image Prompt Questions](FAQs.md#image-prompt-questions)
  * [Text Prompt Questions](FAQs.md#text-prompt-questions)
  * [Error Messages](FAQs.md#errors-and-error-messages)

## General Questions

**Q: What is Midjourney?**

Midjourney is a new research lab focused on new mediums and tools for empowering people.

**Q: Are there any rules?**

* Don't be a jerk.
* Don't use our tools to make images that could inflame, upset, or cause drama. That includes gore and adult content.
* Be respectful to the developers and moderators on the server.
* For more rules, see [#rules](https://discord.com/channels/662267976984297473/964598182225002516/964599412460519476).

**Q: Can I share images?**

You can! When you do pls @midjourney on twitter or link to https://twitter.com/midjourney Example post: "I made these images with tools from @midjourney, you can sign up for their private beta here http://bit.ly/3J2NNVs"

**Q: Can I invite someone to this server?**

Midjourney is now in open beta, which means anyone can join to try the service using the [Discord link](https://discord.gg/midjourney). Type /invite to see the Discord link (`https://discord.gg/midjourney`) they can use.

**Q: Can I do detailed public reviews of the current beta? Can I post screenshots / videos of the Discord?**

Yes! But please specify the date in your review and say the experience is still changing signifigantly.

**Q: Are you taking investment?**

We are not taking equity investment at this time. Business partnerships and donations are welcome.

**Q: I'm a reporter / blogger and want to write something**

Please reach out to press@midjourney.com

**Q: Where does your funding come from?**

Funding comes from business partnerships, donations, and our own savings.

**Q: What's the business model for what we're using here?**

We're figuring things out, but our goal is to allow as many people access to these technologies as possible.

**Q: Can I help? Are you hiring?**

Yes! Email careers@midjourney.com about what you enjoy doing (twitter/linkedin/resume helps us respond faster) ﻿

**Q: Can we use images for commercial projects?**

Check the [Terms of Service](terms-of-service.md) for some basic terms and contact @DavidH if you have anything big you need something custom for

## DMing the Bot (Direct Messaging)

**Q: How do I DM the bot?**

A: The easiest way to initiate a DM conversation with the bot is to reply to a generation you made in a bot channel with the envelope emoji, :envelope:, and it will open a DM conversation with you in Discord. You will have to find it in your Discord Home, where Direct Messages and listed. Click on the **MidJourney Bot**. Now you can use the `/imagine` command and other commands listed below. Please note the images will still appear on your gallery unless you use /private.

You can also right-click on the bot in any bot channel, and you should see the option to message the bot.

{% embed url="https://cdn.discordapp.com/attachments/961148616884506674/981338414194507776/Discord_fzI0SoDLV8.gif" %}
Right-click on the bot in a bot channel (where the bot is creating images)
{% endembed %}

**Q: I thought my DM images were private. Why are they being moderated?**

Images created in DMs and with /private are still viewable by moderators and the Midjourney team.

**Q: The bot should have DM'ed me because I used ✉️, but I don't see any messages.**

A: Right-click on the server -> Privacy settings -> Allow direct messages from server members.

{% embed url="https://cdn.discordapp.com/attachments/961148616884506674/981338414479712356/Discord_vCUySZbwMa.gif" %}
How to change privacy settings
{% endembed %}

## Using Discord Channels

**Q: How do I create a thread?**

Click on the icon with the # on top of a bot channel. It will allow you to view and create threads. Note, they are still public and subject to content moderation guidelines.

![https://support.discord.com/hc/article\_attachments/4403200565911/create\_thread.gif](https://support.discord.com/hc/article\_attachments/4403200565911/create\_thread.gif)

**Q: What's a bot channel?**

A: Any channel where you can use the `/imagine` command and make images. On the Discord server, they are marked as **"Image Generation"** channels. Most commands below require you to be in a bot channel.

**Q: Do the different bot channels have different image generation settings?**

A: No, the bot is the same in all of them.

**Q: I've been kicked out of #newbies-534, or want to move channels but still have access to my work. What can I do?**

A:  You can move your image grids to another channel using the `/show` command.  You can now use the `/show <jobid>` command to produce the resulting image and upscale+variation buttons, based on a job id.&#x20;

This allows you to take a job into a different channel, upscale a job from an archived thread, or other similar situations.&#x20;

**Q: How do I find this job id?**&#x20;

A: Job ids look like this:`e8913dc8-75fa-4b7e-8b61-028b8f43c792`. It can be found in the first part of all image filenames, in the URLs on the website, and other places. It's a unique identifier, and you can only use `/show` on jobs that you are the author of. This will also work on "refreshing" old jobs, so if your button click fails on something you made two months ago, you can use `/show` on this job and continue prompting!

## Bot Commands

**Q: What exactly does the ↻ button do?**

A: The ↻ submits the same job again, which will run with a different seed. You will see more variations.

**Q: I'm having trouble using the bot - how do I use /imagine?**

A: When you type /imagine try clicking on the box that pops up that says "prompt". It should say /imagine prompt then type what you want. Like this:

![https://cdn.discordapp.com/attachments/961148616884506674/969225978356326470/ImaginePrompt.gif](https://cdn.discordapp.com/attachments/961148616884506674/969225978356326470/ImaginePrompt.gif)

If you don't see the /imagine option, update your Discord app, re-log-in, and check your subscription (see Errors).

**Q: How do I see how many jobs I have left?**

A: Use `/info` in a bot channel to check your subscription status and usage.

**Q: My images say "relaxed", how do I change this?**

A: Use `/fast` in a bot channel. This will enable fast generation, but you will be incrementally charged for each image if you are out of fast jobs.

**Q: My images say "metered, fast". I don't want to be charged!**

A: Use `/relax` in a bot channel. This will cost you nothing but images will take longer to generate.

**Q: I don't want anyone to see my images and prompts.**

A: Use `/private` in a bot channel. This will make your images private and hidden from the website, but costs more. It's a subscription upgrade.

**Q: How many jobs can be generating at once?**

A: You can have 3 jobs going at once (of any kind, 2x2, upscale etc). If you submit a 4th job or more you will get this message:

""Your job will start shortly You have reached the maximum allowed number of concurrent jobs. Don't worry, this job will start as soon as another one finishes!"""

**Q: How many concurrent jobs can I run? How many can I queue?**

A: You can generate 3 images at once. If you start more jobs you'll get a message saying "your job will start shortly." You can start 10 jobs before your queue is full. If you are in relax mode this decreases to 2 concurrent images at once.



## Inviting Friends

Midjourney is now in open beta, which means anyone can join to try the service using the [Discord link](https://discord.gg/midjourney). Type /invite to see the Discord link (`https://discord.gg/midjourney`) they can use.

## Upscaling

**Q: The upscale adds too much detail. How can I just change the resolution of one of the image from the 2x2 preview grid?**

A: React to your image with :envelope: and it will send you the separate images in DM. You can then change the resolution using a program on your computer.

**Q How can I prevent preview and upscale to add too much details?**

A: You can use `--stop 80` and replace `80` with the % you want to stop at. Use `--uplight` for the upscale to add less details, or redo it with the button "Light Upscale Redo" afterwards.

**Q: Is there any way to upscale an image and get the video of the process/final result using the --video command**

A: We don't support videos for upscaling right now.

**Q: I don't see the Max Upscale option.**

A: This feature is only available in /fast mode and when --w and --h are under 512.

**Q: What is "Light Upscale Redo"?**

This option redoes the upscaling, with a different algorithm which you may prefer.

**Q: What is the maximum upscale resolution?**

A: 3 megapixels.



You might also find the page [Understanding Image Size](resource-links/understanding-image-size.md) useful.

## Fast and Relaxed

We have two modes for image generation, “fast” and “relax”. Fast tries to give you a GPU instantly. It's our highest priority processing tier, and it's kinda expensive. “Relax” puts you in a queue behind others based on how much you’ve used the system.

Right now, we give 15 gpu-hours/mo of ‘fast’ with the ‘Standard’ plan and 200 gpu-minutes/mo with the ‘Basic’ plan.

One hour is roughly 60 image generation or upscale commands and roughly 200 image variation commands.

These numbers are super experimental and may change at any time.

## Seeds

**Q: How do I get the seed or job id that was used for an image (e.g. so I can report a bug or so I can reuse it to generate a similar image)?**

A: React to your image with the envelope emoji :envelope: and it will send it to you in DM.

![FileID\_Step1](https://user-images.githubusercontent.com/105028755/167305579-1b2c461f-03d7-4aad-b14e-9ce0dd74fd9a.png) ![FileID\_Step2](https://user-images.githubusercontent.com/105028755/167305633-95ad0e19-0754-4b69-b305-f74a554c8d6f.png)

**Q: Are the 4 initial images generated with the same seed?**

A: In a way yes. We use the seed to generate noise (think randomness) for all 4 images at once so the noise is different for each image.

**Q: Does submitting the job again use a different seed?**

A: Yes, unless you specify --seed with a number.

**Q: What exactly does --seed stabilize?**

A: Seed means that the random noise we add during the initialization of the generation will be the same each time but GPUs are non-deterministic, so the images won't look exactly the same.



## Web Gallery Use

**Q: Where is the gallery?**

In the [Midjourney Web App](web-app.md). Go to [https://www.midjourney.com/app/](https://www.midjourney.com/app/).

**Q: Is there a way to save all my images at once?**

A: We don't have a batch download feature yet. The fastest is to go to your web gallery feed, open an image, then click on the save icon. You can use the right arrow to move to the next image and repeat the operation.

**Q: What is the Feed?**

The Feed (button on the upper left) is the public record of all upscaled community images. This includes images created in DMs with the bot, and is subject to moderation review. Only if you are in Private (a higher subscription level) will your upscales not show up in the Feed.

## Image Prompt Questions



**Q: How can I attach an image as inspiration?**

A: Type `/imagine` prompt as normal, but then in the prompt section, paste in the web address where the image is stored online. After the link you can still add new text prompts to complement it.  You can see some examples in the **Imagine Parameters** visual guide [here](imagine-parameters.md#image-prompting-with-url).

An image URL must be a direct link to an online image, which you can usually get by right clicking on an image somewhere and choosing `Copy Link Address`. This address will usually end in a `.png` or `.jpg` if it's a usable address. See the gif [here](user-manual.md#image-prompting-with-url) for using one on Discord.

**Q: Any tips regarding using two image sources? The results seem quite random... Is there any way to influence what those two images are doing?**

A: We don't currently support adding individual weights for images, so the most you can do is just set the global image weight with --iw.

**Q: Is there a way to get the "image prompt" to be closer to the initial image, just like "make variations"?**

A: Your best bet is to increase the weight (see above).

**Q: What's the max size I can use for a image prompt? I keep getting this error "Job encountered an error, likely due to lack of memory".**

A: Your problem is more likely due to not using a plain image page as the image prompt. Make sure it's a public URL with an ending of .png or .jpg, not an html page with an image on it somewhere.  You can find the actual source image with a right-click and "Copy Image Address" (or "Copy Image Link").

**Q: Is it possible to choose how much weight is applied to each image using --iw?**

A: The weight specified is applied on all image prompts given to the bot.

**Q: Can an image prompt have a negative weight?**

A: Yes, with --iw -0.5.

**Q: How do I upload or use an image from my hard-drive for an image prompt?**

It needs to be online, with a public URL, which you can do using Discord (see [demo gif](user-manual.md#image-prompting-with-url) here). If it's already online somewhere, right click on the image to 'copy image address (or link)' and go to step 5:

On desktop:

1. Drag an image into Discord
2. Press enter to send it in the chat
3. Click the image in discord so that it's fullscreen
4. Right click it and press "copy image address"
5. Type `/imagine` and then paste the address in the prompt area.

On Mobile:

1. Push the plus in the lower left then click 'upload'
2. Press 'send message' to send it into the chat
3. Click the image in discord so that it's fullscreen
4. Push share then click 'copy url'
5. Type `/imagine` and then paste the address in the prompt area.

**Q: Is there a way to use "init" images for the bot to start from the way some other tools do?**

A: Some image generation tools can take a starting image as the source and modify it. They often call this an "init\_image."  This is not supported by Midjourney at the moment. You can use a url as part of your prompt, along with text if you want, but it is more of a "influence image" than a true init. The details above are about using those image prompts.

## Text Prompt Questions

**Q: Any tips for successful text prompts?**

A: Here is a short guide on effective text prompts: [A short guide on effective text prompts](https://docs.google.com/document/d/1XUT2G9LmkZataHFzmuOtRXnuWBfhvXDAo8DkS--8tec). Also read this page: [Tips on Text Prompts](resource-links/guide-to-prompting.md).

**Q: Is letter case (caps vs lowercase) taken into consideration in producing the results to the prompt?**

A: No, everything is case-insensitive.

**Q: How do you weigh text prompts?**

A:  You can suffix any part of the prompt with `::0.5` to give that part a weight of 0.5. If the weight is not specified, it defaults to 1.&#x20;

Some examples: `/imagine hot dog::2 food::-1` - This sends a text prompt of `hot dog` with the weight 2 and `food` of weight -1.

`/imagine hot dog::0.5 animal::-0.25` - Sends `hot dog` of weight 0.5 and `animal` of negative 0.25.

`/imagine hot dog:: food::-1 animal::` - Sends `hot dog` of weight 1, `food` of weight -1 and `animal` of weight 1 (unspecified weights default to 1).

Watch out for prompts such as `/imagine hot dog animal::-1`, as this will send the prompt of `hot dog animal` with weight -1, because of how it parses the text before the colons.

**Q: What happens if I combine image and text weights?**

A: Here are some recipes from a tricky guide:

* `[image URL] [text prompt 1]` with no weights specified results in a 25% image(s) / 75% text generation.
* `[image URL] [text prompt 1] --iw 1` Results in a 50% image(s) / 50% text generation.
* `[image URL] [text prompt 1]::2 [text prompt 2]::3 --iw` results in a 1/6=17% image(s) , 2/6= 33% text1 , 3/6 = 50% text2.

**Q: Do commas, pipes, or any other punctuation matter?**

A: Yes, the model considers them like a break in the prompt, but it's not always clear what impact this will have. Use `::` between prompts for a hard separator as describe in the answer above.

**Q: What is the length limit for prompts?**

A: Anything over around 60 words will not affect the output, so don't write a novel. (It must stay under 6000 characters.)

## Errors and Error Messages

**Q: "Job encountered an error, likely due to lack of memory"**

A: Try using --w and --h as multiple of 64 and under 1024, e.g. `--w 256 --h 320`

**Q: "Cannot send messages to this user" when trying to DM the bot**

A: Go to Discord privacy settings for this server and toggle this on:

![privacy settings](https://cdn.discordapp.com/attachments/958069758211797092/979275401249574952/unknown.png)

**Q: "Interaction Failed"**

A: The job will (probably) still go through, but it will not show the intermediate images. If you get this with your DMs with the bot, make sure your security settings allow DMs.

**Q: "Server has reached limit of active threads"**

A: We reached the max number of thread we can create in the server. it will be possible to add new threads when older threads will archive. In the meantime, feel free to work in DM.

**Q: I don't have the /imagine option as a slash command.**

A: Especially on mobile, you may need to update the app (via the app store etc) and restart it. Then try the / prompt in a bot channel and see if the /imagine option is listed. Otherwise, is your account subscription active? Try /info to see your status.
