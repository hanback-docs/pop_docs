<h1> Pop.Pilot </h1>
Pop.Pilot is an easy and fast training library for robot control.  
This library can control the front wheels of two and four wheel drive vehicles with steering control.   
This library is used in AIoT AutoCAR Series, AIoT SerBot Series.  
<br><br>

<!-- # Class & Method Description-->
<hr/>

## <span class="title">Class</span> <span class="title_accent">**Driving**</span>    
<br>

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">Driving()</code> : Driving object. and speed set 20.<br>
&emsp;&emsp;In AIoT AutoCar Prime X, AIoT AutoCAR 2, AIoT AutoCAR 3, AIoT SerBot Prime X, pop.CAN.Car() object also initialize when initialize.<br>

<h4><b>Methods</b></h4>   

&emsp;<code class="code_accent">setSpeed(speed)</code> : set speed.<br> 
&emsp;&emsp;**Params**      
&emsp;&emsp;&emsp;`speed` : Specify a value between 20 and 99.<br>  

&emsp;<code class="code_accent">getSpeed()</code> : return current speed.<br> 

&emsp;<code class="code_accent">stop()</code> : stop driving. wheel set 0.<br> 

&emsp;<code class="code_accent">direction(stat, speed)</code> : set speed and direction.<br> 
&emsp;&emsp;**Params**      
&emsp;&emsp;&emsp;`stat` : driving direction. Driving.STAT_BACKWARD or Driving.STAT_FORWARD.<br> 
&emsp;&emsp;&emsp;`speed` : Specify a value between 20 and 99.<br> 

<h4><b>Example</b></h4> 

<details>
	<summary>simple example</summary>

~~~python
from pop.Pilot import Driving
import time 

drv = Driving()
drv.direction(drv.STAT_FORWARD, 50)
time.sleep(5)
drv.setSpeed(30)
time.sleep(5)
drv.stop()
~~~

</details>

<br>

---

## <span class="title">Class</span> <span class="title_accent">**AutoCar**</span>    

<blockquote class="desc">Class for easy control of AIoT AutoCar Series.</blockquote>

The code to import the Autocar Class :

``` python
from pop.Pilot import Autocar
```

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">AutoCar()</code> : AutoCar object. <br>
&emsp;&emsp;when AIoT AutoCAR Prime X initialize, pop.CAN.Car() object also initialize.<br>
&emsp;&emsp;when AIoT AutoCAR 2 and AIoT AutoCAR 3 initialize, pop.CAN.Car() object also initialize and set ultrasonic & axis9 sensors.<br>

<h4><b>Methods</b></h4>   

&emsp;<code class="code_accent">steering(value)</code> : set wheel angle<br> 
&emsp;&emsp;**Params**      
&emsp;&emsp;&emsp;`value` : set wheel as value. range -1~+1. 0 is center. -1 is left. +1 is right.<br> 

&emsp;<code class="code_accent">turnLeft()</code> : set wheel turn left<br> 

&emsp;<code class="code_accent">turnRight()</code> : set wheel turn right<br> 

&emsp;<code class="code_accent">turnCenter()</code> : set wheel turn center<br> 

&emsp;<code class="code_accent">setSpeed(speed)</code> : set speed<br> 
&emsp;&emsp;**Params**      
&emsp;&emsp;&emsp;`speed` : Specify a value between 20 and 99<br>  

&emsp;<code class="code_accent">getSpeed()</code> : return current speed<br> 

&emsp;<code class="code_accent">stop()</code> : stop driving<br> 

&emsp;<code class="code_accent">forward(speed=None)</code> : set dc motor direction to forward and set speed<br> 
&emsp;&emsp;**Params**      
&emsp;&emsp;&emsp;`speed` : Specify a value between 20 and 99. if do not set speed value, only set dc motor direction<br> 

&emsp;<code class="code_accent">backward(speed=None)</code> : set dc motor direction to backward and set speed<br> 
&emsp;&emsp;**Params**      
&emsp;&emsp;&emsp;`speed` : Specify a value between 20 and 99. if do not set speed value, only set dc motor direction<br>

