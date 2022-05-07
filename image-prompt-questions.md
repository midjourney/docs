# Image prompt questions

Q: How can I attach an image as inspiration?	
A: Type /imagine prompt as normal, but then put in the web address where the image is stored online. After the link you can still add new text prompts.
 
Q: I'm putting in a url but its not working, what is wrong? 

A: Upload your image to discord, for example by posting it in your thread, then open the image and copy the image address

Q: Any tips regarding using two image sources? The results seem quite random... Is there any way to influence what those two images are doing?	
A: We don't currently support adding individual weights for images, so the most you can do is just set the global image weight with --iw 


Q: Is there a way to get the "image prompt" to be closer to the initial image, just like "make variations"?
A: Not currently, "Make variations" uses a feature called init images to basically start the model with a noised image. This isn't available through the bot currently. 

Q: Is there a way to use "init" images for the bot to start from?	
A: "Inits are not supported by Midjourney at the moment You can use a url as part of your prompt, along with text if you want, but it is more of a ""target image"" than an init."

Q: What's the max size I can use for a image prompt? I keep getting this error "Job encountered an error, likely due to lack of memory".	
A: Your problem is more likely due to not using a plain image page as the image prompt. make sure it's a public url with an ending of .png or .jpg, not an html page with an image on it somewhere

Q: Is it possible to choose how much weight is applied to each image using --iw?	
A: The weight specified is applied on all image prompts given to the bot.

Q: Can an image prompt have a negative weight?
A: Yes with --iw -0.5