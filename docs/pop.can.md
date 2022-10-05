<h1> Pop.CAN </h1>
Pop.CAN is easy and fast educational Library for CAN Protocol. It supports can communication and provides motor control and sensor monitoring using CAN communication.   
<br><br>

<!-- # Class & Method Description-->
<hr/>

## <span class="title">Class</span> <span class="title_accent">**Can**</span>
<blockquote class="desc">Class used whe using CAN interface.</blockquote><br>

The code to import the Can Class :

``` python
from pop.CAN import Can
```

<h4><b>&emsp;Initialization</b></h4>

&emsp;<code class="code_accent">Can()</code> : Can Object<br>

<h4><b>&emsp;Methods</b></h4>

&emsp;<code class="code_accent">send(msg_id, buf, is_extended=False)</code> : Sends a message via can communication. This method's name in AIoT AutoCAR Prime X, AIoT SerBot Prime X is "write".<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`msg_id` : Number of Message ID. <br>
&emsp;&emsp;&emsp;`buf` : It is a message to be transmitted through can communication.<br>
&emsp;&emsp;&emsp;`is_extended` : Check if the set ID is extended id.<br>   

&emsp;<code class="code_accent">recv(timeOut=2)</code> : Recv a message via can communication. This method's name in AIoT AutoCAR Prime X, AIoT SerBot Prime X is "read".<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`timeOut` : Time to wait for message.<br>   

&emsp;<code class="code_accent">setFilter(can_id, mask)</code> : Set the id filter for incoming messages.<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`can_id` : Can message id. <br>
&emsp;&emsp;&emsp;`mask` : Can message id. <br>

<br>

---

## <span class="title">Class</span> <span class="title_accent">**Car**</span>
<blockquote class="desc">This class controls AIoT AutoCar using Can communication.<br>
This class is used in AIoT AutoCAR Prime X, AIoT AutoCAR 2, AIoT AutoCAR 3.</blockquote><br>

The code to import the Car Class :

``` python
from pop.CAN import Car
```

<h4><b>&emsp;Initialization</b></h4>

&emsp;<code class="code_accent">Car()</code> : Car Object<br>

<h4><b>&emsp;Methods</b></h4>

&emsp;<code class="code_accent">wheel(value)</code> : Set dc motor speed.<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : Motor speed, between -100 and 100. 100 is forward 100%. -100 is backward 100%.<br>

&emsp;<code class="code_accent">steer(value)</code> : Set steer angle.<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : Steer angle, between -1 and +1. 0 is center.<br>

&emsp;<code class="code_accent">camPan(value)</code> : Set camera Pan angle.   
&emsp;&emsp;This method is used in AIoT Prime X, AIoT AutoCAR 2.<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : Camera Pan angle, between 10 and 170. 90 is center.<br>

&emsp;<code class="code_accent">camTilt(value)</code> : Set camera Tilt angle. <br>
&emsp;&emsp;This method is used in AIoT Prime X, AIoT AutoCAR 2.<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`value` : Camera Tilt angle, between 25 and 135. 90 is center.<br>

&emsp;<code class="code_accent">ultraEnable(enable=[0x03, 0x03, 0x01])</code> : Ultrasonic sensor reception status setting. <br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`enable` : List data with ultrasonic sensor activation information, 1 is activated 0 is disabled. The first factor is the front ultrasonic setup, and the second factor is the rear ultrasonic setup. Bit 0 of each element means left and bit 1 means right. and last factor is interval time(sec) setup.<br>

&emsp;<code class="code_accent">ultraDisable()</code> : Stop ultrasonic sensor receiving.<br>

&emsp;<code class="code_accent">imuEnable(enable=[0x0E, 0x01])</code> : IMU sensor reception status setting.<br>
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`enable` : List data with IMU sensor activation information, 1 is activated 0 is disabled. The first factor is the IMU setup, and the second factor is the interval time(sec) setup. In first factor, bit 0 is calibration, bit 1 is accel, bit 2 is magnetic, bit 3 is gyro, bit 4 is euler, bit 5 is gravity.<br>

