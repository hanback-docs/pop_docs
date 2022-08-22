<h1> Pop.AI </h1>
Pop.AI is easy and fast educational Library for artificial intelligence. This Library supports Linear Regression, Logistic Regression, Perceptron, Artificial Neural Network(ANN), Deep Neural Network(DNN), Convolutional Neural Network(CNN) and Deep Q-Network(DQN).
<br>

<!-- # Class & Method Description-->
<hr/>

## <span class="title">Class</span> <span class="title_accent">**Linear_Regression**</span>    

<blockquote class="desc">A simple Linear Regression class for one to one datasets.</blockquote>

The code to import the Linear_Regression Class :

``` python
from pop.AI import Linear_Regression
```

<h5>&emsp;Initialization</h5>

&emsp;<code class="code_accent">Linear_Regression(restore=False, ckpt_name="linear_regression_models")</code> : Linear Regression Object<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`restore` : Load the recently trained model.   
&emsp;&emsp;&emsp;`ckpt_name` : Custom model name for saving and loading.

<h5>&emsp;Variables</h5>  

&emsp;<code class="code_accent">X_data</code> : Input data for training and prediction. It must be a 1-Dimensional Array. (ex, [0, 1, 2, 3])    
&emsp;<code class="code_accent">Y_data</code> : Result data for training and prediction. It must be a 1-Dimensional Array. (ex, [0, 2, 4, 6])     

<h5>&emsp;Methods</h5>

&emsp;<code class="code_accent">train(times=100, print_every=10)</code> : Train datasets as Linear Regression.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`times` : Number of training. ( = Epochs )   
&emsp;&emsp;&emsp;`print_every` : Training status printing cycle.  

&emsp;<code class="code_accent">run(inputs=X_data)</code> : Predict as trained Linear Regression.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`inputs` : Data to predict.   

&emsp;<code class="code_accent">save(path=ckpt_name)</code> : Save current model of this object.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to save. 

&emsp;<code class="code_accent">load(path=ckpt_name)</code> : Load a model in path.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to load. 

---

## <span class="title">Class</span> <span class="title_accent">**Logistic_Regression**</span>    

<blockquote class="desc">A simple Logistic Regression class for many to one datasets.</blockquote>

The code to import the Logistic_Regression Class :

``` python
from pop.AI import Logistic_Regression
```

<h5>&emsp;Initialization</h5>

&emsp;<code class="code_accent">Logistic_Regression(input_size=1, restore=False, ckpt_name="logistic_regression_models")</code> : Logistic Regression Object<br>
&emsp;&emsp;**Params**  
&emsp;&emsp;&emsp;`input_size` : Size of one dataset input.   
&emsp;&emsp;&emsp;`restore` : Load the recently trained model.   
&emsp;&emsp;&emsp;`ckpt_name` : Custom model name for saving and loading.

<h5>&emsp;Variables</h5>  

&emsp;<code class="code_accent">X_data</code> : Input data for training and prediction. It must be a 2-Dimensional Array. (ex, [[0, 1], [3, 2]])      
&emsp;<code class="code_accent">Y_data</code> : Result data for training and prediction. It must be a 2-Dimensional Array. (ex, [[0], [1]])       

<h5>&emsp;Methods</h5>

&emsp;<code class="code_accent">train(times=100, print_every=10)</code> : Train datasets as Logistic Regression.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`times` : Number of training. ( = Epochs )   
&emsp;&emsp;&emsp;`print_every` : Training status printing cycle.  

&emsp;<code class="code_accent">run(inputs=X_data)</code> : Predict as trained Logistic Regression.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`inputs` : Data to predict.   

&emsp;<code class="code_accent">save(path=ckpt_name)</code> : Save current model of this object.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to save. 

&emsp;<code class="code_accent">load(path=ckpt_name)</code> : Load a model in path.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to load. 

---

## <span class="title">Class</span> <span class="title_accent">**Perceptron**</span>    

<blockquote class="desc">A simple Perceptron class for many to many datasets.</blockquote>

The code to import the Perceptron Class :

``` python
from pop.AI import Perceptron
```

<h5>&emsp;Initialization</h5>

&emsp;<code class="code_accent">Perceptron(input_size, output_size=1, restore=False, ckpt_name="perceptron_models", softmax=True)</code> : Perceptron Object<br>
&emsp;&emsp;**Params**  
&emsp;&emsp;&emsp;`input_size` : Size of one dataset input.   
&emsp;&emsp;&emsp;`output_size` : Size of one dataset output.  
&emsp;&emsp;&emsp;`restore` : Load the recently trained model.   
&emsp;&emsp;&emsp;`ckpt_name` : Custom model name for saving and loading.   
&emsp;&emsp;&emsp;`softmax` : Process output as Softmax Function. However, process as Sigmoid Function if output size is 1.   

