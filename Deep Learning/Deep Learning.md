# Why Deep learning?:
	• Data growth
	• Hardware advancements
	• Python and open source ecosystem
    • Cloud and AI - easy availability 

# Neuron
	• A layer consists of small individual units called neurons. 
	• An artificial neuron is similar to a biological neuron. 
	• It receives input from the other neurons, performs some processing, and produces an output.
<a href="https://www.analyticsvidhya.com/blog/2021/03/basics-of-neural-network/">Blog</a>

# Neural Network

<p align="center"> 
	<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/nn.png" height=300/>
</p>

	• Consists of layers
	• Types :
		○ Input
		○ Output
		○ Hidden

# Backward error Propagation:
	• Feedback from supervisor to output to hidden to input layers

# Epoch
	• # of iteration on training sample
	• 1 Epoch = 1 iteration on all of the training samples


# Activation Function
	• Activation functions are important for an Artificial Neural Network to learn and understand the complex patterns. 
	• The main function of it is to introduce non-linear properties into the network.
	• What it does is, it calculates the ‘weighted sum’ and adds direction and decides whether to ‘fire’ a particular neuron or not. 
	• The nonlinear activation function will help the model to understand  the complexity and give accurate results.
	
## Types:
<table><tr>
	<td><img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/activation_funtions_step.PNG" /></td>
	<td>Step function<br>
		<ul>
			<li>Output is binary -> 0 or 1</li>
		</ul>
	</td>
	</tr>
	<tr>
		<td><img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/activation_function_sigmoid.png" /></td>
	<td>Sigmoid function<br>
		<ul>
			<li>Y = f(x)</li>
			<li>Sigmoid(z) = 1 / 1 + e-2, e = Euler's number, 2.718</li>
			<li>Converts to range 0 to 1</li>
			<li>Classification scenario</li>
			<li>Output is 0 < m < 1</li>
			<li><b>Has Vanishing gradient problem</b></li>
		</ul>
	</td>
	</tr>
	<tr>
		<td><img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/activation_function_tanh.png" /></td>
	<td>tanh<br>
		<ul>
			<li>Output is -1 < m < 1</li>
			<li><b>Also has vanishing gradient problem</b></li>
		</ul>
	</td>
	</tr>
	<tr>
		<td><img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/activation_funtions_relu.png" /></td>
		<td>ReLU
			<ul>
				<li>Preferred for hidden layer</li>
				<li>Lightweight</li>
				<li>Faster computation</li>
				<li>ReLU(z) = max(0,z)</li>
				<li><b>Also has vanishing gradient problem</b></li>
			</ul>
		</td>
	</tr>	
	<tr>
		<td><img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/activation_function_leaky_relu.png" /></td>
		<td>Leaky ReLU
			<ul>
				<li>max(0.1x , x)</li>
				<li>adds a small leak for - ve values (alpha) rather than making them 0. </li>
				<li>negative values are multiplied by small alpha and are not actually 0. </li>
				<li>Leaky relu is preferred when:</li>
				<ul>
					<li>There are lots of negative activations and relu stops learning process.</li>
					<li>If you don't want to carefully initialize weights, relu will get stuck if wrong combination of weights is used but leaky relu will slowly find convergence even on random initialized weights.</li>
				</ul>				
			</ul>
		</td>
	</tr>
</table>

# Soft max:

	- Normalizes the output
	- In sigmoid, the outputs of classes do not add to 1
	- Outputs of all classes add to 1
	- Ex: Class 1 = 0.4, Class 2 = 0.8
	- Softmax ouputs:
		Class 1 = 0.4 / (0.4 + 0.8) = 0.33
		Class 2 = 0.8 / (0.4 + 0.8) = o.67 

# Loss or cost function
	• Used in model training, where the idea is to minimize the loss / cost between actual and predicted
	• Individual errors are called loss and the overall aggregated error (like MAE) is called cost function
		○ Mean absolute error
		○ Mean squared error
		○ Log loss or binary cross entropy

<p align="center"> 
	<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/log_loss.png"/>
</p>			

# Difference b/w slope & derivative :
	• Slope is constant -> Linear
	• Derivative is not constant, is represented as a function-> non-linear

# Derivatives:
<p align="center"> 
	<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/derivatives.png" width=400 />
</p>

# Partial derivatives

<p align="center"> 
	<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/partial_derivatives.png" height=250 width=400 />
</p>


# Chain Rule:
	• The chain rule is essentially a mathematical formula that helps you calculate the derivative of a composite function


<p align="center"> 
	<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/chain_rule.png" height=400 width=800 />
</p>


# Tensorboard

# Dropout Regularizations
	• dropout regularization is used to randomly drop neurons from hidden layers and this helps with generalization.

# Vanishing Gradient & Exploding Gradient Problem :
Ref <a href="https://towardsdatascience.com/the-vanishing-gradient-problem-69bf08b15484">Article</a>

	- Common in RNN
	- Hence, LSTM and GRU

<p align="center"> 
	<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/vanished_gradient1.png" height=300/> 
</p>

## The problem:

	- With more layers & certain activation fns, the gradients of the loss function approaches zero, making the network hard to train.

<p align="center"> 
	<img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Deep%20Learning/images/vanished_gradient2.png" height=300/> 
</p>

## Why:

	- Activation functions, like sigmoid, squishes a large input space into a small input space between 0 and 1. 
	- Therefore, a large change in the input of the sigmoid function will cause a small change in the output. 
	- Hence, the derivative becomes small.

## Why it’s significant:

	- For shallow network with only a few layers that use these activations, this isn’t a big problem. 
	- However, when more layers are used, it can cause the gradient to be too small for training to work effectively.
	
	- Gradients of neural networks are found using backpropagation. 
	- Simply put, backpropagation finds the derivatives of the network by moving layer by layer from the final layer to the initial one 
	- By the chain rule, the derivatives of each layer are multiplied down the network (from final to initial) to compute the derivatives of the initial layers
  
	- However, when n hidden layers use an activation like the sigmoid function, n small derivatives are multiplied together. 
    	- Thus, the gradient decreases exponentially as we propagate down to the initial layers.
	- A small gradient means that the weights and biases of the initial layers will not be updated effectively with each training session. 
    	- Since these initial layers are often crucial to recognizing the core elements of the input data, it can lead to overall inaccuracy of the whole network.

## Solution:
	- ReLU
	- Residual networks
	- Batch normalization

# Interview Questions:

    • Build a simple NN class with mimicking a dense layer with sigmoid activation function
	• Note : Training is not affected by metrics param but only by loss function. Metrics just acts as additional info.

				
