<h1> Pop.AI </h1>
Pop.AI is easy and fast educational Library for artificial intelligence.
This Library supports Linear Regression, Logistic Regression, Perceptron, Artificial Neural Network(ANN), Deep Neural Network(DNN), Convolutional Neural Network(CNN) and Deep Q-Network(DQN).
In addition, it provides functions such as object detection, collision avoidance, road following, face detection, pose estimation using a camera.
<br><br>

<!-- # Class & Method Description-->
<hr/>

## <span class="title">Class</span> <span class="title_accent">**Linear_Regression**</span>    

<blockquote class="desc">A simple Linear Regression class for one to one datasets.</blockquote>

<br>
The code to import the Linear_Regression Class :

``` python
from pop.AI import Linear_Regression
```

<h4><b>&emsp;Initialization</b></h4>

&emsp;<code class="code_accent">Linear_Regression(restore=False, ckpt_name="linear_regression_models")</code> : Linear Regression Object<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`restore` : Load the recently trained model.   
&emsp;&emsp;&emsp;`ckpt_name` : Custom model name for saving and loading.

<h4><b>&emsp;Variables</b></h4>   

&emsp;<code class="code_accent">X_data</code> : Input data for training and prediction. It must be a 1-Dimensional Array. (ex, [0, 1, 2, 3])    
&emsp;<code class="code_accent">Y_data</code> : Result data for training and prediction. It must be a 1-Dimensional Array. (ex, [0, 2, 4, 6])     

<h4><b>&emsp;Methods</b></h4>

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

<br>

---

## <span class="title">Class</span> <span class="title_accent">**Logistic_Regression**</span>    

<blockquote class="desc">A simple Logistic Regression class for many to one datasets. Inherited Linear_Regression class</blockquote>

<br>
The code to import the Logistic_Regression Class :

``` python
from pop.AI import Logistic_Regression
```

<h4><b>&emsp;Initialization</b></h4>

&emsp;<code class="code_accent">Logistic_Regression(input_size=1, restore=False, ckpt_name="logistic_regression_models")</code> : Logistic Regression Object<br>
&emsp;&emsp;**Params**  
&emsp;&emsp;&emsp;`input_size` : Size of one dataset input.   
&emsp;&emsp;&emsp;`restore` : Load the recently trained model.   
&emsp;&emsp;&emsp;`ckpt_name` : Custom model name for saving and loading.

<h4><b>&emsp;Methods</b></h4>

&emsp;<code class="code_accent">loss_function(y_true, y_pred)</code> : loss_function.    
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`y_true` : Ground truth.   
&emsp;&emsp;&emsp;`y_pred` : Prediction.

<br>

---

## <span class="title">Class</span> <span class="title_accent">**Perceptron**</span>    

<blockquote class="desc">A simple Perceptron class for many to many datasets.</blockquote>

<br>
The code to import the Perceptron Class :

``` python
from pop.AI import Perceptron
```

<h4><b>&emsp;Initialization</b></h4>

&emsp;<code class="code_accent">Perceptron(input_size, output_size=1, restore=False, ckpt_name="Perceptron_models", softmax=True, activation_function=None)</code> : Perceptron Object<br>
&emsp;&emsp;**Params**  
&emsp;&emsp;&emsp;`input_size` : Size of one dataset input.   
&emsp;&emsp;&emsp;`output_size` : Size of one dataset output.  
&emsp;&emsp;&emsp;`restore` : Load the recently trained model.   
&emsp;&emsp;&emsp;`ckpt_name` : Custom model name for saving and loading.   
&emsp;&emsp;&emsp;`softmax` : Process output as Softmax Function. However, process as Sigmoid Function if output size is 1.    
&emsp;&emsp;&emsp;`activation_function` : Activation function when 'softmax' parameter is False.

<h4><b>&emsp;Variables</b></h4>  

&emsp;<code class="code_accent">X_data</code> : Input data for training and prediction. It must be a 2-Dimensional Array. (ex, [[0, 1], [3, 2]])      
&emsp;<code class="code_accent">Y_data</code> : Result data for training and prediction. It must be a 2-Dimensional Array. (ex, [[0], [1]])       

