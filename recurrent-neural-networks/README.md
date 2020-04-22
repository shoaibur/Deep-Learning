# Recurrent Neural Networks
### Introduction
Feedforward and convolutional neural networks provide outputs based on the current inputs. These networks do not consider any inputs or state of the inputs prior to their current states. However, biological neural networks use a lot a recurrent connection, i.e., use the previous inputs in addition to the current inputs. In other words, the biological neural networks "memorize" some of its previous input states and use them later when needed. Recurrent neural networks (RNNs) introduce this "memory" component in the operations performed by the artificial neural networks.

The first attempt to introduce memory in the neural networks was to use time delay neural network (TDNN). In TDNN, the inputs are time-delayed (think of a delay block!) and are fed into the next layers of the network. However, this network can introduce memory of a certain time window, i.e., the memory is limited by the number of the time-delay block. This invention was followed by other simple RNNs, like Elman network or Jordan network. Notably, although these networks paved the paths toward the state-of-the-art developments of RNNs, all these earlier networks suffered from a problem called vanishing gradient.

In mid-nineties, long short-term memory (LSTM) cell was invented to overcome the vanishing gradient problem. The key novel of LSTM is that some signals, also called state variables, are kept fixed by using gates, and reintroduce or not at the appropriate time in the future. In this way, arbitrary time interval can be represented, and temporal dependencies can be captured. Further refinement of this idea was proposed by discovering gradient recurrent units (GRUs).

### Applications of RNNs
* Speech recognition - Examples include Google's Assistant, Apple's Siri, Amazon's Alexa, Nuance's Dragon Solutions, etc.
* Time series prediction - Examples include stock price prediction, traffic patterns prediction, movie selection, etc.
* Natural language processing - Example includes machine translation (Google, salesforce), question answering (Google analytics), chatbots, etc.
* Gesture recognition - Capture gesture by analyzing a sequence of frames, for example, to recognize if a person is waving a hand or swinging it. Qualcomm, EyeSight, Intel, GestureTek, GestSure, Omek are some of the companies who use gesture recognition techniques in many of their products.


### Basic concepts of RNNs
* RNN at time t and t+1
  * At time t+1, state variable s<sub>t</sub> is used as the input to the network. State variable s<sub>t</sub> is the output from the network, specifically, from layer L, at time t. This output goes as the input to the layer L in the next time point. 
* Folded vs. unfolded representations of the RNN
* Single vs. multi-layer RNNs
* Backpropagation through time (BPTT)

# LSTM
  * LSTM with 4 standard gates
  * Peephole LSTM and GRU

# Hyperparameters
  * Optimizer hyperparameters
    * Learning rate - The most important one. 
    * Mini-batch size
    * Number of epochs
  * Model hyperparameters
    * Number of hidden units
    * Number of hidden layers
    * Cell type
    * Word embedding size