<h5>&emsp;Variables</h5>  

&emsp;<code class="code_accent">X_data</code> : Input data for training and prediction. It must be a 2-Dimensional Array. (ex, [[0, 1], [3, 2]])      
&emsp;<code class="code_accent">Y_data</code> : Result data for training and prediction. It must be a 2-Dimensional Array. (ex, [[0], [1]])       

<h5>&emsp;Methods</h5>

&emsp;<code class="code_accent">train(times=100, print_every=10)</code> : Train datasets as Logistic Regression.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`times` : Number of training. ( = Epochs )   
&emsp;&emsp;&emsp;`print_every` : Training status printing cycle.  

&emsp;<code class="code_accent">run(inputs=X_data)</code> : Predict as trained Logistic Regression.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`inputs` : Data to predict.   

&emsp;<code class="code_accent">save(path=ckpt_name)</code> : Save current model of this object.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to save. 

&emsp;<code class="code_accent">load(path=ckpt_name)</code> : Load a model in path.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to load. 

---

## <span class="title">Class</span> <span class="title_accent">**ANN**</span>    

<blockquote class="desc">A simple Artifitial Neural Network class for many to many datasets.</blockquote>

The code to import the ANN Class :

``` python
from pop.AI import ANN
```

<h5>&emsp;Initialization</h5>

&emsp;<code class="code_accent">ANN(input_size, hidden_size=10, output_size=1, restore=False, ckpt_name="ANN_models", softmax=True)</code> : Artifitial Neural Network Object<br>
&emsp;&emsp;**Params**  
&emsp;&emsp;&emsp;`input_size` : Size of one dataset input.   
&emsp;&emsp;&emsp;`hidden_size` : Size of hidden layer.   
&emsp;&emsp;&emsp;`output_size` : Size of one dataset output.  
&emsp;&emsp;&emsp;`restore` : Load the recently trained model.   
&emsp;&emsp;&emsp;`ckpt_name` : Custom model name for saving and loading.   
&emsp;&emsp;&emsp;`softmax` : Process output as Softmax Function. However, process as Sigmoid Function if output size is 1.   

<h5>&emsp;Variables</h5>  

&emsp;<code class="code_accent">X_data</code> : Input data for training and prediction. It must be a 2-Dimensional Array. (ex, [[0, 1], [3, 2]])      
&emsp;<code class="code_accent">Y_data</code> : Result data for training and prediction. It must be a 2-Dimensional Array. (ex, [[0], [1]])       

<h5>&emsp;Methods</h5>

&emsp;<code class="code_accent">train(times=100, print_every=10)</code> : Train datasets as Logistic Regression.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`times` : Number of training. ( = Epochs )   
&emsp;&emsp;&emsp;`print_every` : Training status printing cycle.  

&emsp;<code class="code_accent">run(inputs=X_data)</code> : Predict as trained Logistic Regression.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`inputs` : Data to predict.   

&emsp;<code class="code_accent">save(path=ckpt_name)</code> : Save current model of this object.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to save. 

&emsp;<code class="code_accent">load(path=ckpt_name)</code> : Load a model in path.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to load. 

---

## <span class="title">Class</span> <span class="title_accent">**DNN**</span>    

<blockquote class="desc">A simple Deep Neural Network class for many to many datasets.</blockquote>

The code to import the DNN Class :

``` python
from pop.AI import DNN
```

<h5>&emsp;Initialization</h5>

&emsp;<code class="code_accent">ANN(input_size, hidden_size=10, output_size=1, layer_level=3, restore=False, ckpt_name="DNN_models", softmax=True)</code> : Deep Neural Network Object<br>
&emsp;&emsp;**Params**  
&emsp;&emsp;&emsp;`input_size` : Size of one dataset input.   
&emsp;&emsp;&emsp;`hidden_size` : Size of hidden layer.   
&emsp;&emsp;&emsp;`output_size` : Size of one dataset output.  
&emsp;&emsp;&emsp;`layer_level` : Number of hidden layer. (Depth of layer)  
&emsp;&emsp;&emsp;`restore` : Load the recently trained model.   
&emsp;&emsp;&emsp;`ckpt_name` : Custom model name for saving and loading.   
&emsp;&emsp;&emsp;`softmax` : Process output as Softmax Function. However, process as Sigmoid Function if output size is 1.   

<h5>&emsp;Variables</h5>  