<h4><b>&emsp;Methods</b></h4>

&emsp;<code class="code_accent">train(times=100, print_every=10)</code> : Train datasets as Logistic Regression.    
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`times` : Number of training. ( = Epochs )   
&emsp;&emsp;&emsp;`print_every` : Training status printing cycle.  

&emsp;<code class="code_accent">run(inputs=X_data)</code> : Predict as trained Logistic Regression.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`inputs` : Data to predict. 

&emsp;<code class="code_accent">save(path=ckpt_name)</code> : Save current model of this Object   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to save.

&emsp;<code class="code_accent">load(path=ckpt_name)</code> : Load a model in path.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to load.

<br>

---

## <span class="title">Class</span> <span class="title_accent">**ANN**</span>    

<blockquote class="desc">A simple Artifitial Neural Network class for many to many datasets. Inherited Perceptron</blockquote>

<br>
The code to import the ANN Class :

``` python
from pop.AI import ANN
```

<h4><b>&emsp;Initialization</b></h4>

&emsp;<code class="code_accent">ANN(input_size, hidden_size=10, output_size=1, restore=False, ckpt_name="ANN_models", softmax=True)</code> : Artifitial Neural Network Object<br>
&emsp;&emsp;**Params**  
&emsp;&emsp;&emsp;`input_size` : Size of one dataset input.   
&emsp;&emsp;&emsp;`hidden_size` : Size of hidden layer.   
&emsp;&emsp;&emsp;`output_size` : Size of one dataset output.  
&emsp;&emsp;&emsp;`restore` : Load the recently trained model.   
&emsp;&emsp;&emsp;`ckpt_name` : Custom model name for saving and loading.   
&emsp;&emsp;&emsp;`softmax` : Process output as Softmax Function. However, process as Sigmoid Function if output size is 1.   

<br>

---

## <span class="title">Class</span> <span class="title_accent">**DNN**</span>    

<blockquote class="desc">A simple Deep Neural Network class for many to many datasets. Inherited ANN</blockquote>

The code to import the DNN Class :

``` python
from pop.AI import DNN
```

<h4><b>&emsp;Initialization</b></h4>

&emsp;<code class="code_accent">ANN(input_size, hidden_size=10, output_size=1, layer_level=3, restore=False, ckpt_name="DNN_models", softmax=True)</code> : Deep Neural Network Object<br>
&emsp;&emsp;**Params**  
&emsp;&emsp;&emsp;`input_size` : Size of one dataset input.   
&emsp;&emsp;&emsp;`hidden_size` : Size of hidden layer.   
&emsp;&emsp;&emsp;`output_size` : Size of one dataset output.  
&emsp;&emsp;&emsp;`layer_level` : Number of hidden layer. (Depth of layer)  
&emsp;&emsp;&emsp;`restore` : Load the recently trained model.   
&emsp;&emsp;&emsp;`ckpt_name` : Custom model name for saving and loading.   
&emsp;&emsp;&emsp;`softmax` : Process output as Softmax Function. However, process as Sigmoid Function if output size is 1.   

<br>

---

## <span class="title">Class</span> <span class="title_accent">**CNN**</span>    

<blockquote class="desc">A simple Convolutional Neural Network class for many to many datasets. Inherited DNN</blockquote>

The code to import the CNN Class :

``` python
from pop.AI import CNN
```

<h4><b>&emsp;Initialization</b></h4>

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

<h4><b>&emsp;Variables</b></h4>  

&emsp;<code class="code_accent">X_data</code> : Input data for training and prediction. It must be a 2-Dimensional Array. (ex, [[0, 1], [3, 2]])      
&emsp;<code class="code_accent">Y_data</code> : Result data for training and prediction. It must be a 2-Dimensional Array. (ex, [[0], [1]])       

<h4><b>&emsp;Methods</b></h4>

