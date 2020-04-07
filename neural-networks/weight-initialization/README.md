# Weight initialization

Here, we will ...
* Investigage the importance of proper weight initialization technique to achieve desired performance of the deep learning algorithms.
* Use an example dataset: Fashion MNIST from torchvision package.
* Investigate eight (8) methods of initialization of the weights in the deep learning models. Weights will be initialized with...
  1. All zeros
  2. All ones
  3. Uniform distribution, U ~ (0, 1)
  4. Uniform distribution, U ~ (-0.5, 0.5)
  5. Uniform distribution, U ~ (-y, y), where, y = sqrt( 1/ number of input features in the given layer )
  6. Normal distribution, N ~ (0, 1)
  7. Normal distribution, N ~ (0, y), where, y = sqrt( 1/ number of input features in the given layer )
  8. Normal distribution, N ~ (0, y), where, y = sqrt( 1/ number of input and ouput features in the given layer )
