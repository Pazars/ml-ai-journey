This is a summary and collection of definitions, concepts, models, and other interesting resources related to computer vision (but not directly to MNIST) that I stumbled upon while working on the MNIST task.

**ImageNet**: 

    - A [large visual database](https://www.image-net.org/index.php) designed for use in visual object recognition software research.
    - Popular model reference A. Krizhevsky et al. "Imagenet classification with deep convolutional neural networks" (2017)

**CIFAR**:

    - The CIFAR-10 and CIFAR-100 are labeled subsets of the 80 million tiny images dataset.
    - CIFAR-10 contains 10 and CIFAR-100 contains 100 labeled categories.
    - CIFAR stands or Canadian Institute or Advanced Research

**COCO**:

    - A large-scale object detection, segmentation, and captioning dataset.

**U-Net**:

    - A convolutional neural network that was developed for biomedical image segmentation at the Computer Science Department of the University of Freiburg.
    - It is a U-shaped encoder-decoder network architecture.
    - Image segmentation is the process of partitioning a digital image into multiple image segments.
    - Original paper Olaf Ronneberger et al. "U-Net: Convolutional Networks for Biomedical Image Segmentation" (2015)

**ResNet**

    - Deeper neural networks are more difficult to train (e.g. vanishing gradient problem).
    - Introduces residual learning and skip connections (haven't fully explored the principle yet).
    - Original paper by K. He et al. "Deep Residual Learning for Image Recognition" (2015) from Microsoft Research.
    - A ResNet50 implies that it is a ResNet architecture with 50 layers.

**JAX**:

    - [High-Performance Array Computing](https://jax.readthedocs.io/en/latest/) developed by Google.
    - Autograd and XLA (Accelerated Linear Algebra)


**Max pooling**

    - A limitation of the feature map output of convolutional layers is that they record the precise position of features in the input. This means that small movements in the position of the feature in the input image will result in a different feature map. This can happen with re-cropping, rotation, shifting, and other minor changes to the input image.A common approach to addressing this problem from signal processing is called down sampling. This is where a lower resolution version of an input signal is created that still contains the large or important structural elements, without the fine detail that may not be as useful to the task. Down sampling can be achieved with convolutional layers by changing the stride of the convolution across the image. A more robust and common approach is to use a pooling layer.
    - In all cases, pooling helps to make the representation become approximately invariant to small translations of the input. Invariance to translation means that if we translate the input by a small amount, the values of most of the pooled outputs do not change.
    - Many people dislike the pooling operation and think that we can get away without it. For example, J.T. Springenberg et al. propose in "Striving for Simplicity: The All Convolutional Net" to discard the pooling layer in favor of architecture that only consists of repeated CONV layers. **To reduce the size of the representation they suggest using larger stride in CONV layer once in a while**. Discarding pooling layers has also been found to be important in training good generative models, such as variational autoencoders (VAEs) or generative adversarial networks (GANs). It seems likely that future architectures will feature very few to no pooling layers.


**Convolution layer receptive field**

- Intuition behind how 2 3x3 convolution layers have the same receptive field as a single 5x5 convolution layer [StackExchange: Convolution layers without pooling](https://datascience.stackexchange.com/questions/64156/convolutional-layers-without-pooling).
- More mathematical explanation in [Stanford's CNN cheatsheet](https://stanford.edu/~shervine/teaching/cs-230/cheatsheet-convolutional-neural-networks#hyperparameters)
