# Autoencoders

Autoencoders are neural networks used for data compression, signal de-noising and dimensionality reduction. An autoencoder contains an encoder and a decoder.

[insert an image of an autoencoder]

Two major types of auto-encoding methods:

* Linear auto-encoding
  * Use only linear or fully connected layers in both encoder and decoder
  * Example: linear-autoencoder.ipynb

* Convolutional auto-encoding
  * Transpose convolution - Encoder uses convolutional layers, while decoder uses transposed convolutional layers. Transposed convolution is opposite of the convolution operation, but they are not receiprocal. In transposed convolution, a filter/kernel is initialized, each element of the kernel is multiplied by a pixel value, which is repeated for each pixel in the image/feature. With a kernel size of 2 and a stride of 2, transposed convolution increases the spatial dimension by a factor of 2.
    * Example: convolutional-autoencoder.ipynb
  * Upsampling or interpolation - Encoder uses convolutional layers, while decoder uses interpolation techniques. Torch's interpolation function takes arguments scale factor and interpolation mode like nearest neighbors. The spatial dimension of the image increases by a factor equal to the scale factor.
    * Example: convolutional-autoencoder-upsampling.ipynb

Application example - image denoising
 * autoencoder-image-denoising.ipynb
