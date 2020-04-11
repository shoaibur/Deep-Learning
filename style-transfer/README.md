# Style Transfer

Content image - The image whose style needs to be modified.
Style image - Style of this image will be transfered to the content image
Target image - contains content of the content image and style of the style image.

C<sub>C</sub> and S<sub>C</sub>: Content and style of the content image, respectively.

So, we need to separte the content and style from both content image and style image
Content image = content + style
Style image = content + style



VGG19 architecture
input image >>
conv1_1, ReLU > conv1_2, ReLU > MaxPool_1 >>
conv2_1, ReLU > conv2_2, ReLU > MaxPool_2 >>
conv3_1, ReLU > conv3_2, ReLU > conv3_3, ReLU > conv3_4, ReLU > MaxPool_3 >>
conv4_1, ReLU > conv4_2, ReLU > conv4_3, ReLU > conv4_4, ReLU > MaxPool_4 >>
conv5_1, ReLU > conv5_2, ReLU > conv5_3, ReLU > conv5_4, ReLU > MaxPool_5 >>
fc1 >> fc2 >> fc3, Softmax
