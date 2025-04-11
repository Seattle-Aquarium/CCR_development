# AI_image_processing

## Background
We equip our ROV with two downard-facing GoPro HERO12 cameras to take images of the seafloor during flights.
Both cameras capture RAW images at 3-second intervals across four transects, leaving us with hundreds to a 1000+ unedited `.GPR` images.
Each image requires a substantial amount of cleaning in Adobe Lightroom Classic before any meaningful data may be extracted from it.
These images help us identify key characteristics about each site, including community composition and substrate.

We sort our `.GPR` images into folders based on their associated transect.
Once the transects are organized, we typically begin the editing process by applying the denoise feature to all of the images, then we choose a single image with a white patch to crop, white balance, and make any other adjustments to Tone and Presence. 
We copy the settings from this lone image and paste to all other images to achieve a baseline level of quality for the entire set.
The final results are `.JPEG` images that have been cropped, color-corrected, denoised, and brightened significantly ([see example transect](https://www.dropbox.com/scl/fo/nkgka51g6zmk94c3je1zm/APA28IzNJSZ-_4uRkBHgLk0?rlkey=p7knm31b0la2kudx235fx3h72&st=ummi5snl&dl=0)).

## The Problem
However, the time it takes to edit a single transect is a major time-limiting factor to our workflow.
Under our current editing method, only images closest in the set to the baseline image become satisfactory.
Those images further from the origin require manual readjustments as the physical conditions of the seafloor change, meaning we must trace through the whole set to ensure every image is usable.

## The Proposed Solution
We seek to incorporate some aspects of machine learning into our image processing methods to cut down on editing time.
We have thousands of edited `.JPEG` images, preview `.JPEG` images, and unedited `.GPR` files to help inform potential machine learning algorithms ([see examples](https://www.dropbox.com/scl/fo/ydtj9jelnbfsdm260vjqm/AI3v0hELR70864K-PVWP_zA?rlkey=bmjk2xysma4u9c56ay92ifnng&st=fo332qp6&dl=0)).
There appear to be some AI-powered image editing software available, such as [Aftershoot](https://aftershoot.com/edit/) or [Imagen](https://imagen-ai.com/).
But with no trained editors on our team, we lack the experience to make an informed choice and do not know of any preferable alternatives.