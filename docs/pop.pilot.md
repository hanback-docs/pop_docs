<h1> Pop.Pilot </h1>
Pop.Pilot is an easy and fast training library for robot control. 
This library can control the front wheels of two and four wheel drive vehicles with steering control. 
In addition, it provides functions such as object tracking and collision avoidance using a camera.
<br>

<!-- # Class & Method Description-->
<hr/>

## <span class="title">Class</span> <span class="title_accent">**AutoCar**</span>    

<blockquote class="desc">Class for easy control of AIoT AutoCar.</blockquote>

The code to import the AutoCar Class :

``` python
from pop.Pilot import AutoCar
```

<h5>&emsp;Initialization</h5>

&emsp;<code class="code_accent">AutoCar(bus=0)</code> : AutoCar Object<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`bus` : I2c bus number to control AutoCar's motors and sensors.   

<h5>&emsp;Variables</h5>  

&emsp;<code class="code_accent">steering</code> : Steer the front wheel of the AutoCar left or right. Specify a value between -1 and 1.    

<h5>&emsp;Methods</h5>

&emsp;<code class="code_accent">setSpeed(speed)</code> : Control AutoCar speed.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`speed` : Specify a value between 0 and 99.   

&emsp;<code class="code_accent">stop()</code> : Stop AutoCar.   

&emsp;<code class="code_accent">forward()</code> : Let the AutoCar move forward.   

&emsp;<code class="code_accent">backward()</code> : Let the AutoCar move backward.   

&emsp;<code class="code_accent">joystick()</code> : The AutoCar is controlled using a virtual joystick.   

&emsp;<code class="code_accent">camPan(value)</code> : Control the camera mounted on the AutoCar from side to side.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : Specify a value between 0 and 180.   

&emsp;<code class="code_accent">camTilt(value)</code> : Control the camera mounted on the AutoCar up or down.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : Specify a value between -30 and 200.   

&emsp;<code class="code_accent">getAccel(axis=None)</code> : Return the accel value through the sensor mounted on the AutoCar.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`axis` : Enter'x' or'y' or'z' to return the accel value of the axis. Return all if there is no input.   

&emsp;<code class="code_accent">getGyro(axis=None)</code> : Return the gyro value through the sensor mounted on the AutoCar.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`axis` : Enter'x' or'y' or'z' to return the gyro value of the axis. Return all if there is no input.   

---

## <span class="title">Class</span> <span class="title_accent">**DataCollector**</span>    

<blockquote class="desc">Image data collection class for machine learning.</blockquote>

The code to import the DataCollector Class :

``` python
from pop.Pilot import DataCollector
```

<h5>&emsp;Initialization</h5>

&emsp;<code class="code_accent">DataColletor(separator, camera=None, auto_ready=True, save_per_sec=5)</code> : DataCollector Object<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`seperator` : Enter the purpose of data collection. 'Collision_Avoid' or 'Track_Follow'   
&emsp;&emsp;&emsp;`camera` : Camera class to utilize camera images.   
&emsp;&emsp;&emsp;`auto_ready` : .   
&emsp;&emsp;&emsp;`save_per_sec` : Amount of data stored per second .   

<h5>&emsp;Methods</h5>

&emsp;<code class="code_accent">show()</code> : GUI display for data collection.   

&emsp;<code class="code_accent">ready()</code> : .   

&emsp;<code class="code_accent">save_as_joystick(value)</code> : Save the image using the joystick. Only use for Track Follow.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : .   

&emsp;<code class="code_accent">control_as_joystick(value)</code> : Use the joystick to control the robot. Only use for Collision Avoid.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : .   

&emsp;<code class="code_accent">save_blocked()</code> : Save the block image file in the specified path. Only use for Collision Avoid. default save path "./collision_dataset/blocked".  

&emsp;<code class="code_accent">save_free()</code> : Save the free image file in the specified path. Only use for Collision Avoid. default save path "./collision_dataset/free".   

&emsp;<code class="code_accent">save_snapshot(directory)</code> : Save the image file in the specified path. Only use for Collision Avoid.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`directory` : Path to save image file.   

---

## <span class="title">Class</span> <span class="title_accent">**Collision_Avoid**</span>    

