# Introduction to OpenCV

### Installation of OpenCV on Anaconda:
conda install opencv

### Import OpenCV and read an image
import cv2

img = cv2.imread(path_to_image)

OpenCV reads an image with color BGR. So, we may want to change the color to RGB.


### Change colors in OpenCV
rgb_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

gray_img = cv2.cvtColor(img, cv2.COLOR_RGB2GRAY)


### Apply filters
filt_img = cv2.filter2D(img, ddepth, kernel)

Input arguments:

img -- input image

ddepth -- desired depth of the output image (filt_img). If ddepth is negative, then the output image will have same depth of the input image.

kernel -- filter that will be applied on the input image (img).

