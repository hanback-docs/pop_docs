<h1> Pop.CAN </h1>
Pop.CAN is easy and fast educational Library for CAN Protocol. It supports can communication and provides motor control and sensor monitoring using CAN communication.
<br>

<!-- # Class & Method Description-->
<hr/>

## <span class="title">Class</span> <span class="title_accent">**Can**</span>    

<blockquote class="desc">Class used whe using CAN interface.</blockquote>

The code to import the Can Class :

``` python
from pop.CAN import Can
```

<h5>&emsp;Initialization</h5>

&emsp;<code class="code_accent">Can()</code> : Can Object<br>

<h5>&emsp;Methods</h5>

&emsp;<code class="code_accent">send(msg_id, buf, is_extended=False)</code> : Sends a message via can communication. 
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`msg_id` : Number of Message ID. 
&emsp;&emsp;&emsp;`buf` : It is a message to be transmitted through can communication.  
&emsp;&emsp;&emsp;`is_extended=False` : Check if the set ID is extended id.  

&emsp;<code class="code_accent">recv(timeOut=2)</code> : Recv a message via can communication.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`timeOut=2` : Time to wai for message.   

&emsp;<code class="code_accent">setFilter(can_id, mask)</code> : Set the id filter for incoming messages.   
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`can_id` : can message id. 
&emsp;&emsp;&emsp;`mask` : can message id. 

---

## <span class="title">Class</span> <span class="title_accent">**OmniWheel**</span>    

<blockquote class="desc">This class controls OmniWheel using Can communication.</blockquote>

The code to import the OmniWheel Class :

``` python
from pop.CAN import OmniWheel
```

<h5>&emsp;Initialization</h5>

&emsp;<code class="code_accent">OmniWheel()</code> : OmniWheel Object<br>

<h5>&emsp;Variables</h5>  

&emsp;<code class="code_accent">MOTOR_CONTROL</code> :      
&emsp;<code class="code_accent">MOTOR_STOP</code> :      
&emsp;<code class="code_accent">SENSOR_REQUEST</code> :      
&emsp;<code class="code_accent">OBSTACLE_DISTANCE</code> :      
&emsp;<code class="code_accent">OBSTACLE_DETECT</code> :      
&emsp;<code class="code_accent">OBSTACLE_ALARM</code> :      
&emsp;<code class="code_accent">RECV_ULTRASONIC</code> :      
&emsp;<code class="code_accent">RECV_PSD</code> :      
&emsp;<code class="code_accent">ULTRASONIC</code> :      
&emsp;<code class="code_accent">PSD</code> :      
&emsp;<code class="code_accent">ALARM</code> :      
&emsp;<code class="code_accent">SENSOR_ALL</code> :      

<h5>&emsp;Methods</h5>

&emsp;<code class="code_accent">forward(data)</code> : 
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`data` : 

&emsp;<code class="code_accent">backward(data)</code> : 
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`data` : 

&emsp;<code class="code_accent">setObstacleDetect(distance)</code> : 
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`distance` : 

&emsp;<code class="code_accent">stop()</code> : 

&emsp;<code class="code_accent">allSensorEnable()</code> : 

&emsp;<code class="code_accent">ultraEnable(enable=[1,1,1,1,1,1])</code> : 
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`enable` : 

&emsp;<code class="code_accent">psdEnable(enable=[1,1,1])</code> : 
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`enable` : 

&emsp;<code class="code_accent">getEnable()</code> : 

&emsp;<code class="code_accent">sensorDisable()</code> : 

&emsp;<code class="code_accent">readStart()</code> : 

&emsp;<code class="code_accent">readStop()</code> : 

&emsp;<code class="code_accent">read(sensorType)</code> : 
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`sensorType` : 

---