&emsp;<code class="code_accent">camPan(value)</code> : set pan angle<br> 
&emsp;&emsp;This method is used in AIoT AutoCAR, AIoT AutoCAR Prime, AIoT AutoCAR Prime X, AIoT AutoCAR 2.    
&emsp;&emsp;**Params**      
&emsp;&emsp;&emsp;`value` : Pan angle<br>

&emsp;<code class="code_accent">camTilt(value)</code> : set tilt angle<br> 
&emsp;&emsp;This method is used in AIoT AutoCAR, AIoT AutoCAR Prime, AIoT AutoCAR Prime X, AIoT AutoCAR 2.   
&emsp;&emsp;**Params**      
&emsp;&emsp;&emsp;`value` : Tilt angle<br>

&emsp;<code class="code_accent">joystick()</code> : display joystick<br> 

&emsp;<code class="code_accent">alarm(scale, pitch, duration=0)</code> : control buzzer<br> 
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.   
&emsp;&emsp;**Params**      
&emsp;&emsp;&emsp;`scale` : set scale<br>
&emsp;&emsp;&emsp;`pitch` : set pitch<br>
&emsp;&emsp;&emsp;`duration` : set duration<br>

&emsp;<code class="code_accent">setSensorStatus(ultrasonic=1, axis9=1, euler=0, gravity=0, battery=0, cds=0)</code> : set sensor data receive<br> 
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.   
&emsp;&emsp;**Params**      
&emsp;&emsp;&emsp;`ultrasonic` : set ultrasonic sensor on(1)/off(0)<br>
&emsp;&emsp;&emsp;`axis9` : set axis9 sensor on(1)/off(0)<br>
&emsp;&emsp;&emsp;`euler` : set euler sensor on(1)/off(0)<br>
&emsp;&emsp;&emsp;`gravity` : set gravity sensor on(1)/off(0)<br>
&emsp;&emsp;&emsp;`battery` : set battery value on(1)/off(0)<br>
&emsp;&emsp;&emsp;`cds` : set cds sensor on(1)/off(0)<br>

&emsp;<code class="code_accent">setObstacleDistance(distance=20)</code> : set obstacle distance<br> 
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.   
&emsp;&emsp;**Params**      
&emsp;&emsp;&emsp;`distance` : set obstacle distance. 20 < range <= 180. if distance set below 20, obstacle distance function disable.<br>

&emsp;<code class="code_accent">setLamp(front=0, rear=0)</code> : set lamp on/off<br> 
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.   
&emsp;&emsp;**Params**      
&emsp;&emsp;&emsp;`front` : front lamp on(1)/off(0)<br>
&emsp;&emsp;&emsp;`rear` : rear lamp on(1)/off(0)<br>

&emsp;<code class="code_accent">setPixelDisplay(num, red, green=0, blue=0)</code> : set PixelDisplay<br> 
&emsp;&emsp;This method is used in AIoT AutoCAR 2.   
&emsp;&emsp;**Params**      
&emsp;&emsp;&emsp;`num` : pixel display number. 0~255<br>
&emsp;&emsp;&emsp;`red` : red value. 0~255<br>
&emsp;&emsp;&emsp;`green` : green value. 0~255<br>
&emsp;&emsp;&emsp;`blue` : blue value. 0~255<br>

&emsp;<code class="code_accent">getUltrasonic()</code> : Return ultrasonic value as list. [front0, front1, rear1, rear2]<br> 
&emsp;&emsp;This method is used in AIoT AutoCAR Prime X, AIoT AutoCAR 2, AIoT AutoCAR 3.    
  
&emsp;<code class="code_accent">getAxis9()</code> : Return the accel, Magnetic, Gyro value as list. [accel_data x y z, magnetic_data x y z, gyro_data x y z]<br> 
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.     
  
&emsp;<code class="code_accent">getAccel(axis=None)</code> : Return the accel value   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`axis` : Enter 'x' or 'y' or 'z' to return the accel value of the axis. Return all if there is no input.  

&emsp;<code class="code_accent">getMagnetic(axis=None)</code> : Return the magnetic value   
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`axis` : Enter 'x' or 'y' or 'z' to return the magnetic value of the axis. Return all if there is no input. 

&emsp;<code class="code_accent">getGyro(axis=None)</code> : Return the gyro value   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`axis` : Enter 'x' or 'y' or 'z' to return the gyro value of the axis. Return all if there is no input. 

