# Applications of Computer Vision

    • Image classification and object detection
    • Banking (ex Chequebook recognition)
    • Agriculture (ex: yield and price estimates)
    • Automonous cars 
    • Retail (Amazon Go stores)

# Convolutional Neural Network:
	
	Deep Learning algorithm which can 
		• take in an input image, 
		• assign importance (learnable weights and biases) to various aspects/objects in the image and 
		• be able to differentiate one from the other.

## Disadvantages of ANN for image classification

    - High computation
    - Treats local pixels same as pixels far apart
    - Sensitive to location of an object in an image


<p align="center"> 
	<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/koala_detection.png" height=300/> 
</p>


## Filters
	
	• Feature detectors
	• Filters detect spatial patterns such as edges in an image by detecting the changes in intensity values of the image
	• a high-frequency image is the one where the intensity of the pixels changes by a large amount, 
	• whereas a low-frequency image is the one where the intensity is almost uniform.
	• Usually, an image has both high and low frequency components.
	• high-frequency components correspond to edges of an object because at the edges the rate of change of intensity of pixel values is high.

## Feature map:

	• The feature maps of a CNN capture the result of applying the filters to an input image. 
	• I.e. at each layer, the feature map is the output of that layer.

<p align="center"> 
	<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/feature_map_formula.png" /> 
</p>

## Stride:

	• Stride is the number of pixels shifts over the input matrix. 
	• When the stride is 1 then we move the filters to 1 pixel at a time. 
	• When the stride is 2 then we move the filters to 2 pixels at a time and so on.

## Pooling layer:

	• another building block of a CNN. Pooling. 
	• function is to progressively reduce the spatial size of the representation to reduce the amount of parameters and computation
	• operates on each feature map independently.
	• Benefits :
		○ Reduces dimensions & computations
		○ Reduce overfitting
		○ Model is tolerant to noise
	• Ex : Avg pooling, max pooling
		

## Parameter sharing:

	• sharing of weights by all neurons in a particular feature map.
	
## Local connectivity:

	• concept of each neural connected only to a subset of the input image
	• (unlike a neural network where all the neurons are fully connected)
	• This helps to reduce the number of parameters in the whole system and makes the computation more efficient.


## Padding:

	• Why? Corner pixels don’t contribute much in feature detection

<table>
	<tr>
		<td>
			<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/padding_1.png" height="300" width="100%"/> 
		</td>
		<td>
			<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/padding_2.png" height="300" width="100%"/>
		</td>
	</tr>
</table>


### Difference b/w valid convolution and Same convolution:
	• In same convolution, the output / feature map shape is same as that of the original image

# Data Augmentation:
	• A CNN that can robustly classify objects even if its placed in different orientations is said to have the property called invariance. 
	• More specifically, a CNN can be invariant to translation, viewpoint, size or illumination
	• technique to artificially create new training data from existing training data. 
	• done by applying domain-specific techniques to examples from the training data that create new and different training examples.

# Transfer Learning

	• A research problem in ML 
	• that focuses on storing knowledge gained while solving one problem and applying it to a different but related problem
	• Ex: knowledge gained while learning to recognize cars could apply when trying to recognize trucks

<p align="center"> 
	<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/transfer_learning.png" height="300" width="70%"/> 
</p>

# Object Detection Models:

<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/object_detection_models.png" />

## YOLO:

	• You only look once
	• Anchor box
	• Divide the image into multiple windows, ex : 4 * 4

### Sliding Window (Annotations & Training):

<table>
	<tr>
		<td>
			<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/sliding_window_annot.png" height="300" width="100%"/> 
		</td>
		<td>
			<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/sliding_window_train.png" height="300" width="100%"/>
		</td>
	</tr>
</table>


### YOLO(Annotations & Training):

<table>
	<tr>
		<td>
			<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/yolo_annot.png" height="300" width="100%"/> 
		</td>
		<td>
			<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/yolo_train.png" height="300" width="100%"/>
		</td>
	</tr>
</table>
	
	• Intersection over Union:
	• Calculate IOU for a given class: (Non max Suppression)
		○ If IOU >  0, the boxes are overlapping, take the Bounding box with max class probability
		○ If IOU = 0, the boxes are not overlapping, keep both 

<p align="center"> 
	<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/yolo_ioc.png" /> 
</p>
		
	
### Multiple anchor boxes:
<p align="center"> 
	<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/yolo_multiple_anchors.png" height="300" width="60%" /> 
</p>

<a href"https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/Deep%20Learning%20Part%203.md">Continued...</a>