<blockquote class="desc">The Collision_Avoid is a convolutional neural network class for obstacle recognition.</blockquote>

The code to import the Collision_Avoid Class :

``` python
from pop.Pilot import Collision_Avoid
```

<h5>&emsp;Initialization</h5>

&emsp;<code class="code_accent">Collision_Avoid(camera=None)</code> : Collision_Avoid Object<br>
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
&emsp;&emsp;&emsp;`value` : .   
&emsp;&emsp;&emsp;`callback` : .   

---

## <span class="title">Class</span> <span class="title_accent">**Object_Follow**</span>    

<blockquote class="desc">The Object_Follow is a convolutional neural network class for optimal object recognition.</blockquote>

The code to import the Object_Follow Class :

``` python
from pop.Pilot import Object_Follow
```

<h5>&emsp;Initialization</h5>

&emsp;<code class="code_accent">Object_Follow(camera=None)</code> : Object_Follow Object<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`camera` : Camera class to utilize camera images.    

<h5>&emsp;Methods</h5>

&emsp;<code class="code_accent">load_model(path='ssd_mobilenet_v2_coco.engine')</code> : Load the saved model.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to model file.   

&emsp;<code class="code_accent">show()</code> : .   

&emsp;<code class="code_accent">detect(image=None, index=None, show=True, callback=None)</code> : .   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`image` : .   
&emsp;&emsp;&emsp;`index` : .   
&emsp;&emsp;&emsp;`show` : .   
&emsp;&emsp;&emsp;`callback` : .   

---

## <span class="title">Class</span> <span class="title_accent">**Track_Follow**</span>    

<blockquote class="desc">The Track_Follow is a neural network class designed with a convolutional neural network for track recognition.</blockquote>

The code to import the Track_Follow Class :

``` python
from pop.Pilot import Track_Follow
```

<h5>&emsp;Initialization</h5>

&emsp;<code class="code_accent">Track_Follow(camera=None)</code> : Track_Follow Object<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`camera` : Camera class to utilize camera images.    

<h5>&emsp;Methods</h5>

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
&emsp;&emsp;&emsp;`value` : .   
&emsp;&emsp;&emsp;`callback` : .   

&emsp;<code class="code_accent">load_model(path=MODEL_PATH)</code> : Load the saved model.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to model file.   

&emsp;<code class="code_accent">save_model(path=MODEL_PATH)</code> : Save the model.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`path` : Path to model file.   

---

## <span class="title">Class</span> <span class="title_accent">**SerBot**</span>    

<blockquote class="desc">Class for easy control of AIoT SerBot.</blockquote>

The code to import the SerBot Class :

``` python
from pop.Pilot import SerBot
```

<h5>&emsp;Initialization</h5>

&emsp;<code class="code_accent">SerBot(bus=1)</code> : SerBot Object<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`bus` : I2c bus number to control SerBot's motors and sensors.   

<h5>&emsp;Variables</h5>  

&emsp;<code class="code_accent">steering</code> : Steer the front wheel of the SerBot left or right. Specify a value between -1 and 1.    

<h5>&emsp;Methods</h5>

&emsp;<code class="code_accent">move(degree, speed)</code> : Serbot moves in the direction specified by degree.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`degree` : Specify the direction of movement.   
&emsp;&emsp;&emsp;`speed` : Specify a value between 0 and 99.   

&emsp;<code class="code_accent">setSpeed(speed)</code> : Control SerBot speed.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`speed` : Specify a value between 0 and 99.   

&emsp;<code class="code_accent">stop()</code> : Stop SerBot.   

&emsp;<code class="code_accent">forward()</code> : Let the SerBot move forward.   

&emsp;<code class="code_accent">backward()</code> : Let the SerBot move backward.   

&emsp;<code class="code_accent">joystick()</code> : The SerBot is controlled using a virtual joystick.   

&emsp;<code class="code_accent">getAccel(axis=None)</code> : Return the accel value through the sensor mounted on the SerBot.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`axis` : Enter'x' or'y' or'z' to return the accel value of the axis. Return all if there is no input.   

&emsp;<code class="code_accent">getGyro(axis=None)</code> : Return the gyro value through the sensor mounted on the SerBot.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`axis` : Enter'x' or'y' or'z' to return the gyro value of the axis. Return all if there is no input.   

---