&emsp;<code class="code_accent">train(times=100, batch=500, print_every=10)</code> : Train datasets as Logistic Regression.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`times` : Number of training. ( = Epochs )    
&emsp;&emsp;&emsp;`batch` : The number of consecutive elements of the dataset to combine in a single batch.   
&emsp;&emsp;&emsp;`print_every` : Training status printing cycle.  

&emsp;<code class="code_accent">run(inputs=X_data, show=True)</code> : Predict as trained Logistic Regression.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`inputs` : Data to predict.   
&emsp;&emsp;&emsp;`show` : Showing Image data.   

&emsp;<code class="code_accent">load_MNIST()</code> : Load dataset of MNIST and input them into X_data, Y_data.  

&emsp;<code class="code_accent">show_img(input)</code> : Show an image.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`input` : Image data to show. It must be a 3-Dimensional Array. 

<br>

--- 

## <span class="title">Class</span> <span class="title_accent">**RNN**</span>    

<blockquote class="desc">A simple Convolutional Neural Network class for many to many datasets. Inherited ANN</blockquote>

The code to import the RNN Class :

``` python
from pop.AI import RNN
```

<h4><b>&emsp;Initialization</b></h4>

&emsp;<code class="code_accent">RNN(input_size, hidden_size=64, output_size=1, layer_level=1, restore=False, ckpt_name="RNN_models", softmax=False)</code> : Convolutional Neural Network Object<br>
&emsp;&emsp;**Params**  
&emsp;&emsp;&emsp;`input_size` : Size of one dataset input.   
&emsp;&emsp;&emsp;`hidden_size` : Size of hidden layer.    
&emsp;&emsp;&emsp;`output_size` : Size of one dataset output.   
&emsp;&emsp;&emsp;`layer_level` : Number of hidden layers. (Depth of layer)     
&emsp;&emsp;&emsp;`restore` : Load the recently trained model.    
&emsp;&emsp;&emsp;`ckpt_name` : Custom model name for saving and loading.     
&emsp;&emsp;&emsp;`softmax` : Process output as Softmax Function. However, process as Sigmoid Function if output size is 1.         

<h4><b>&emsp;Methods</b></h4>

&emsp;<code class="code_accent">train(times=100, batch=500, print_every=10)</code> : Train datasets as Logistic Regression.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`times` : Number of training. ( = Epochs )   
&emsp;&emsp;&emsp;`batch` : The number of consecutive elements of the dataset to combine in a single batch.
&emsp;&emsp;&emsp;`print_every` : Training status printing cycle.  

&emsp;<code class="code_accent">run(inputs=None)</code> : Predict as trained Logistic Regression.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`inputs` : Data to predict   

<br>

--- 

## <span class="title">Class</span> <span class="title_accent">**DQN**</span>    

<blockquote class="desc">A simple Deep Q-Network class. Inherited DQN</blockquote>

<br>
The code to import the DQN Class :

``` python
from pop.AI import DQN
```

<h4><b>&emsp;Initialization</b></h4>

&emsp;<code class="code_accent">DQN(state_size, hidden_size=5, output_size=1, layer_level=1, restore=False, ckpt_name="DQN_models", softmax=True)</code> : Deep Q-Network Object<br>
&emsp;&emsp;**Params**  
&emsp;&emsp;&emsp;`state_size` : Size of state data. Input the size of the lowest dimension.   
&emsp;&emsp;&emsp;`hidden_size` : Size of hidden layer.   
&emsp;&emsp;&emsp;`output_size` : Size of one dataset output. Input the size of the lowest dimension.  
&emsp;&emsp;&emsp;`layer_level` : Number of hidden layer. (Depth of layer)  
&emsp;&emsp;&emsp;`restore` : Load the recently trained model.   
&emsp;&emsp;&emsp;`ckpt_name` : Custom model name for saving and loading.  
&emsp;&emsp;&emsp;`softmax` : Process output as Softmax Function.

<h4><b>&emsp;Methods</b></h4>

&emsp;<code class="code_accent">train(states, rewards, actions, times=1)</code> : Adjust the agent's weight.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`states` : Current state.  
&emsp;&emsp;&emsp;`rewards` : Rewards for action.  
&emsp;&emsp;&emsp;`actions` : Options that the agent can take.  
&emsp;&emsp;&emsp;`times` : Number of training. ( = Epochs )  

