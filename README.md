# Deep Convolutional GAN

This is an implementation of the <a href="https://arxiv.org/abs/1511.06434">DCGAN</a> paper. 

* The training images have been scaled to a range of [-1, 1]. 
* The activation function used is LeakyRELU(for both the generator and discriminator) with 0.2 as the alpha(slope) value except for the last layer of the generator which uses **tanh** as the activation function.
* There are no Fully connected layers used.
* Instead of Max-pooling, strided convolutions are used in the discriminator.
* For the generator, Upsampling followed by a convolutional layer is used to increase the resolution of the image.
* The optimizer used is Adam.
* A batch size of 128 is used to the train the generator and the discriminator.


The image below has been obtained after training the model for **50 epochs**.

![image1](https://raw.githubusercontent.com/yashk2810/DCGAN-Keras/master/images/dcgan.png "image1")

# Requirements

* Keras
* Tensorflow
* Numpy
* Tqdm
* Matplotlib

# Usage

The DCGAN.ipynb notebook contains the entire code. To model weights for the generator and the discriminator are available in the model weights folder. The dataset used is the MNIST dataset. This dataset is provided by Keras, so there is no need to download it separately.


