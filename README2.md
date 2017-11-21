# MPAGS-Project First Draft Readme

The Python program takes in an AFM image of PTCDI on hexagonal-Boron Nitride, filters it and calculates the percentage coverage of the flakes.  This is done as follows:

> Takes in a local image file and plots it as an image

> Flattens the image by aligning the substrate layers on the image

> Performs a percentile filter on the flattened image to sharpen the edges of the flakes

> Performs binary thresholding on the filtered image for all possible threshold values and uses a Gaussian gradient function to find where the proportion of 0s to 1s changes the least, the height just above the substrate level, to find the optimal binary image

> Generates a circular binary structuring element using a specified radius and performs morphological binary closing on the binary image, to remove any non-flake features and noise smaller than the structuring element

> Prints the percentage surface coverage of the flakes for that image.

This is done using a combination of numpy, scipy and matplotlib, all native to Anaconda.