&emsp;<code class="code_accent">X_data</code> : Input data for training and prediction. It must be a 2-Dimensional Array. (ex, [[0, 1], [3, 2]])      
&emsp;<code class="code_accent">Y_data</code> : Result data for training and prediction. It must be a 2-Dimensional Array. (ex, [[0], [1]])       

<h5>&emsp;Methods</h5>

&emsp;<code class="code_accent">train(times=100, print_every=10)</code> : Train datasets as Logistic Regression.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`times` : Number of training. ( = Epochs )   
&emsp;&emsp;&emsp;`print_every` : Training status printing cycle.  

&emsp;<code class="code_accent">run(inputs=X_data)</code> : Predict as trained Logistic Regression.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`inputs` : Data to predict.   

&emsp;<code class="code_accent">save(path=ckpt_name)</code> : Save current model of this object.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to save. 

&emsp;<code class="code_accent">load(path=ckpt_name)</code> : Load a model in path.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to load. 

---

## <span class="title">Class</span> <span class="title_accent">**CNN**</span>    

<blockquote class="desc">A simple Convolutional Neural Network class for many to many datasets.</blockquote>

The code to import the CNN Class :

``` python
from pop.AI import CNN
```

<h5>&emsp;Initialization</h5>

&emsp;<code class="code_accent">CNN(input_size=[28,28], input_level=1, kernel_size=[3,3], kernel_count=32, strides=[1,1], hidden_size=128, output_size=1, conv_level=2, layer_level=1, restore=False, ckpt_name="CNN_models", softmax=True)</code> : Convolutional Neural Network Object<br>
&emsp;&emsp;**Params**  
&emsp;&emsp;&emsp;`input_size` : Size of one dataset input.   
&emsp;&emsp;&emsp;`input_level` : Color. (RGB: 3, BW: 1)  
&emsp;&emsp;&emsp;`kernel_size` : Size of kernel.  
&emsp;&emsp;&emsp;`kernel_count` : Number of kernels.  
&emsp;&emsp;&emsp;`strides`: Value of strides.     
&emsp;&emsp;&emsp;`hidden_size` : Size of hidden layer.   
&emsp;&emsp;&emsp;`output_size` : Size of one dataset output.  
&emsp;&emsp;&emsp;`conv_level` : Number of convolutional layers.  
&emsp;&emsp;&emsp;`layer_level` : Number of hidden layers. (Depth of layer)  
&emsp;&emsp;&emsp;`restore` : Load the recently trained model.   
&emsp;&emsp;&emsp;`ckpt_name` : Custom model name for saving and loading.   
&emsp;&emsp;&emsp;`softmax` : Process output as Softmax Function. However, process as Sigmoid Function if output size is 1.   

<h5>&emsp;Variables</h5>  

&emsp;<code class="code_accent">X_data</code> : Input data for training and prediction. It must be a 2-Dimensional Array. (ex, [[0, 1], [3, 2]])      
&emsp;<code class="code_accent">Y_data</code> : Result data for training and prediction. It must be a 2-Dimensional Array. (ex, [[0], [1]])       

<h5>&emsp;Methods</h5>

&emsp;<code class="code_accent">train(times=100, print_every=10)</code> : Train datasets as Logistic Regression.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`times` : Number of training. ( = Epochs )   
&emsp;&emsp;&emsp;`print_every` : Training status printing cycle.  

&emsp;<code class="code_accent">run(inputs=X_data)</code> : Predict as trained Logistic Regression.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`inputs` : Data to predict.   

&emsp;<code class="code_accent">load_MNIST()</code> : Load dataset of MNIST and input them into X_data, Y_data.  

&emsp;<code class="code_accent">show_img(input)</code> : Show an image.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`input` : Image data to show. It must be a 3-Dimensional Array. 

--- 

## <span class="title">Class</span> <span class="title_accent">**DQN**</span>    

<blockquote class="desc">A simple Deep Q-Network class.</blockquote>

The code to import the DQN Class :

``` python
from pop.AI import DQN
```

<h5>&emsp;Initialization</h5>

&emsp;<code class="code_accent">DQN(state_size, hidden_size=5, output_size=1, layer_level=1, restore=False, ckpt_name="DQN_models")</code> : Deep Q-Network Object<br>
&emsp;&emsp;**Params**  
&emsp;&emsp;&emsp;`state_size` : Size of state data. Input the size of the lowest dimension.   
&emsp;&emsp;&emsp;`hidden_size` : Size of hidden layer.   
&emsp;&emsp;&emsp;`output_size` : Size of one dataset output. Input the size of the lowest dimension.  
&emsp;&emsp;&emsp;`layer_level` : Number of hidden layer. (Depth of layer)  
&emsp;&emsp;&emsp;`restore` : Load the recently trained model.   
&emsp;&emsp;&emsp;`ckpt_name` : Custom model name for saving and loading.  

