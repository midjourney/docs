# FAQs
 
- [FAQs](#faqs)
  - [DMing the Bot](#dming-the-bot)
  - [Using Discord Tools](#using-discord-tools)
  - [Bot Commands](#bot-commands)
  - [Upscaling](#upscaling)
  - [Seeds](#seeds)
  - [Using Dimensions](#using-dimensions)
  - [Gallery Use](#gallery-use)
  - [Image Prompt Questions](#image-prompt-questions)
  - [Text Prompt Questions](#text-prompt-questions)


## DMing the Bot


**Q: How do I DM the bot?**

A: The easiest way to initiate a DM conversation with the bot is to reply to a generation you made in a bot channel with the envelope emoji, :envelope:, and it will open a DM conversation with you in Discord.  You will have to find it in your Discord Home, where Direct Messages and listed.  Click on the **MidJourney Bot**.  Now you can use the `/imagine` command and other commands listed below.

**Q: I thought my DM images were private. Why are they being moderated?**

They are not private unless you have paid for `/private` mode.  Images created in DM (or via sub-threads) are still viewable by others in the gallery feed unless you have specified you are `/private`.


**Q: The bot should have DM'ed me because I used ✉️, but I don't see any messages.**

A: Right-click on the server -> Privacy settings -> Allow direct messages from server members.


## Using Discord Tools


**Q: How do I create a thread?**

Click on the icon with the # on top of a bot channel.  It will allow you to view and create threads.  Note, they are still public and subject to content moderation guidelines.

[https://support.discord.com/hc/article\_attachments/4403200565911/create\_thread.gif](https://support.discord.com/hc/article\_attachments/4403200565911/create\_thread.gif)

{% embed url="https://support.discord.com/hc/article_attachments/4403200565911/create_thread.gif" %}


**Q: What's a bot channel?**

A: Any channel where you can use the `/imagine` command and make images. On the Discord server, they are marked as **"Image Generation"** channels.  Most commands below require you to be in a bot channel.


**Q: Do the different bot channels have different image generation settings?**

A: No, the bot is the same in all of them.


## Bot Commands


**Q: What exactly does the ↻ button do?**

A: The ↻ submits the same job again, which will run with a different seed. You will see more variations.


**Q: I'm having trouble using the bot - how do I use /imagine?**

A: When you type /imagine try clicking on the box that pops up that says "prompt".  It should say /imagine prompt then type what you want. Like this:

[https://cdn.discordapp.com/attachments/961148616884506674/969225978356326470/ImaginePrompt.gif](https://cdn.discordapp.com/attachments/961148616884506674/969225978356326470/ImaginePrompt.gif)

{% embed url="https://cdn.discordapp.com/attachments/961148616884506674/969225978356326470/ImaginePrompt.gif" %}

**Q: How do I see how many credits I have?**

A: Use `/info` in a bot channel.

**Q: My images say "relaxed", how do I change this?**

A: Use `/fast` in a bot channel. This will enable fast generation, but you will be incrementally charged for each image if you are out of fast credits.

**Q: My images say "metered, fast". I don't want to be charged!**

A: Use `/relax` in a bot channel. This will cost you nothing but images will take longer to generate.

**Q: I don't want anyone to see my images and prompts.**

A: Use `/private` in a bot channel. This will make your images private and hidden from the website, but costs more.  It's a subscription upgrade.

**Q: How many jobs can be generating at once?**

A: You can have 3 jobs going at once (of any kind, 2x2, upscale etc). If you submit a 4th job or more you will get this message: 

""Your job will start shortly
You have reached the maximum allowed number of concurrent jobs. Don't worry, this job will start as soon as another one finishes!"""

**Q: How many concurrent jobs can I run? How many can I queue?**

A: You can generate 3 images at once. If you start more jobs you'll get a message saying "your job will start shortly". You can start 10 jobs before your queue is full. If you are in relax mode this decreases to 2 concurrent images at once.

**Q: How do I invite someone?**

A: In a bot channel, type `/invite`.  It will create a one-time use link for you to copy and send to the person you want to invite.  Don't lose it!  It's safest to do this in your DM channel with the bot, if you are a subscriber.

[https://cdn.discordapp.com/attachments/961148616884506674/973955120721174538/invite2.gif](https://cdn.discordapp.com/attachments/961148616884506674/973955120721174538/invite2.gif)

{% embed url="https://cdn.discordapp.com/attachments/961148616884506674/973955120721174538/invite2.gif"}


## Upscaling

**Q: The upscale adds too much detail. How can I just change the resolution of one of the image from the 2x2 preview grid?**

A: React to your image with :envelope: and it will send you the separate images in DM. You can then change the resolution using a program on your computer. 

**Q: Is there any way to upscale an image and get the video of the process/final result using the --video command**

A: We don't support videos for upscaling yet.


## Seeds

**Q: How do I get the seed or job id that was used for an image (e.g. so I can report a bug or so I can reuse it to generate a similar image)?**

A: React to your image with :envelope: and it will send it to you in DM.

<img width="400" alt="FileID_Step1" src="https://user-images.githubusercontent.com/105028755/167305579-1b2c461f-03d7-4aad-b14e-9ce0dd74fd9a.png">
<img width="400" alt="FileID_Step2" src="https://user-images.githubusercontent.com/105028755/167305633-95ad0e19-0754-4b69-b305-f74a554c8d6f.png">

**Q: Are the 4 initial images generated with the same seed?**

A: In a way yes. We use the seed to generate noise(think randomness) for all 4 images at once so the noise is different for each image. 

**Q: Does submitting the job again use a different seed?**

A: Yes, unless you specify --seed

**Q: What exactly does --seed stabilize?**

A: Seed means that the random noise we add during the initialization of the generation will be the same each time but gpus are non-deterministic, so the images won't look exactly the same. 

## Using Dimensions

**Q: Certain dimensions specified with —h y —w x will generate less images than the normal 4 (3 to 1), is there some reason for this?**

A: The gpus we use have a finite amount of memory, larger images means each one takes up more memory so we have to generate less. 

## Gallery Use

**Q: Where is the gallery?**

Go to [https://gallery.midjourney.com/](https://gallery.midjourney.com/).

**Q: Is there a way to save all my images at once?**

A: We don't have a batch download feature yet. The fastest is to go to your web gallery feed, open an image, then click on the save icon. You can use the right arrow to move to the next image and repeat the operation.

## Image Prompt Questions

Go to [Image Prompt Questions](image-prompt-questions.md).

## Text Prompt Questions

Go to [Text Prompt Questions](text-prompt-questions.md).