&emsp;<code class="code_accent">getEuler(axis=None)</code> : Return the euler value   
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`axis` : Enter 'x' or 'y' or 'z' to return the euler value of the axis. Return all if there is no input.

&emsp;<code class="code_accent">getGravity(axis=None)</code> : Return the gravity value   
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`axis` : Enter 'x' or 'y' or 'z' to return the gravity value of the axis. Return all if there is no input.

&emsp;<code class="code_accent">getLight()</code> : Return the CDS value   
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.   

&emsp;<code class="code_accent">getBattery()</code> : Return the Battery voltage value  
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.   

<br>

---

## <span class="title">Class</span> <span class="title_accent">**SerBot**</span>    

<blockquote class="desc">Class for easy control of AIoT SerBot Series.</blockquote>

The code to import the SerBot Class :

``` python
from pop.Pilot import SerBot
```

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">SerBot(bus=1)</code> : SerBot Object<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`bus` : I2c bus number to control SerBot's motors and sensors.   

<h4><b>Variables</b></h4>

&emsp;<code class="code_accent">steering</code> : Steer the front wheel of the SerBot left or right. Specify a value between -1 and 1.    

<h4><b>Methods</b></h4>

&emsp;<code class="code_accent">move(degree, speed)</code> : SerBot moves in the direction specified by degree.   
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
&emsp;&emsp;&emsp;`axis` : Enter 'x' or 'y' or 'z' to return the accel value of the axis. Return all if there is no input.   

&emsp;<code class="code_accent">getGyro(axis=None)</code> : Return the gyro value through the sensor mounted on the SerBot.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`axis` : Enter 'x' or 'y' or 'z' to return the gyro value of the axis. Return all if there is no input.   

<br>

---

## <span class="title">Class</span> <span class="title_accent">**joystick**</span>    
<br>

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">joystick()</code> : joystick object<br>
   
<h4><b>Methods</b></h4>   

&emsp;<code class="code_accent">show()</code> : display joystick<br> 

<br>

---

## <span class="title">Class</span> <span class="title_accent">**Data_Collector**</span>    

<blockquote class="desc">Image data collection class for machine learning.</blockquote>

The code to import the Data_Collector Class :

``` python
from pop.Pilot import Data_Collector
```

<h4><b>&emsp;Initialization</b></h4>

&emsp;<code class="code_accent">Data_Collector(separator, camera=None, auto_ready=True, save_per_sec=5)</code> : Data_Collector Object<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`separator` : Enter the purpose of data collection. 'Collision_Avoid' or 'Track_Follow'. In AIoT AutoCAR 3, 'Track_Follow_Turn' or 'Object_Follow' can be available.      
&emsp;&emsp;&emsp;`camera` : Camera class to utilize camera images.   
&emsp;&emsp;&emsp;`auto_ready` : Set whether to automatically configure a GUI screen to assist data collection.   
&emsp;&emsp;&emsp;`save_per_sec` : Amount of data stored per second.   

<h4><b>&emsp;Methods</b></h4>

&emsp;<code class="code_accent">show()</code> : GUI display for data collection.   

&emsp;<code class="code_accent">ready()</code> : Construct a GUI screen to assist data collection. It is configured according to Collision Avoid or Track Follow..   

&emsp;<code class="code_accent">save_as_joystick(value)</code> : Save the image using the joystick. Only use for Track Follow.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : This is a list containing 'sep', 'x', 'y'.   

&emsp;<code class="code_accent">control_as_joystick(value)</code> : Use the joystick to control the robot. Only use for Collision Avoid.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : This is a list containing 'sep', 'x', 'y'.   

&emsp;<code class="code_accent">save_blocked()</code> : Save the block image file in the specified path. Only use for Collision Avoid. default save path "./collision_dataset/blocked".  

&emsp;<code class="code_accent">save_free()</code> : Save the free image file in the specified path. Only use for Collision Avoid. default save path "./collision_dataset/free".   

&emsp;<code class="code_accent">save_snapshot(directory)</code> : Save the image file in the specified path. Only use for Collision Avoid.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`directory` : Path to save image file.   

<br>