&emsp;<code class="code_accent">run(inputs, boolean=True)</code> : Predict the agent's behavior with current state.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`inputs` : Current states.   
&emsp;&emsp;&emsp;`boolean` : Type of return value.

<br>

---

## <span class="title">Class</span> <span class="title_accent">**FaceNet**</span>    

<blockquote class="desc">The FaceNet is a convolutional neural network class for face detection.<br>
This class is used in AIoT Home.</blockquote>

<br>
The code to import the FaceNet Class :

``` python
from pop.AI import FaceNet
```

<h4><b>&emsp;Initialization</b></h4>

&emsp;<code class="code_accent">FaceNet(path=MODEL_PATH)</code> : FaceNet Object<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`path` : Path to model file.    

<h4><b>&emsp;Methods</b></h4>

&emsp;<code class="code_accent">regist(label, data, cropped=True)</code> : Register the face.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`label` : Name to display when a face is detected.   
&emsp;&emsp;&emsp;`data` : Face image data.   
&emsp;&emsp;&emsp;`cropped` : Whether the face image is cropped. When this is False, find the face automatically and crop it.    

&emsp;<code class="code_accent">run(inputs, cropped=True)</code> : Compare a detected face with a registered face.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`inputs` : Data with face.   
&emsp;&emsp;&emsp;`cropped` : Whether the face image is cropped. When this is False, find the face automatically and crop it.   

<br>

--- 

## <span class="title">Class</span> <span class="title_accent">**Collision_Avoid**</span>    

<blockquote class="desc">The Collision_Avoid is a convolutional neural network class for obstacle recognition.<br>
This class can be used in AIoT AutoCAR Series, AIoT SerBot Series.<br>
In AIoT AutoCAR, AIoT AutoCAR Prime, AIoT SerBot, this class is in Pilot.</blockquote>

<br>
The code to import the Collision_Avoid Class :

``` python
from pop.AI import Collision_Avoid
```

<h4><b>&emsp;Initialization</b></h4>

&emsp;<code class="code_accent">Collision_Avoid(camera)</code> : Collision_Avoid Object<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`camera` : Camera class to utilize camera images.    

<h5>&emsp;Methods</h5>

&emsp;<code class="code_accent">load_datasets(path=dataset_path)</code> : Load the previously collected dataset.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`load_datasets` : Path of pre-collected dataset. default path "./collision_dataset"   

&emsp;<code class="code_accent">train(times=5, autosave=True)</code> : Train through the loaded dataset.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`time` : Learning count.   
&emsp;&emsp;&emsp;`autosave` : Whether to automatically save after learning.   

&emsp;<code class="code_accent">load_model(path=MODEL_PATH)</code> : Load the saved model.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to model file.   

&emsp;<code class="code_accent">save_model(path=MODEL_PATH)</code> : Save the model.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to model file.   

&emsp;<code class="code_accent">show()</code> : The camera screen and model prediction values are displayed on the screen.   

&emsp;<code class="code_accent">run(value=None, callback=None)</code> : Output the predicted value of the model.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : Direct image data to be recognized. Used to recognize data other than the camera image currently assigned to the class.   
&emsp;&emsp;&emsp;`callback` : Callback method to process by passing the result value. 

<br>

---

## <span class="title">Class</span> <span class="title_accent">**Object_Follow**</span>    

<blockquote class="desc">The Object_Follow is a convolutional neural network class for optimal object recognition.<br>
This class can be used in AIoT AutoCAR Series, AIoT SerBot Series.<br>
In AIoT AutoCAR, AIoT AutoCAR Prime, AIoT SerBot, this class is in Pilot.</blockquote>

<br>
The code to import the Object_Follow Class :

``` python
from pop.AI import Object_Follow
```

<h4><b>&emsp;Initialization</b></h4>

