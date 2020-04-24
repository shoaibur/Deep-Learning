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

