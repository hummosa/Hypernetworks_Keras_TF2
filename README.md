
## Guide to Hypernetworks in Keras and Tensorflow 2.0¶

This is a keras implementation of hypernetworks, which are typically a pair of networks where one generates the parameters (weights) of the other (Ha, et al., 2016). Keras layer implementation exposes the parameters of a layer as two modifiable properties: ‘kernel’ and ‘bias’, which allows assiging them new values during inference.

This code will separate the hypernetwork into two keras models: an inference model which will perform the inference task (for e.g. classify handwritten digits), and a hyper model, which will generate the parameters of the inference model for each input example. We will demonstrate using a convolutional network as the inference model to classify MNIST digits.

The jupyter notebook can be opened in Google's Colab for a ready-made tensorflow-2 environment.

