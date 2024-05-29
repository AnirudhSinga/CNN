# CNN

##Normal dataset

Considered MNIST dataset, flattened 28x28 each image into a 784 dimensional vector. Next, Created a NN with 784 inputs are fully connected to 1000 neurons(i.e., hidden layer)
then those fully connected to 10 output identity neurons to classify ten 0-9 handwritten numbers. Cross Entropy loss function by default includes softmax in the code. Experimented with Sigmoid and Relu activation functions along with different optimizers i.e., SGD and Adam. Then plotted training losses, test losses, training accuracy and test accuracy over 50 epochs. Overall, observed that the performance of Adam is better compared to SGD optimizer. Specifically, the test accuracy falls in the range of about 96% - 97.5% for all 4 NN’s with Adam and 70% - 78% for 3 NN’s, but with the Sigmoid function, it’s about 50% with SGD).

For CNN, added additional convolution layer before flattening the image and considered specification as per the given problem. For Max pooling, added Max pool additional layer after convolution layer. Repeated the above mentioned steps.

The training and test accuracy of CNN is improved compared to other NN’s for both SGD and Adam combination. Even Convolution + max pooling classification accuracy is almost matching with CNN(i.e., around test accuracy = 98.5% with Adam optimizer). Plotted outputs of different layers as mentioned in the problem. As we compare the images, we can notice that the output of the convolution layer produced image size depends on the kernel size, stride and padding provided. For the 28 x 28 input size, the output size is 26 x 26(dimension reduction) which reduces computation burden later and if we apply max pooling layer it further reduces the size, i.e., 24 x 24, as per the provided specification. From the image comparisons, the insights we can draw are: Convolution layers help in learning meaningful patterns, hieracrchical features, local connectivity and takes advantage of spatial invariance.

Max pooling layers help in downsampling the CNN output and highlights most important features (we can observe the image is sort of zoomed compared to other two images while retaining features).

##Permuted dataset

Repeated all the above steps for permuted dataset by permuting the pixels in the image with the same seed value. Noticed that the performance of permuted dataset has remained
comparable to the normal dataset behavior. The classification test accuracy is around 97% with Adam optimizer for the normal neural network (NN), convolutional neural network
(CNN), and CNN + max pooling architectures. With the SGD optimizer, the test accuracy for the normal dataset was around 98%, while for the permuted dataset, it ranged from
72% to 78%. However, the combination using the Sigmoid activation function showed lower performance in both cases. The similarity in performance between the normal and permuted datasets with ReLu activation function indicates that the CNN model is robust and capable of generalizing well.

CNNs are robust to variations in input data due to their hierarchical feature learning and take advantage of spatial invariance by using weight sharing and convolution operations. Moreover, MNIST is a simple dataset compared to CIFAR-10 to train a Neural Network.
