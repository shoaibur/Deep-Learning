# Style Transfer

Content image - The image whose style needs to be modified.

Style image - Style of this image will be transfered to the content image

Target image - contains content of the content image and style of the style image.


Content image = content of content image + style of content image

Style image = content of style image + style of style image

Target image = content of content image + style of style image


Lets take VGG19 architecture
'''
input image >>
conv1_1, ReLU > conv1_2, ReLU > MaxPool_1 >>
conv2_1, ReLU > conv2_2, ReLU > MaxPool_2 >>
conv3_1, ReLU > conv3_2, ReLU > conv3_3, ReLU > conv3_4, ReLU > MaxPool_3 >>
conv4_1, ReLU > conv4_2, ReLU > conv4_3, ReLU > conv4_4, ReLU > MaxPool_4 >>
conv5_1, ReLU > conv5_2, ReLU > conv5_3, ReLU > conv5_4, ReLU > MaxPool_5 >>
fc1 >> fc2 >> fc3, Softmax
'''

Lets say, we the content representations from conv4_2 layer, while style representations from conv1_1, conv2_1, conv3_1, conv4_1 and conv5_1 layers. The representations in these layers commonly known as feature maps or features.


Content loss: L<sub>content</sub> = mean ( target_image_features[conv4_2] - content_image_features[conv4_2] )<sup>2</sup>

Style loss: L<sub>style</sub> = sum_i ( N<sub>layer</sub> * mean ( target_image_gram[layer] - content_image_gram[layer] )<sup>2</sup> )

where, layer = conv1_1, conv2_1, conv3_1, conv4_1 and conv5_1 and N<sub>layer</sub> = 1 / total number of elements in the current layer.

Total loss = content_weight * L<sub>content</sub> + sytyle_weight * L<sub>style</sub>
