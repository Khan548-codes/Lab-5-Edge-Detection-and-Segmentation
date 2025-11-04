# Lab-5-Edge-Detection-and-Segmentation

Quick Summary of Edge Detection and Segmentation
This part of the experiment was all about finding the edges in an image and then using those edges to split the image into regions (segmentation).

Steps I Took
Simple Edge Filters (Sobel, Prewitt): I started with basic filters like Sobel and Prewitt. These just look for sharp changes in brightness—the gradient—to mark where edges are (Section 1).

Advanced Edge Detection (Canny): I then used the Canny detector. This is a much smarter, multi-step process that first smooths the image, then finds the gradients, and finally cleans up the lines. It gave me much thinner and cleaner edges (Section 2).

Second-Order Edge Detector (LoG): I also tried the Laplacian of Gaussian (LoG) method. This approach first blurs the image slightly (using Gaussian) and then finds edges using the Laplacian. It's good for detail but can be sensitive to noise (Section 3).

Segmentation (Otsu Threshold): Next, I took the edge map and used the Otsu method to create a simple segmentation. Otsu automatically analyzes the image's brightness levels (its histogram) and finds the best cutoff point (threshold) to separate the object from the background, resulting in a binary mask (Section 4).

Visualization: Finally, I counted and colored all the separated, distinct areas on the binary mask to make the segmented regions easy to see and count (Section 5).

What I Learned
The Canny filter clearly produced the best, thinnest, and most accurate edges. It beat out Sobel/Prewitt because it includes steps to remove noise and uses a clever "double threshold" to make sure the lines are connected and clean.

The Otsu method is essentially a smart way of doing histogram thresholding. Instead of guessing where to put the dividing line between 'object' and 'background' brightness, Otsu automatically picks the value that gives the best separation.

![images](https://github.com/Khan548-codes/Lab-5-Edge-Detection-and-Segmentation/blob/main/images/ss1.png)
![images](https://github.com/Khan548-codes/Lab-5-Edge-Detection-and-Segmentation/blob/main/images/ss2.png)
![images](https://github.com/Khan548-codes/Lab-5-Edge-Detection-and-Segmentation/blob/main/images/ss3.png)
![images](https://github.com/Khan548-codes/Lab-5-Edge-Detection-and-Segmentation/blob/main/images/ss4.png)
![images](https://github.com/Khan548-codes/Lab-5-Edge-Detection-and-Segmentation/blob/main/images/ss5.png)
![images](https://github.com/Khan548-codes/Lab-5-Edge-Detection-and-Segmentation/blob/main/images/ss6.png)