&emsp;<code class="code_accent">Object_Follow(camera, label_list=None)</code> : Object_Follow Object<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`camera` : Camera class to utilize camera images.    
&emsp;&emsp;&emsp;`label_list` : List of objects that can be detected. This parameter is used in AIoT AutoCAR 3.    

<h4><b>&emsp;Methods</b></h4>

&emsp;<code class="code_accent">load_model(path=MODEL_PATH)</code> : Load the saved model.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to model file.   

&emsp;<code class="code_accent">show()</code> : Whether the execution result is expressed as a graphic element.   

&emsp;<code class="code_accent">detect(image=None, index=None, threshold=0.3, show=True, callback=None)</code> : Recognize objects with the loaded model.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`image` : Direct image data to be recognized. Used to recognize data other than the camera image currently assigned to the class.   
&emsp;&emsp;&emsp;`index` : You can specify which objects are recognized. If you do not enter an index, results are returned for all recognizable objects.   
&emsp;&emsp;&emsp;`threshold` : Value that determines which index the detected object corresponds to.     
&emsp;&emsp;&emsp;`show` : Whether the execution result is expressed as a graphic element.   
&emsp;&emsp;&emsp;`callback` : Callback method to process by passing the result value.   

<br>

---

## <span class="title">Class</span> <span class="title_accent">**Track_Follow**</span>    

<blockquote class="desc">The Track_Follow is a neural network class designed with a convolutional neural network for track recognition.<br>
This class can be used in AIoT AutoCAR Series, AIoT SerBot Series.<br>
In AIoT AutoCAR, AIoT AutoCAR Prime, AIoT SerBot, this class is in Pilot.</blockquote>

<br>
The code to import the Track_Follow Class :

``` python
from pop.AI import Track_Follow
```

<h4><b>&emsp;Initialization</b></h4>

&emsp;<code class="code_accent">Track_Follow(camera)</code> : Track_Follow Object<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`camera` : Camera class to utilize camera images.    

<h4><b>&emsp;Methods</b></h4>

&emsp;<code class="code_accent">load_datasets(path=dataset_path)</code> : Load the previously collected dataset.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path of pre-collected dataset. default path "./track_dataset".   

&emsp;<code class="code_accent">train(time=5, autosave=True)</code> : Train through the loaded dataset.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`time` : Learning count.   
&emsp;&emsp;&emsp;`autosave` : Whether to automatically save after learning.   

&emsp;<code class="code_accent">show()</code> : The camera screen and model prediction values are displayed on the screen.   

&emsp;<code class="code_accent">run(value=None, callback=None)</code> : Output the predicted value of the model.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : Direct image data to be recognized. Used to recognize data other than the camera image currently assigned to the class.   
&emsp;&emsp;&emsp;`callback` : Callback method to process by passing the result value.   

&emsp;<code class="code_accent">load_model(path=MODEL_PATH)</code> : Load the saved model.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to model file.   

&emsp;<code class="code_accent">save_model(path=MODEL_PATH)</code> : Save the model.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to model file.   

<br>

---

## <span class="title">Class</span> <span class="title_accent">**Object_Detect**</span>    

<blockquote class="desc">Class for experiencing object detection models.<br>
This class is used in AI Mavin.</blockquote>

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

<br>

---

## <span class="title">Class</span> <span class="title_accent">**Pose_Estimation**</span>    

<blockquote class="desc">The Pose_Estimation is a convolutional neural network class for optimal pose estimation.<br>
This class is used in AIoT AutoCAR 2.</blockquote>

<br>
The code to import the Pose_Estimation Class :

``` python
from pop.AI import Pose_Estimation
```

<h4><b>&emsp;Initialization</b></h4>

&emsp;<code class="code_accent">Pose_Estimation(camera)</code> : Pose_Estimation Object<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`camera` : Camera object.      

<h4><b>&emsp;Methods</b></h4>

&emsp;<code class="code_accent">detect(value=None)</code> : Estimate pose with the loaded model.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : Direct image data to be recognized. Used to recognize data other than the camera image currently assigned to the class.   

&emsp;<code class="code_accent">show()</code> : Whether or not to express results in graphic.      

<br>
