---
layout: post
title:  "Working with Ricoh Theta S VR Footage"
categories: vr
description: This is my workflow for using VR Footage from a Ricoh Theta S in Premier.
---

The process for working with Ricoh Theta S VR files requires a couple intermediate steps before you can import the footage into Premiere. I can't speak to any other editing software but I would expect it to be the case for others as well.

## What is VR and why should I care?

I'm guessing that since you are here, you probably know what VR is and are looking for the answer to a specific question. If that's the case. You can skip this intro section and get right to the article.

For those that don't know what VR is, here is a brief explanation. 

VR stands for [Virtual Reality](https://en.wikipedia.org/wiki/Virtual_reality). You may have seen ads for VR headsets, in which people with giant headsets grasp at thin air and talk about how amazing it is. For the purposes of this article, we're going to talk about VR as 360 degree video. Consumer priced camera's like the [Ricoh Theta S](http://amzn.to/2fABZfS) can record 360 degrees of footage, allowing you to pan around as the video is playing. You can also pause the video and pan around to look at some specific item or area that has been captured. It's really pretty interesting. Best of all, you don't need a special headset. Most VR can be viewed using your smartphone (especially when uploaded to YouTube), allowing you to pan around by simply changing the direction that your phone is facing.

Here is a rough, sample video of a [walkthrough of my office](https://www.youtube.com/watch?v=K508tGvjkEs), that I created with the Ricoh Theta S. To view the video in VR you must use a supported browser - Chrome or Firefox. Or, you can use your mobile device and the YouTube app.

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed//K508tGvjkEs' frameborder='0' allowfullscreen></iframe></div>

Finally, if you want to use a headset, try a [Google Cardboard compatible headset](http://amzn.to/2fPhdK8). They are pretty cheap and allow you to get a good idea for what VR is all about.

Now that we know what VR is. It's time to get started.

## Getting the files off the camera

Using the Theta S mobile app, you can save your VR files directly to your device (iPhone or iPad) and then import them using the Photos app. I prefer to connect the Ricoh camera to my Mac and import them using the Image Capture app. This seems like a more straightforward process to me. The camera doesn't mount on the desktop when plugged into the Mac, like a GoPro or other camera would, so we need to use the Image Capture app where the camera will show up in your list of devices. Once it shows up, you can then import the files to the location of your choice.

If you try to use the imported files as-is they will show up as two spherical images side by side. 

![Screen capture of spherical images](/images/vr-spherical-images.png "Screen capture of video directly from the Ricoh Theta S")

Not what we want. So begins the process of converting - processing - and injecting our files to make them usable.

Before importing into our video editor, we need to convert the files. We can do this using the [Ricoh Theta app](https://theta360.com/en/support/download/). There are a number of apps available on the download page, including a live streaming app and the mobile apps. We will be using the "[Basic App](https://theta360.com/en/about/application/pc.html)." _I was somewhat surprised to find that the Basic App was an Adobe AIR application. I'm not sure why that surprised me. I guess it's because I hadn't seen an Adobe AIR app in a while._ So, if you don't have Adobe AIR installed, you will be prompted to download and install that before proceeding.

## Top and Bottom Orientation Correction?

In addition to converting the files to a format that can be edited in Premiere, the app also corrects top and bottom orientation in your VR files. Whether you are working with VR files in Premiere or simply uploading to YouTube, you will want to correct the orientation. As I worked through how to prepare files for Premiere, I went through a process of trial and error and was surprised to see that the orientation was incorrect when I uploaded my first VR file to YouTube. Initially, I thought it was a problem with the camera. Then I realized that this needed to be corrected using the Ricoh software.

_As a side note, if you are uploading directly to YouTube, Ricoh provides instructions for an [upload to YouTube workflow](https://theta360.com/en/howto-youtube/)._

## Conversion Process

The conversion process is pretty straightforward. Open the Theta App and drop the files that you want to convert on to the main window. You will then be able to select the location to save the converted file, provide a new name and enable top / bottom correction. Depending on the size of the files to be converted, the process can take a while.

For comparison, I have uploaded a raw file from the Ricoh camera and a converted file to YouTube.

[Raw File from Ricoh Theta S](https://youtu.be/TTKe1Im5Gy4)

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed//TTKe1Im5Gy4' frameborder='0' allowfullscreen></iframe></div>

[File converted with Ricoh App](https://www.youtube.com/watch?v=25WfsXS3Ofc)

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/25WfsXS3Ofc' frameborder='0' allowfullscreen></iframe></div>

As you can see, the file converted with the Ricoh App is the only one that displays properly.

## Importing into Premiere (Finally)

Once the file is converted, you are ready to import it into Premiere and start editing. Editing a VR clip in Premiere is basically the same as with a non-VR video clip. To make previewing your VR content more natural, you will want to enable VR Video display in either the Program or Source monitor. This allows you to pan around your VR the way you would when viewing the video on YouTube. You can read more about this in the [Working with immersive VR video](https://helpx.adobe.com/premiere-pro/kb/work-with-vr.html) article on the Adobe Help site.

## Exporting from Premiere

Once you have finished editing your video in Premiere, the export process is largely unchanged. If you scroll through the settings, you will notice that there is a VR checkbox which should be ticked. Adobe also recommends that you select "Stretch to Fill" in the Source Scaling option.

>Regardless of the Format and Preset you select, be certain to change the Source Scaling option in the Export Settings dialog box to Stretch To Fill. If you don't change this option, you are likely to introduce either letterbox or pillars to the exported video, which breaks the seam of the sphere and distorts it. [- Working with immersive VR video](https://helpx.adobe.com/premiere-pro/kb/work-with-vr.html)

As you can see in the video below, I didn't use the "Stretch to Fill" option and there is a hole (black area) in the video if you pan down as if looking at the floor..

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/EJUzrqhfe2g' frameborder='0' allowfullscreen></iframe></div>

Once you change those settings, export the file.

## Injecting Meta Data

Now that we have the exported file from Premiere, we have one final step which requires another app, this one called [Spatial Media Metadata Injector](https://support.google.com/jump/answer/7044297?hl=en) which adds metadata to the file allowing YouTube to recognize it as a spherical file.

Again, this app is very straightforward. Simply open the app, select the file, tick the "My video is spherical (360)" checkbox and hit "Inject metadata." Once the app finishes, you are now ready to upload the app to YouTube. Once the video has been uploaded to YouTube you can use your web browser (currently Chrome and Firefox are compatible with YouTube VR videos), phone (YouTube app) or a VR Viewer like Google Cardboard to explore the VR video.

Obviously, it would be a lot easier if you didn't have to run your video file through multiple apps to prep it for viewing. I would assume that as the VR format matures and becomes more mainstream, tools like Premiere will do a better job of handling all of these steps. In the mean time, it's a small price to pay for such an interesting technology.
