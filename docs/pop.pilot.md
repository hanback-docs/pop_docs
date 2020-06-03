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