&emsp;<code class="code_accent">imuDisable()</code> : Stop IMU sensor receiving.<br>
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.  

&emsp;<code class="code_accent">calibrationEnable(enable=[0x01, 0x01])</code> : IMU sensor reception status setting.<br>
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`enable` : List data with IMU sensor activation information, 1 is activated 0 is disabled. The first factor is the IMU setup, and the second factor is the interval time(sec) setup. In first factor, bit 0 is calibration, bit 1 is accel, bit 2 is magnetic, bit 3 is gyro, bit 4 is euler, bit 5 is gravity.<br>

&emsp;<code class="code_accent">cdsEnable(enable=[0x01])</code> : Cds sensor reception status setting.<br>
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`enable` : List data is the interval time(sec) setup.<br>

&emsp;<code class="code_accent">cdsDisable()</code> : Stop cds sensor receiving.<br>
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.  

&emsp;<code class="code_accent">battEnable(enable=[0x01])</code> : Battery voltage reception status setting.<br>
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.  
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`enable` : List data is the interval time(sec) setup.<br>

&emsp;<code class="code_accent">battDisable()</code> : Stop battery voltage receiving.<br>
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.  

&emsp;<code class="code_accent">setObstacleDistance(distance = 20)</code> : Obstacle detection distance setting.<br>
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.  
&emsp;&emsp;**Params**      
&emsp;&emsp;&emsp;`distance` : Set obstacle distance. 20 < range <= 180. If distance set below 20, obstacle distance function disable.<br>

&emsp;<code class="code_accent">readStart()</code> : Read thread start.<br>

&emsp;<code class="code_accent">readStop()</code> : Read thread stop.<br>

&emsp;<code class="code_accent">readUltra()</code> : Return ultrasonic sensor as list. [front0, front1, rear0, rear1]   
&emsp;&emsp;This method's name in AIoT AutoCAR Prime X is "read".<br>

&emsp;<code class="code_accent">readAccel()</code> : Return accel sensor as list. [x,y,z]<br>
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.  

&emsp;<code class="code_accent">readMagnetic()</code> : Return magnetic sensor as list. [x,y,z]<br>
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.  

&emsp;<code class="code_accent">readGyro()</code> : Return gyro sensor as list. [x,y,z]<br>
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.  

&emsp;<code class="code_accent">readEuler()</code> : Return euler sensor as list. [x,y,z]<br>
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.  

&emsp;<code class="code_accent">readGravity()</code> : Return gravity sensor as list. [x,y,z]<br>
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.  

&emsp;<code class="code_accent">imu_calibration()</code> : Return IMU calibration result. bit0~1 is mag, bit 2~3 is accel, bit4~5 is gyro, bit6~7 is sys.<br>
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.  

&emsp;<code class="code_accent">readCds()</code> : Return cds sensor as int.<br>
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.  

&emsp;<code class="code_accent">readBattery()</code> : Return Battery voltage.<br>
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.  

&emsp;<code class="code_accent">lampControl(front=0, rear=0)</code> : Set lamp on/off.<br> 
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.  
&emsp;&emsp;**Params**      
&emsp;&emsp;&emsp;`front` : Front lamp on(1)/off(0)<br>
&emsp;&emsp;&emsp;`rear` : Rear lamp on(1)/off(0)<br>

&emsp;<code class="code_accent">alarm(scale,pitch,duration=0)</code> : Control buzzer.<br> 
&emsp;&emsp;This method is used in AIoT AutoCAR 2, AIoT AutoCAR 3.  
&emsp;&emsp;**Params**      
&emsp;&emsp;&emsp;`scale` : Set scale<br>
&emsp;&emsp;&emsp;`pitch` : Set pitch<br>
&emsp;&emsp;&emsp;`duration` : Set duration<br>

&emsp;<code class="code_accent">PixelDisplay(num, red, green=0, blue=0)</code> : Set PixelDisplay.<br> 
&emsp;&emsp;This method is used in AIoT AutoCAR 2.  
&emsp;&emsp;**Params**      
&emsp;&emsp;&emsp;`num` : Pixel display number. 0~255<br>
&emsp;&emsp;&emsp;`red` : Red value. 0~255<br>
&emsp;&emsp;&emsp;`green` : Green value. 0~255<br>
&emsp;&emsp;&emsp;`blue` : Blue value. 0~255<br>

