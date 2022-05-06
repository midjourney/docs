# Common usage questions

Q: The upscale is adding too much details. How could I just change the resolution of one of the image from the 2x2 preview grid?

A: React to your image with :envelope: and it will send you the separate images in DM. You can upscale them using a seprate tool like Topaz

Q: What external tools can I use for upscaling without adding details?

A: Some users have great success with Topaz Gigapixel, Pixelmator Pro, BigJpg or ESRGAN\
[https://www.topazlabs.com/gigapixel-ai](https://www.topazlabs.com/gigapixel-ai)\
[https://www.pixelmator.com/support/guide/pixelmator-photo/797](https://www.pixelmator.com/support/guide/pixelmator-photo/797)\
[https://bigjpg.com/](https://bigjpg.com)\
[https://github.com/xinntao/Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN)

Q: How many concurrent jobs can I run? How many can I queue?

A: You can generate 3 images at once. If you start more jobs you will get a message saying "your job will start shortly". You can start 10 jobs before your queue is full. If you are in relax mode this decreases to 2 images at once.

Q: Is there a way to use init images?

A: We don't currently support init images. The closest we have is an image prompt, which is like a text prompt so it's not guaranteed to look like the image. See the docs for how to use images prompt with weights.&#x20;

Q: I'm having trouble using the bot - how do I use /imagine?

A: When you type /imagine try clicking on the box that pops up that says "prompt".  It should say /imagine prompt then type what you want. Also check out [Usage screenshots](usage-screenshots.md)

Q: Do the different bot channels have different image generation settings?

A: No, the bot is the same in all of them.

Q: How many jobs can be generating at once?

A: You can have 3 jobs going at once (of any kind, 2x2, upscale etc). If you submit a 4th job or more you will get this message: 

""Your job will start shortly
You have reached the maximum allowed number of concurrent jobs. Don't worry, this job will start as soon as another one finishes!"""


# Less common questions:

Q: Is there any way to upscale an image and get the video of the process/final result using the --video command

A: We don't support videos for upscaling yet.

Q: Certain dimensions specified with —h y —w x will generate less images than the normal 4 (3 to 1), is there some reason for this?

A: The gpus we use have a finite amount of memory, larger images means each one takes up more memory so we have to generate less. 

Q: Is there a way to "make variations" but change the text that it is following for the upscaling process?

A: Not yet

Q: Are the 4 initial images generated with the same seed? 

A: In a way yes. we use the seed to generate noise(think randomness) for all 4 images at once so the noise is different for each image. 

Q: Does submitting the job again use a different seed?

A: Yes, unless you specify --seed

Q: What exactly does --seed stabilize?

A: Seed means that the random noise we add during the initialization of the generation will be the same each time but gpus are non-deterministic, so the images won't look exactly the same. 

Q: What exactly does the ↻ button do?

A: The ↻ submits the same job again.


Q Is there a way to save all my images at once? 

A: We don't have a batch download feature yet. The fastest is to go to your web gallery feed, open an image, then click on the save icon. You can use the right arrow to move to the next image and repeat the operation.