<h5>&emsp;Methods</h5>

&emsp;<code class="code_accent">train(states, rewards, actions)</code> : Adjust the agent's weight.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`states` : Current state.  
&emsp;&emsp;&emsp;`rewards` : Rewards for action.  
&emsp;&emsp;&emsp;`actions` : Options that the agent can take.  

&emsp;<code class="code_accent">run(inputs=None)</code> : Predict the agent's behavior with current state.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`inputs` : Current states.   

---

## <span class="title">Class</span> <span class="title_accent">**Face_Detection**</span>    

<blockquote class="desc">Class for experiencing face recognition models.</blockquote>

The code to import the Face_Detection Class :

``` python
from pop.AI import Face_Detection
```

<h5>&emsp;Initialization</h5>

&emsp;<code class="code_accent">Face_Detection(camera=None, resolution_type=1)</code> : Face Detection Object<br>
&emsp;&emsp;**Params**  
&emsp;&emsp;&emsp;`camera` : Camera object.   
&emsp;&emsp;&emsp;`resolution_type` : Resolution of the image.    

<h5>&emsp;Methods</h5>

&emsp;<code class="code_accent">get_faces(value=None, show=True)</code> : Find the location of the face.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : Input the array or name of the image file. When value is None, the camera image is used.   
&emsp;&emsp;&emsp;`show` : Whether or not to express results in graphic.  

&emsp;<code class="code_accent">get_feautres(value=None, show=True)</code> : Find a total of 68 landmarks along eyes, nose, mouth, eyebrows, and face shape and characterize someone.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : Input the array or name of the image file. When value is None, the camera image is used.   
&emsp;&emsp;&emsp;`show` : Whether or not to express results in graphic.  

&emsp;<code class="code_accent">show()</code> : Show an image.  

&emsp;<code class="code_accent">set_source(value=None)</code> : Set Reference Image.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : Input the array or name of the image file to be the reference. When value is None, the camera image is used. 

&emsp;<code class="code_accent">compare_face(value=None, src=None, threshold=0.5, show=True)</code> : Show an image.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : Input the array or name of the image file. When value is None, the camera image is used.  
&emsp;&emsp;&emsp;`src` : Input the array or name of the image file to be the reference. When value is None, the camera image is used.  
&emsp;&emsp;&emsp;`threshold` : Value to determine whether the person is the same or different.  
&emsp;&emsp;&emsp;`show` : Whether or not to express results in graphic.  

&emsp;<code class="code_accent">register_face(value, name, show=False)</code> : Register a face on the list.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : Input the array or name of the image file. When value is None, the camera image is used.  
&emsp;&emsp;&emsp;`name` : Name of face.  
&emsp;&emsp;&emsp;`show` : Whether or not to express results in graphic.  

&emsp;<code class="code_accent">list_faces()</code> : Names of faces registered on the list.   

&emsp;<code class="code_accent">drop_face(name)</code> : Delete the face on the list.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`name` : Name of face to delete. 

&emsp;<code class="code_accent">search(value=None, threshold=0.5, show=True)</code> : Show an image.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : Input the array or name of the image file. When value is None, the camera image is used.  
&emsp;&emsp;&emsp;`threshold` : Value to determine whether the person is the same or different.  
&emsp;&emsp;&emsp;`show` : Whether or not to express results in graphic.  

---

## <span class="title">Class</span> <span class="title_accent">**Object_Detect**</span>    

<blockquote class="desc">Class for experiencing object detection models.</blockquote>

The code to import the Object_Detect Class :

``` python
from pop.AI import Object_Detect
```

<h5>&emsp;Initialization</h5>

&emsp;<code class="code_accent">Object_Detect(camera=None)</code> : Object Detection Object<br>
&emsp;&emsp;**Params**  
&emsp;&emsp;&emsp;`camera` : Camera object.   

<h5>&emsp;Methods</h5>

&emsp;<code class="code_accent">show()</code> : The camera screen and model prediction values are displayed on the screen.  

&emsp;<code class="code_accent">load_model()</code> : Load the saved model.   

&emsp;<code class="code_accent">detect(image=None, index=None, threshold=0.5, show=True)</code> : Show an image.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`image` : Input the array or name of the image file. When value is None, the camera image is used.  
&emsp;&emsp;&emsp;`index` : Index of recognizable list used by YOLOv4-tiny model.  
&emsp;&emsp;&emsp;`threshold` : Value that determines which index the detected object corresponds to.  
&emsp;&emsp;&emsp;`show` : Whether or not to express results in graphic.  

---
