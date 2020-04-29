# Style Transfer
Concept: Use already trained model to solve problems with new data.


## Content, style and target images
Content image - The image whose style needs to be modified.

Style image - Style of this image will be transfered to the content image

Target image - contains content of the content image and style of the style image.


Content image = content of content image + style of content image

Style image = content of style image + style of style image

Target image = content of content image + style of style image

## Model architecture
Lets take VGG19 architecture for style transfer.

input image >>

conv1_1, ReLU > conv1_2, ReLU > MaxPool_1 >>

conv2_1, ReLU > conv2_2, ReLU > MaxPool_2 >>

conv3_1, ReLU > conv3_2, ReLU > conv3_3, ReLU > conv3_4, ReLU > MaxPool_3 >>

conv4_1, ReLU > conv4_2, ReLU > conv4_3, ReLU > conv4_4, ReLU > MaxPool_4 >>

conv5_1, ReLU > conv5_2, ReLU > conv5_3, ReLU > conv5_4, ReLU > MaxPool_5 >>

fc1 >> fc2 >> fc3, Softmax



## Optimize
We need to minimize the total loss contributed from content loss and style loss.

Lets say, we the content representations from conv4_2 layer, while style representations from conv1_1, conv2_1, conv3_1, conv4_1 and conv5_1 layers. The representations in these layers commonly known as feature maps or features.

### Content loss
L<sub>content</sub> = mean ( target_image_features[conv4_2] - content_image_features[conv4_2] )<sup>2</sup>

### Style loss
L<sub>style</sub> = sum_i ( N<sub>layer</sub> * mean ( target_image_gram[layer] - content_image_gram[layer] )<sup>2</sup> )

where, layer = conv1_1, conv2_1, conv3_1, conv4_1 and conv5_1, N<sub>layer</sub> = 1 / total number of elements in the current layer, and image_gram[layer] is the gram matrix of the layer for the image.

For computing gram matrix, let's consider that the features of a given layer has a shape of (number of channels x Height x Width) = (nC x H x W). We first convert the features into a 2D shape of (nC x HW) and then the gram matrix of a given image is computed as: gram matrix = features * transpose of features. Note that the shape of the gram matrix is (nC x nC), which is independent of the spatial dimension of the features. For the target and style images,

target_image_gram[layer] = target_image_features[layer] * target_image_features[layer]<sup>T</sup>

style_image_gram[layer] = style_image_features[layer] * style_image_features[layer]<sup>T</sup>


### Total loss
Total loss = content_weight * L<sub>content</sub> + sytyle_weight * L<sub>style</sub>
