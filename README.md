# MPAGS-Project
Original idea:
So I've previously been working with images of surfaces returned by atomic force microscopes, attached, and a key characteristic of the surface is the flake coverage.  Previously, I was using a ruler and an Excel document of each flake's height and width and approximated them as an ellipses to find their total coverage.

I struggled to make a program that detected flakes in Matlab, as the software didn't like working with such large arrays.  I plan to make a similar program in Python that does the following:
>Reads in a grayscale image of a surface, and displays the image (matplotlib.pyplot.imshow) and a grayscale histogram (matplotlib.pyplot.hist binning a ravel of the grayscale points)


>Applies a median filter (scipy.ndimage.median_filter/scipy.signal.medfilt) to the image and displays it and the histogram as before


>Thresholds the image, based on the histogram of the filtered image


>Prints the percentage of pixels in the image above the threshold ie. the flake coverage.

This would be done using a combination of numpy, scipy, matplotlib and OpenCV.
