---
description: >-
  An easy to understand explanation of image size, dimensions, resolutions, and
  DPI, by schofe.
---

# Understanding Image Size

There are lots of terms for how "big" an image is. Words like resolution, file size, pixel count, dots per inch, high-res, are used interchangeably by many. Understanding what these words mean can help you get the results you want from Midjourney images.

_This guide is a simplified non-technical way of approaching each concept._



## Image Size Basics

#### Examples will use this simple sailboat picture

![](../.gitbook/assets/Resolution\_MJBoat.png)



### **What is an image file?**

Image files like .jpg, .png, or .gif are instructions for how to create an image. \
Each image is a mosaic of small colored tiles (**pixels**) that form the picture.&#x20;

![Think about image files as a set of instructions on how to arrange colored pixels to create an image.](../.gitbook/assets/Resolution\_Instructions.png)

### What is File Size?

File size is directly related to the amount of information inside the file. In the boat picture, the file contains 10 rows and 10 columns, or 100 pieces of information. If each colored dot is one byte of information, the image file would be 100 bytes.&#x20;

If the file has a grid of 200 x 400 pieces of color information it would be a 80,000 byte file (200\*400=80,000) or 80,000byte/1000 = 80kilobyte file

#### Image Dimensions

People generally don't talk about the file size of an image in kilobytes or megabytes, they talk about the dimensions (the number of columns and rows information) of the image. The boat.jpg example above would be described as a 10x10 pixel image.&#x20;

1024x1024, 720p, 4K, are all shorthand ways of talking about the pixel dimensions of an image.



There are no "high-res" image files when working on a monitors, phones, TVs or other screens. The only thing that matters is how much information you have (the image dimensions) vs. the size of the display.

The boat.jpg image might be a great size on a vintage flip phone, fine on your tablet, and not enough on your brand-new monitor.

![The same image dimension seen on multiple screens](../.gitbook/assets/Resolution\_screenSize.png)

### DPI Dots Per Inch

Dots Per Inch, Pixels Per Inch, Dots Per Centimeter, Points Per Inch all refer to generally the same concept. The amount of information in a given length. 300 "dots" per inch means there are 300 pieces of color information (pixels, printed CMYK dots, etc) in each inch.

DPI is **NOT** a measurement that is useful on screens. The **dimensions** of the file are what matters on screen. DPI is **VERY** important when printing. The basic standard for a great looking print is 300 dots of color in every inch. 300DPI is the point where the individual dots are so closely packed together you can't distinguish individual dots and the picture looks smooth and crisp.

#### So... What DPI is this file?

It depends! Knowing that your file only contains instructions on how to make an image, the DPI is only determined when you tell the printer how closely or loosely that information is packed together.

Think about building the file with Legos.  You can take the same set of instructions and if you have a pile of small 1x1 bricks you pack your information into a smaller space than if you start with a pile of 2x2 bricks

![The same "file instructions" using two sizes of tiles ](../.gitbook/assets/Resolution\_TileSize.png)

#### A Simplified Example of the Math

For this example, you have a 1200x1200 pixel image.  What DPI is that image? It depends on how large you want it to print out.

1200/300 = 4. A 1200x1200 pixel image would produce an great looking 4in x 4in image.

1200/150 = 8. A 1200x1200 pixel image would produce an OK looking 8in x 8in image.

1200/100 = 12. A 1200x1200 pixel image would produce an pretty bad looking 12in x 12in image.&#x20;





## Midjourney Image Sizes

The default size of the initial 2x2 grid is 512x512 pixels.

The default upscale size is 1024 x 1024 pixels.

The default upscale to max size is 1664 x 1664 pixels.

![](<../.gitbook/assets/Image Comparisson.png>)

Lots of other aspect ratios can be generated, but **the maximum file size Midjourney can generate is about 3 megabytes.**

An upscaled default square image at 1664x1664 has 2,768,896 pixels. Let's round that to 3million for simplicity. These 3 million pixels could be a 10x300,000 pixel image, a 100x30,000 pixel image or any other aspect ratio. You can not go above that 3mb ceiling though, so you could not make a typical 4K (3840 x 2160) image because it would be over 8 million pixels.

#### Okay, I put  `--w 448` on my prompt and I didn't get a 448 pixel wide image?!

Keep in mind that  `--ar` is better supported and should be used in place of `--w` or `--h`.

The `--w` and `--h` (width and height) modifiers only affect the initial 2x2 grid.  Adding `--w 448` will make the initial 2x2 grid produce individual grid images are 448 pixels wide

![/imagine sailboat --w 448 produces a 896 x 512 beginning grid. Equivalent to using /imagine sailboat --ar 7:4, which is better supported and should be used instead](<../.gitbook/assets/image (1) (1) (1).png>)

When you upscale one of these images it will no longer be 448 pixels wide, but it will maintain the original aspect ratio of your 2x2 grid.

Larger numbers, like `--w 600` will produce a very wide image, but it will not produce a 600 pixel initial grid image because the 2x2 grid is too large, it will be scaled down proportionally.

Again, it's best to use the `--ar` parameter instead. If you want a 448 x 256 image, for example, you can use `--ar 7:4` to generate an image with an equivalent aspect ratio. You can also use reducible fractions, such as `--ar 1344:768`, which will be reduced for you before generating the image.&#x20;

Only certain ratios are currently supported, while others are only supported when upscaling to maximum. If the chosen aspect ratio is not valid, the closest supported ratio will be used instead.



## Can You Print a Midjourney Image?

Absolutely! The quality of your print simply follows the above rules of DPI.  If you want a quality print you need 300 pieces of information in every inch.  So the default 1664x1664 pixel midjourney max-upscale image would produce a good quality 5.5 in x 5.5 in print.

1664 / 300 = 5.55



#### What about upscaling in other programs like Photoshop?

It depends. When you upscale an image you are asking the computer to take a guess at what information should be added. Sometimes it works great, sometimes not.&#x20;

If you have two bricks (pixels) that are very similar in color and try to double the size of the image a new brick will be added between each existing pair of bricks.&#x20;

![Easy to guess what color should be inserted](../.gitbook/assets/Upscale2x.jpg)

The issue with upscaling an image happens when lots of guesses have to be made about what new information is added (you want an image 4 or 6 times larger than the original). Recent AI advancements in upscale technology are really good, but the more guesses you ask the program to make the more errors will be made and the worse the result. &#x20;

![Harder to guess what color should be inserted](<../.gitbook/assets/MJ\_Upscales (1) (1) (1) (1) (1).jpg>)



![Really hard to guess what color should be inserted](../.gitbook/assets/MJ\_Upscales\_4X.jpg)