<br>

----

## <span class="title">Class</span> <span class="title_accent">**OmniWheel**</span>    

<blockquote class="desc">This class controls OmniWheel using Can communication.<br>
This class is used in AIoT SerBot Prime X.</blockquote><br>

The code to import the OmniWheel Class :

``` python
from pop.CAN import OmniWheel
```

<h5>&emsp;Initialization</h5>

&emsp;<code class="code_accent">OmniWheel()</code> : OmniWheel Object<br>

<h5>&emsp;Variables</h5>  
  
&emsp;<code class="code_accent">ULTRASONIC</code> : Constant for reading ultrasonic sensor data.    
&emsp;<code class="code_accent">PSD</code> : Constant for reading PSD sensor data.     
&emsp;<code class="code_accent">ALARM</code> : Constant for reading Obstacle Detect Alarm.     
&emsp;<code class="code_accent">SENSOR_ALL</code> : Constant for reading All sensor data.     

<h5>&emsp;Methods</h5>

&emsp;<code class="code_accent">forward(data)</code> : Method used to move the wheel forward. <br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`data` : List including motor speed, input motor 1,2,3 in sequence, integer between 0 and 100, and if 100, motor operates at 100% speed </br>

&emsp;<code class="code_accent">backward(data)</code> : Method used to move the wheel backward. <br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`data` : List including motor speed, input motor 1,2,3 in sequence, integer between 0 and 100, and if 100, motor operates at 100% speed </br>

&emsp;<code class="code_accent">setObstacleRange(ultra_distance, psd_distance)</code> : Obstacle detection distance setting <br>
&emsp;&emsp; When the two values are the same -> No notification, only detection, motor stops when detected. <br>
&emsp;&emsp; When the two values are not the same -> Only the notification message is delivered between the maximum and minimum values. <br>
&emsp;&emsp; When the two values are not the same -> Motor stop and notification message when it is less than the minimum value. <br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`ultra_distance` : Ultrasonic sensor detection distance. </br>
&emsp;&emsp;&emsp;`psd_distance` : PSD sensor detection distance </br>

&emsp;<code class="code_accent">stop()</code> : Method used to Motor stop 

&emsp;<code class="code_accent">allSensorEnable()</code> : Method used to receive all sensor data from the Omni Wheel </br>

&emsp;<code class="code_accent">ultraEnable(enable=[1,1,1,1,1,1])</code> : Ultrasonic sensor reception status setting. <br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`enable` : List data with ultrasonic sensor activation information, 1 is activated 0 is disabled. </br>

&emsp;<code class="code_accent">psdEnable(enable=[1,1,1])</code> : PSD sensor reception status setting. <br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`enable` : List data with PSD sensor activation information, 1 is activated 0 is disabled </br>

&emsp;<code class="code_accent">getEnable()</code> : Return sensor reception status. </br>

&emsp;<code class="code_accent">sensorDisable()</code> : Disable sensor reception. </br>

&emsp;<code class="code_accent">read(msgType)</code> : Reading messages received on the Omni wheel via CAN communication. <br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`msgType` : There are 4 types of data to be passed to msgType. </br>
&emsp;&emsp;&emsp;&emsp;`SENSORALL` : Constant for reading All sensor data. </br>
&emsp;&emsp;&emsp;&emsp;`ULTRASONIC` : Constant for reading ultrasonic sensor data. </br> 
&emsp;&emsp;&emsp;&emsp;`PSD` : Constant for reading PSD sensor data. </br>
&emsp;&emsp;&emsp;&emsp;`ALARM` : Constant for reading Obstacle Detect Alarm. </br>

&emsp;<code class="code_accent">setCallback(func,param=None)</code> : Set up callback function for Obstacle Alarm <br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`func` : Function to use when calling Callback </br>
&emsp;&emsp;&emsp;`param` : Parameters passed to the Callback function , Default None </br>
