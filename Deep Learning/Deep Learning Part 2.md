# Applications of Computer Vision

    • Image classification and object detection
    • Banking (ex Chequebook recognition)
    • Agriculture (ex: yield and price estimates)
    • Automonous cars 
    • Retail (Amazon Go stores)

# Convolutional Neural Network
Deep Learning algorithm which can take in an input image, assign importance (learnable weights and biases) to various aspects/objects in the image and be able to differentiate one from the other.

## Disadvantages of ANN for image classification

    - High computation
    - Treats local pixels same as pixels far apart
    - Sensitive to location of an object in an image


![](../2022-02-07-11-36-21.png)



## Filters

Filters:

	• Feature detectors
	•  Filters detect spatial patterns such as edges in an image by detecting the changes in intensity values of the image
	•  a high-frequency image is the one where the intensity of the pixels changes by a large amount, whereas a low-frequency image is the one where the intensity is almost uniform.
	•  Usually, an image has both high and low frequency components.
	•  The high-frequency components correspond to the edges of an object because at the edges the rate of change of intensity of pixel values is high.

Feature map:
	• The feature maps of a CNN capture the result of applying the filters to an input image. I.e. at each layer, the feature map is the output of that layer.

Stride:
	• Stride is the number of pixels shifts over the input matrix. 
	• When the stride is 1 then we move the filters to 1 pixel at a time. When the stride is 2 then we move the filters to 2 pixels at a time and so on.

Pooling layer:
	• another building block of a CNN. Pooling. 
	• Its function is to progressively reduce the spatial size of the representation to reduce the amount of parameters and computation in the network
	• operates on each feature map independently.
	• Benefits :
		○ Reduces dimensions & computations
		○ Reduce overfitting
		○ Model is tolerant to noise
	• Ex : Avg pooling, max pooling
		

Parameter sharing
	• sharing of weights by all neurons in a particular feature map.
	
Local connectivity 
	• the concept of each neural connected only to a subset of the input image (unlike a neural network where all the neurons are fully connected)
This helps to reduce the number of parameters in the whole system and makes the computation more efficient.

![](../2022-02-07-13-55-08.png)
