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
