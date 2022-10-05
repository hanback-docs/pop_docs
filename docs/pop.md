<h1> Pop </h1>
The code to import the whole of Pop Library : 

```python
from pop import *
```
<br>

<!-- # Class & Method Description-->

---   

## <span class="title">Class</span> <span class="title_accent">**Camera**</span>    
<blockquote class="desc">Camera</blockquote><br>

<h4><b>Initialization</b></h4>    

&emsp;<code class="code_accent">Camera(width=224, height=224, auto_load=True)</code> : Camera object<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`width` : camera width. default 224    
&emsp;&emsp;&emsp;`height` : camera height. default 224    
&emsp;&emsp;&emsp;`auto_load` : set auto load<br>    

<h4><b>Methods</b></h4> 

&emsp;<code class="code_accent">show()</code> : display camera image  

&emsp;<code class="code_accent">stop()</code> : stop display camera image    

<h4><b>Example</b></h4> 

<details>
	<summary>simple example</summary>

~~~python
from pop import Camera
import time 

cam = Camera()
cam.show()
time.sleep(5)
cam.stop()
~~~

</details>

<br>

---   

## <span class="title">Class</span> <span class="title_accent">**Out**<a id="class-out"></a></span>    
<blockquote class="desc">Output device is controlled by GPIO.</blockquote><br> 

<h4><b>Initialization</b></h4>     

&emsp;<code class="code_accent">Out(n)</code> : Out Object<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`n` : GPIO number connected to the Output Device   

<h4><b>Methods</b></h4> 

&emsp;<code class="code_accent">allOn()</code> : Set all GPIO connected to Output Device to HIGH<br>

&emsp;<code class="code_accent">allOff()</code> : Set all GPIO connected to Output Device to LOW<br>

<h4><b>Example</b></h4> 

<details>
	<summary>simple example</summary>

~~~python
from pop import Leds
import time 

leds = Leds()
leds.allOn()
time.sleep(1)
leds.allOff()  
~~~

</details>

<br>

---   

## <span class="title">Class</span> <span class="title_accent">**Led**</span>    
<blockquote class="desc">LEDs are controlled by GPIO.<br>
This class is used in AIoT Home, AIoT Server Plus.</blockquote><br> 

<h4><b>Initialization</b></h4>     

&emsp;<code class="code_accent">Led(n)</code> : Led Object inheriting from [Out Class](pop.md#class-out)<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`n` : GPIO number connected to the LED   

<h4><b>Methods</b></h4> 

&emsp;Refer to [Out Class](pop.md#class-out) for inherited and used methods.<br>

<h4><b>Example</b></h4> 

<details>
	<summary>simple example 1</summary>

~~~python
from pop import Led
import time 

led = Led(1)
o.on()
time.sleep(1)
o.off()    
~~~

</details>

<details>
	<summary>simple example 2</summary>

~~~python
from pop import Led
import time 

leds = [Led(23), Led(24), Led(25), Led(27)]    

for i in range(20):
	for led in leds:
	led.on()
	time.sleep(0.1)

	for led in leds:
	led.off()
	time.sleep(0.1)  
~~~

</details>

<br>

---   

## <span class="title">Class</span> <span class="title_accent">**Leds**</span>    
<blockquote class="desc">LEDs are controlled by GPIO.<br>
This class is used in PyCBasic.</blockquote><br>

<h4><b>Initialization</b></h4>    

&emsp;<code class="code_accent">Leds(n)</code> : Leds object inheriting from Led Class<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`n` : List number defined in board and connected to the LED<br>    

<h4><b>Methods</b></h4> 

&emsp;<code class="code_accent">show()</code> : display camera image    

&emsp;<code class="code_accent">stop()</code> : stop display camera image    

<h4><b>Example</b></h4> 

<details>
	<summary>simple example</summary>

~~~python
from pop import Leds
import time 

leds = Leds()
leds.allOn()
time.sleep(1)
leds.allOff()
~~~

</details>

<br>

---   

## <span class="title">Class</span> <span class="title_accent">**Fan**</span>    
<blockquote class="desc">Fan is controlled by GPIO.<br>
This class is used in AIoT Home.</blockquote><br>

<h4><b>Initialization</b></h4>    

&emsp;<code class="code_accent">Fan(n)</code> : Fan object inheriting from [Out Class](pop.md#class-out)<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`n` : GPIO number connected to the Fan<br>    

<h4><b>Methods</b></h4> 

&emsp;Refer to [Out Class](pop.md#class-out) for inherited and used methods.<br>

<h4><b>Example</b></h4> 

<details>
	<summary>simple example</summary>

~~~python
from pop import Fan
import time 

dcfan = Fan(17)
dcfan.on()
time.sleep(2)
dcfan.off()
~~~

</details>

<br>

---   

## <span class="title">Class</span> <span class="title_accent">**Input**<a id="class-input"></a></span>    
<blockquote class="desc">Read the Input Device through GPIO.</blockquote><br>

<h4><b>Initialization</b></h4>    

&emsp;<code class="code_accent">Input(n,activeHigh=True)</code> : Input Object<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`n` : GPIO number connected to the Input Device.<br>
&emsp;&emsp;&emsp;`activeHigh` : Used to check if the Input Device is HIGH when pressed, Default True.<br>    

<h4><b>Definitions</b></h4> 

&emsp;<code class="code_accent">FALLING</code> : Detect Falling Edge.   
&emsp;<code class="code_accent">RISING</code> : Detect Rising Edge.  
&emsp;<code class="code_accent">BOTH</code> : Detect Both Side.   

<h4><b>Methods</b></h4> 

&emsp;<code class="code_accent">read()</code> : Read the Input Device status.   

&emsp;<code class="code_accent">setCallback(func,param=None,type=BOTH)</code> : Set Callback function when detecting Edge.   
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`func` : Function to use when calling Callback.<br>
&emsp;&emsp;&emsp;`param` : Parameters passed to the Callback function, Default None.<br>
&emsp;&emsp;&emsp;`type` : Call condition of Callback function, Default BOTH.<br>

<h4><b>Example</b></h4> 

<details>
	<summary>simple example</summary>

~~~python
from pop import Input

input = Input(22)
data = input.read()
print(ret)
~~~

</details>

<br>

---   

## <span class="title">Class</span> <span class="title_accent">**Flame**</span>    
<blockquote class="desc">Flame sensor status reading.<br>
This class is used in AIoT Server Plus, SensorPack option.</blockquote><br>    

<h4><b>Initialization</b></h4>    

&emsp;<code class="code_accent">Flame(n)</code> : Flame object inheriting from [Input Class](pop.md#class-input)<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`n` : Connected pin number.    

<h4><b>Methods</b></h4> 

&emsp;<code class="code_accent">read()</code> : Returns Flame status. If flame is detected, value is `False`. And if flame is not detected, value is `True`.<br>

&emsp;<code class="code_accent">setCallback(func,param=None,type=BOTH)</code> : Callback function setting called Edge is detected.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`func` : Callback function<br>
&emsp;&emsp;&emsp;`param` : Parameters passed to Callback function<br>
&emsp;&emsp;&emsp;`type` : Edge type

<h4><b>Example</b></h4> 

<details>
	<summary>simple example 1</summary>

~~~python
from pop import Flame
import time
flame1 = Flame(17)
flame2 = Flame(27)
while True:
	print("flame1 : %d , flame2 : %d"%(flame1.read(),flame2.read()))
	time.sleep(0.05)
~~~

</details>

<details>
	<summary>simple example 2</summary>

~~~python
from pop import Flame
import time
flame1 = Flame(17)
count = 0
def onFlame(unuse):
	globla count
	caount += 1
	print("flame = %d"%(count))
	time.sleep(1)

flame.setCallback(onFlame, None, Flame.FALLING)
input("Press <Enter> Key...\n")
~~~

</details>

<br>

---

## <span class="title">Class</span> <span class="title_accent">**Switch**<a id="class-switch"></a></span>    
<blockquote class="desc">Read the switch status through GPIO.<br>
This class is used in AIoT Server Plus.</blockquote><br>    

<h4><b>Initialization</b></h4>   

&emsp;<code class="code_accent">Switch(n)</code> : Switch object inheriting from [Input Class](pop.md#class-input)<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`n` : GPIO number connected to the switch.    

<h4><b>Methods</b></h4> 

&emsp;Refer to [Input Class](pop.md#class-input) for inherited and used methods.

<h4><b>Example</b></h4> 

<details>
	<summary>simple example</summary>

~~~python
from pop import Switch

sw = Switch(22)
data = sw.read()
print(data)
~~~

</details>

<br>

---

## <span class="title">Class</span> <span class="title_accent">**Switches**</span>    
<blockquote class="desc">Read the switch status through GPIO.<br>
This class is used in PyCBasic.</blockquote><br>    

<h4><b>Initialization</b></h4>   

&emsp;<code class="code_accent">Switches(n)</code> : Switch object inheriting from [Input Class](pop.md#class-input)<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`n` : List number defined in the board and connected to the Switch.    

<h4><b>Methods</b></h4> 

&emsp;Refer to [Input Class](pop.md#class-input) or [Switch Class](pop.md#class-switch) for inherited and used methods.

<h4><b>Example</b></h4> 

<details>
	<summary>simple example</summary>

~~~python
from pop import Switches
switch = Switches()

data = switch[0].read()

print(data)
~~~

</details>

<br>

---
## <span class="title">Class</span> <span class="title_accent">**Bme680**</span>    
<blockquote class="desc">Read the gas, temperature, humidity and pressure status.<br>
This class is used in SensorPack option.</blockquote><br>    

<h4><b>Initialization</b></h4>   

&emsp;<code class="code_accent">Bme680(n)</code> : Bme680 object<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`n` : I2C Address of Bme680. Default 0x77.    

<h4><b>Methods</b></h4>

&emsp;<code class="code_accent">init()</code> : Bme680 chip initialization, called when creating a class.<br>

&emsp;<code class="code_accent">softReset()</code> : Bme680 chip software reset.<br>

&emsp;<code class="code_accent">getSensorData()</code> : Data collection of temperature/humidity sensor, return in list format (temperature, pressure, humidity, gas_resistance).<br>

&emsp;<code class="code_accent">getTemperature()</code> : Returns temperature data(°C).<br>

&emsp;<code class="code_accent">getHumidity()</code> : Returns humidity data(%).<br>

&emsp;<code class="code_accent">getPressure()</code> : Returns atmospheric pressure data(hpa).<br>

&emsp;<code class="code_accent">getGas()</code> : Returns gas data(ohm).<br>

<h4><b>Example</b></h4> 

<details>
	<summary>simple example</summary>

~~~python
from pop import Bme680
import time
b = Bme680(0x77)
while True:
	sensor = b.getSensorData()
	temp = b.getTemperature()
	humi = b.getHumidity()
	pressure = b.getPressure()
	gas = b.getGas()
	print("sensor data = %d, %d, %d, %d"%(sensor[0],sensor[1],sensor[2] ,sensor[3]))
	print("temp : %d [C], humi : %d [%%] , pressure : %d [hpa], gas : %d [ohm]"%(temp,humi,pressure,gas))
	time.sleep(0.5)
~~~

</details>

<br>

---

## <span class="title">Class</span> <span class="title_accent">**Light**</span>    
<blockquote class="desc">Light status reading.<br>
This class is used in SensorPack option.</blockquote><br>    

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">Light(n)</code> : Light object<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`n` : I2C Address of Light chip. Default 0x23.    

<h4><b>Methods</b></h4>

&emsp;<code class="code_accent">init()</code> : Light chip initialization, Called when creating class.<br>

&emsp;<code class="code_accent">getLight()</code> : Returns Light data(lx).<br>

<h4><b>Example</b></h4> 

<details>
	<summary>simple example</summary>

~~~python
from pop import Light
import time
l = Light(0x23)
while True:
	print("light : %d [lx]"%l.getLight())
	time.sleep(0.5)
~~~

</details>

<br>

---
## <span class="title">Class</span> <span class="title_accent">**CO2**</span>    
<blockquote class="desc">Read status of CO2 Sensor.<br>
This class is used in SensorPack option.</blockquote><br>    

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">CO2()</code> :  CO2 Producer. It takes 1 second to initialize<br>
   

<h4><b>Methods</b></h4>

&emsp;<code class="code_accent">read()</code> :  Return CO2 ppm value of CO2 Sensor. It takes 5 seconds to return.<br>

<h4><b>Example</b></h4> 

<details>
	<summary>simple example</summary>

~~~python
from pop import CO2
import time
c = CO2()
while True:
	print(c.read())
~~~

</details>

<br>

---

## <span class="title">Class</span> <span class="title_accent">**Thermopile**</span>    
<blockquote class="desc">Thermopile sensor status reading.<br>
This class is used in SensorPack option.</blockquote><br>  

<h4><b>Initialization</b></h4>  

&emsp;<code class="code_accent">Thermopile(n)</code> : Thermopile object inheriting from PopThread<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`n` :  Connected SEC pin number.    

<h4><b>Methods</b></h4>

&emsp;<code class="code_accent">read()</code> : Returns measured temperature(°C).<br>

&emsp;<code class="code_accent">setChipSelect(cs) </code> : Sets SEC pin.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`cs` : Connected pin number<br>

&emsp;<code class="code_accent">setInterval(n)</code> : Sets Laser Turn on cycle(sec).<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`n` : Laser Turn on cycle (sec)<br>

&emsp;<code class="code_accent">laserOn()</code> : Manual command for Laser Turn on.<br>

&emsp;<code class="code_accent">setLaserAutomode(Automode)</code> : Laser Automode setting. Sets to Default True when creating a class.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`Automode` : If `True`, sets Automode. Release if `False`.

<h4><b>Example</b></h4> 

<details>
	<summary>simple example</summary>

~~~python
from pop import Thermopile
import time
d = Thermopile(7)
while True:
	print(d.read())
	time.sleep(1)
~~~

</details>	

<br>

---
## <span class="title">Class</span> <span class="title_accent">**MicroWave**</span>    
<blockquote class="desc">Reading the speed of obstacles ahead of Micro Wave Sensor.<br>
This class is used in SensorPack option.</blockquote><br> 

<h4><b>Initialization</b></h4>   

&emsp;<code class="code_accent">MicroWave(n)</code> : MicroWave object<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`n` : Connected pin information.    

<h4><b>Methods</b></h4>   

&emsp;<code class="code_accent">read()</code> :  Returns the speed of the obstacle ahead (km/h). If not, returns 0.<br>

<h4><b>Example</b></h4>

<details>
	<summary>simple example</summary>

~~~python
from pop import MicroWave
import time
m = MicroWave(16)
while True:
	result = m.read()
	if result!=0:
		print("%5.5f [km/h]\r\n"%(result))
	else:
		print(".\n")
	time.sleep(0.5)
~~~

</details>	


---

## <span class="title">Class</span> <span class="title_accent">**Pir**</span>    
<blockquote class="desc">Responds to the movement of infrared wavelengths emitted or reflected from an object.<br>
This class is used in AIoT Server Plus, SensorPack option.</blockquote><br> 

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">Pir(n)</code> : Pir object inheriting from [Input Class](pop.md#class-input)<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`n` : GPIO number connected to the Pir. 

<h4><b>Methods</b></h4>

&emsp;Refer to [Input Class](pop.md#class-input) for inherited and used methods.

<h4><b>Example</b></h4> 

<details>
	<summary>simple example 1</summary>

~~~python
from pop import Pir
pir = Pir(22)

data = pir.read()

print(data)
~~~

</details>

<details>
	<summary>simple example 2</summary>

~~~python
from pop import Pir
import time

pir = Pir(22)

def onPir(param):
	ret = pir.read()
	if (ret == True):
	print("detect...")
	time.sleep(2)
	else:
	time.sleep(0.1)

pir.setCallback(onPir)
input("Press <Enter> Key...\n")
~~~

</details>

<br>

---
## <span class="title">Class</span> <span class="title_accent">**SpiAdc**<a id="class-spiadc"></a></span>    
<blockquote class="desc">adc chip control through spi interface.</blockquote><br>   

<h4><b>Initialization</b></h4>   

&emsp;<code class="code_accent">SpiAdc(channel, device=0, ce=0, speed=1000000)</code> : SpiAdc object <br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`channel` : ADC Channel.    
&emsp;&emsp;&emsp;`device` : SPI Interface Channel, Default 0 (in Raspberry Pi).    
&emsp;&emsp;&emsp;`ce` : The SPI_CE(or CS) number to which the slave is connected. Default 0.     
&emsp;&emsp;&emsp;`speed` : SPI Interface Clock Speed, Default 1000000(1MHz).  
			
<h4><b>Definitions</b></h4>  

&emsp;<code class="code_accent">TYPE_AVERAGE</code> : Average data based on sampling count.    
&emsp;<code class="code_accent">TYPE_NORMAL</code> : Unaveraged raw data.    
&emsp;<code class="code_accent">MODE_FULL</code> : Call Callback function always.    
&emsp;<code class="code_accent">MODE_INCLUSIVE</code> : If data is in a range (max, min), call Callback function.    
&emsp;<code class="code_accent">MODE_EXCLUSIVE</code> : If data is over a range, call Callback function.    

<h4><b>Methods</b></h4>   

&emsp;<code class="code_accent">getSample()</code> : Get Sampling Count.    

&emsp;<code class="code_accent">read()</code> : Read Data from Device (Raw Type).    

&emsp;<code class="code_accent">readAverage()</code> : Read Average Data from Device.    

&emsp;<code class="code_accent">run()</code> : Read data and call Callback function according to mode.  

&emsp;<code class="code_accent">setSample(sample)</code> : Set Sampling Count.<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`sample` : Sampling count.   

&emsp;<code class="code_accent">readVolt(ref=3.3,max=3020.0)</code> : Read Data from Device. (Voltage Type)<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`ref` : Reference Voltage.    
&emsp;&emsp;&emsp;`max` : Maximum value of raw data.   

&emsp;<code class="code_accent">readVoltAverage(ref=3.3,max=3020.0)</code> : Read Data from Device. (Voltage Type)<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`ref` : Reference Voltage.    
&emsp;&emsp;&emsp;`max` : Maximum value of raw data.   

&emsp;<code class="code_accent">setCallback(func,param=None,type=TYPE_AVERAGE,mode=MODE_FULL,min=0,max=ADC_MAX)</code> : Set up callback function for automatic data read.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`func` : Function to use when calling Callback.    
&emsp;&emsp;&emsp;`param` : Arguments passed to the Callback function. Default None.    
&emsp;&emsp;&emsp;`type` : Data Read Type. Default TYPE_AVERAGE.    
&emsp;&emsp;&emsp;`mode` : Select Mod. Default MODE_FULL.    
&emsp;&emsp;&emsp;`min` : analog data minimum. Default 0.    
&emsp;&emsp;&emsp;`max` : analog data maximum. Default 4095. (MCP3208 12bit ADC Chip)

<br>

---

## <span class="title">Class</span> <span class="title_accent">**Psd**</span>    
<blockquote class="desc">Distance measurement using PSD sensor.<br>
This class is used in AIoT Server Plus, PyCBasic.</blockquote><br>   

<h4><b>Initialization</b></h4>   

&emsp;<code class="code_accent">Psd(channel=-1, device=0, ce=0, speed=1000000)</code> : PSD object inheriting from [SpiAdc Class](pop.md#class-spiadc)<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`channel` : ADC Channel.    
&emsp;&emsp;&emsp;`device` : SPI Interface Channel. Default 0. (in Raspberry Pi)    
&emsp;&emsp;&emsp;`ce` : The SPI_CE(or CS) number to which the slave is connected. Default 0.    
&emsp;&emsp;&emsp;`speed` : SPI Interface Clock Speed. Default 1000000(1MHz).    

<h4><b>Methods</b></h4>  

&emsp;<code class="code_accent">calcDist(val,calibration=1.1)</code> : Calculate distance value from raw data.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`val` : ADC Raw Data.    
&emsp;&emsp;&emsp;`calibration` : Calibration Value. Default 1.1.    
			
<br>

---

## <span class="title">Class</span> <span class="title_accent">**CDS**</span>  
<blockquote class="desc">Light measurement using CDS sensor.<br>
This class is used in AIoT AutoCAR, AIoT AutoCAR Prime, AIoT AutoCAR Prime X, AIoT Home, AIoT SerBot, AIoT SerBot Prime X, AIoT Server Plus, PyCBasic.</blockquote><br>   

<h4><b>Initialization</b></h4>   

&emsp;<code class="code_accent">Cds(channel=-1, device=0, ce=0, speed=1000000)</code> : Cds object inheriting from [SpiAdc Class](pop.md#class-spiadc)<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`channel` : ADC Channel    
&emsp;&emsp;&emsp;`device` : SPI Interface Channel. Default 0. (in Raspberry Pi)    
&emsp;&emsp;&emsp;`ce` : The SPI_CE(or CS) number to which the slave is connected. Default 0.    
&emsp;&emsp;&emsp;`speed` : SPI Interface Clock Speed. Default 1000000(1MHz).    
			
<h4><b>Methods</b></h4>  

&emsp;<code class="code_accent">readAverage()</code> : Read lux data from device and calibration function.  
&emsp;<code class="code_accent">setCalibrationPseudoLx(func)</code> : Set calibration function.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`func` : Calibration function.

<br>

---

## <span class="title">Class</span> <span class="title_accent">**Gas**</span>    
<blockquote class="desc">Gas amount measurement using Gas sensor.<br>
This class is used in AIoT Home, AIoT Server Plus.</blockquote><br>   

<h4><b>Initialization</b></h4>   

&emsp;<code class="code_accent">Gas(channel=-1, device=0, ce=0, speed=1000000)</code> : Gas object inheriting from [SpiAdc Class](pop.md#class-spiadc)<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`channel` : ADC Channel    
&emsp;&emsp;&emsp;`device` : SPI Interface Channel. Default 0. (in Raspberry Pi)    
&emsp;&emsp;&emsp;`ce` : The SPI_CE(or CS) number to which the slave is connected. Default 0.    
&emsp;&emsp;&emsp;`speed` : SPI Interface Clock Speed. Default 1000000(1MHz).       
			
<h4><b>Methods</b></h4>

&emsp;<code class="code_accent">read()</code> : Measured gas volume read as voltage value.<br>

&emsp;<code class="code_accent">readAverage()</code> : Read the average gas volume as an RMS-based voltage value.<br>

&emsp;<code class="code_accent">calcPropan(val)</code> : Convert gas volume into propane amounts in PPM units.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`val` : Value read through method 'readAverage'.    

&emsp;<code class="code_accent">calcMethan(val)</code> : Convert gas volume into methane amounts in PPM units.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`val` : Value read through method 'readAverage'.    

&emsp;<code class="code_accent">calcEthanol(val)</code> : Convert gas volume into ethanol amounts in PPM units.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`val` : Value read through method 'readAverage'.    

<br>

---

## <span class="title">Class</span> <span class="title_accent">**Temperature**</span>  
<blockquote class="desc">Temperature measurement using LM32 sensor.<br>
This class is used in AIoT Server Plus.</blockquote><br>   

<h4><b>Initialization</b></h4>   

&emsp;<code class="code_accent">Temperature(channel, device=0, ce=0, speed=1000000)</code> : Temperature object inheriting from [SpiAdc Class](pop.md#class-spiadc)<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`channel` : ADC Channel.    
&emsp;&emsp;&emsp;`device` : SPI Interface Channel. Default 0. (in Raspberry Pi)    
&emsp;&emsp;&emsp;`ce` : The SPI_CE(or CS) number to which the slave is connected. Default 0.    
&emsp;&emsp;&emsp;`speed` : SPI Interface Clock Speed. Default 1000000(1MHz).   
			
<h4><b>Methods</b></h4>

&emsp;<code class="code_accent">calcTempC(val)</code> : Convert the value read to Celsius temperature.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`val` : Value read through method 'readAverage'.    

<br>

---

## <span class="title">Class</span> <span class="title_accent">**Sound**</span>    
<blockquote class="desc">Ambient sound measurement using Sound sensor.<br>
This class is used in AIoT Server Plus, PyCBasic.</blockquote><br>   

<h4><b>Initialization</b></h4>   

&emsp;<code class="code_accent">Sound(channel=-1, device=0, ce=0, speed=1000000)</code> : Sound object inheriting from [SpiAdc Class](pop.md#class-spiadc)<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`channel` : ADC Channel.    
&emsp;&emsp;&emsp;`device` : SPI Interface Channel. Default 0. (in Raspberry Pi)    
&emsp;&emsp;&emsp;`ce` : The SPI_CE(or CS) number to which the slave is connected. Default 0.    
&emsp;&emsp;&emsp;`speed` : SPI Interface Clock Speed. Default 1000000(1MHz).    
			
<br>

---
<!-- 
## <span class="title">Class</span> <span class="title_accent">**Vr**</span>    
<blockquote class="desc">Voltage measurement with variable resistor.<br>
This class is used in AIoT Server Plus.</blockquote><br>   

<h4><b>Initialization</b></h4>   

&emsp;<code class="code_accent">Vr(channel=-1, device=0, ce=0, speed=1000000)</code> : Vr object inheriting from [SpiAdc Class](pop.md#class-spiadc)<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`channel` : ADC Channel.    
&emsp;&emsp;&emsp;`device` : SPI Interface Channel. Default 0. (in Raspberry Pi)    
&emsp;&emsp;&emsp;`ce` : The SPI_CE(or CS) number to which the slave is connected. Default 0.    
&emsp;&emsp;&emsp;`speed` : SPI Interface Clock Speed. Default 1000000(1MHz).    
			
<br>

--- -->

## <span class="title">Class</span> <span class="title_accent">**Potentiometer**</span>    
<blockquote class="desc">Voltage measurement with variable resistor.<br>
This class is used in AIoT Server Plus, PyCBasic.</blockquote><br>   

<h4><b>Initialization</b></h4>

&emsp;<code class="code_accent">Potentiometer(channel=-1, device=0, ce=0, speed=1000000)</code> : Potentiometer object inheriting from [SpiAdc Class](pop.md#class-spiadc)<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`channel` : ADC Channel.    
&emsp;&emsp;&emsp;`device` : SPI Interface Channel. Default 0. (in Raspberry Pi)    
&emsp;&emsp;&emsp;`ce` : The SPI_CE(or CS) number to which the slave is connected. Default 0.    
&emsp;&emsp;&emsp;`speed` : SPI Interface Clock Speed. Default 1000000(1MHz).    

<h4><b>Methods</b></h4>   
  
&emsp;<code class="code_accent">readAverage()</code> : return level from range table.   
&emsp;<code class="code_accent">getRangeTable()</code> : return range table.  
&emsp;<code class="code_accent">setRangeTable(table)</code> : Set potentiometer range table.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`table` : Table with 10 elements.    
&emsp;&emsp;&emsp;&emsp;ex) [48, 300, 700, 1090, 1540, 1945, 2320, 2715, 2980, 3040]

---

## <span class="title">Class</span> <span class="title_accent">**PiezoBuzzer**</span>    
<blockquote class="desc">PiezoBuzzer is controlled by Software PWM.<br>
This class is used in AIoT Home, PyCBasic, SensorPack option.</blockquote><br> 

<h4><b>Initialization</b></h4>   

&emsp;<code class="code_accent">PiezoBuzzer(n)</code> : PiezoBuzzer object inheriting from PopThread<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`n` : A GPIO number connected to the PiezoBuzzer defined in board, or it can be manually set.    

<h4><b>Methods</b></h4>   

&emsp;<code class="code_accent">isPlay()</code> : Return play status.  
&emsp;<code class="code_accent">getTempo()</code> : Get tempo value.  
&emsp;<code class="code_accent">setTempo(n)</code> : Set tempo value.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`n` : Value to be set to tempo.

&emsp;<code class="code_accent">tone(scale,pitch,duration)</code> : Play a note on piezo buzzer during duration value.    <br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`scale` : Scale value to play on piezo buzzer (int type).    
&emsp;&emsp;&emsp;`pitch` : Pitch value to play on piezo buzzer. 'Do' is 1, 'Do♯' is 2, 'Re' is 3 and 'Si' is 12.    
&emsp;&emsp;&emsp;`duration` : Tone is playing during duration value.

&emsp;<code class="code_accent">rest(duration)</code> : Stop to play piezo buzzer.    <br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`duration` : The duration of the stopping.

&emsp;<code class="code_accent">play(sheet)</code> : Play music by sheet.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`sheet` : list [[scale],[pitch],[duration]].

<h4><b>Example</b></h4>

<details>
	<summary>simple example 1</summary>

~~~python
from pop import PiezoBuzzer
p = PiezoBuzzer(12)

p.tone(4, 8, 4)
~~~

</details>	

<details>
	<summary>simple example 2</summary>

~~~python
from pop import PiezoBuzzer
p = PiezoBuzzer(12)

p.setTempo(120)

butterfly_scale = [4,4,4, 4,4,4, 4,4,4,4, 4,4,4,  4,4,4,4, 4,4,4, 4,4,4,4, 4,4,4]
butterfly_pitch = [8,5,5, 6,3,3, 1,3,5,6, 8,8,8,  8,5,5,5, 6,3,3, 1,5,8,8, 5,5,5]
butterfly_duration = [8,8,4, 8,8,4, 8,8,8,8, 8,8,4,  8,8,8,8, 8,8,4, 8,8,8,8, 8,8,4]
sheet_butterfly = [butterfly_scale, butterfly_pitch, butterfly_duration]

p.play(sheet_butterfly)
~~~

</details>	
<br>

---

## <span class="title">Class</span> <span class="title_accent">**PixelDisplay**</span>    
<blockquote class="desc">Pixel Display is controlled by Hardware PWM.<br>
This class is used in PyCBasic, SensorPack option.</blockquote><br> 
  
<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">PixelDisplay(width=8, height=8, gpio=-1, type=GRB, dma=10, automode=True, debug=False)</code> : PixelDisplay object    
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`width` : Number of pixel width.    
&emsp;&emsp;&emsp;`height` : Number of pixel height.    
&emsp;&emsp;&emsp;`automode` : Automode setting. `True` or `False`.    

<h4><b>Methods</b></h4>  

&emsp;<code class="code_accent">display()</code> : Send command from buffer when Automode is `False`, this is not executed and the command is automaically sent when Automode is `True`.     
&emsp;<code class="code_accent">getRGBType()</code>: Get the RGB Type.    
&emsp;<code class="code_accent">RGBtoHEX(color_arr)</code> : Convert the RGB list data to HEX.  
&emsp;<code class="code_accent">clear()</code> : Clear Pixel Display.  
&emsp;<code class="code_accent">rainbow()</code> : Display rainbow color on Pixel Display.  
&emsp;<code class="code_accent">fill(color_arr)</code> : Fill Pixel Display with one color.    
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`color_arr` : A color to be filled. Type is list of [R, G, B].  
   
&emsp;<code class="code_accent">setColor(x, y, color_arr)</code> : Set Pixel Display color_arr on x,y.    
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`x` : x-axis.    
&emsp;&emsp;&emsp;`y` : y-axis.    
&emsp;&emsp;&emsp;`color_arr` : A color to be set. Type is list of [R, G, B] or HEX (0xRRGGBB).    

&emsp;<code class="code_accent">getColor(x, y)</code> : Return color on x,y as INT type.    
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`x` : x-axis.    
&emsp;&emsp;&emsp;`y` : y-axis. 

&emsp;<code class="code_accent">setAutomode(automode)</code> : Set automode. Default `True`. If `False` set, display() should be used.    
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`automode` : `True` or `False`.    
   
&emsp;<code class="code_accent">setBrightness(brightness)</code> : Set Brightness.    
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`brightness` : Brightness (0~255).    
  
&emsp;<code class="code_accent">setColorInvert(invert)</code> : Invert the color. Default `False`.    
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`invert`  
&emsp;&emsp;&emsp;&emsp;`True` : input (255,0,0) -> (0,255,255).    
&emsp;&emsp;&emsp;&emsp;`False` : input (255,0,0) -> (255,0,0).    

<h4><b>Example</b></h4>

<details>
	<summary>simple example</summary>

~~~python
from pop import PixelDisplay
import time 

display = PixelDisplay()

display.setColor(0, 0, [5, 0, 0])
time.sleep(1)
display.fill([5, 0, 0])
time.sleep(1)
~~~

</details>
<br>

---

## <span class="title">Class</span> <span class="title_accent">**Dust**</span>   
<blockquote class="desc">dust measurement using Dust sensor.<br>
This class is used in AIoT Home, AIoT Server Plus, SensorPack option.</blockquote><br>   

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">Dust(addr)</code> : Dust object<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`addr` : I2c slave address. default 0x28.

<h4><b>Methods</b></h4>  

&emsp;<code class="code_accent">reset()</code> : Software reset for Dust Sensor.     

&emsp;<code class="code_accent">read()</code> : Read all sensor data that can be read by the dust sensor.  

&emsp;**Variables**    
&emsp;<code class="code_accent">pm_1p0_grimm</code> : Fine dust data read pm1.0 by grimm.    
&emsp;<code class="code_accent">pm_2p5_grimm</code> : Fine dust data read pm2.5 by grimm.   
&emsp;<code class="code_accent">pm_10_grimm</code> : Fine dust data read pm10 by grimm.   
&emsp;<code class="code_accent">pm_1p0_tsi</code> : Fine dust data read pm1.0 by tsi.    
&emsp;<code class="code_accent">pm_2p5_tsi</code> : Fine dust data read pm2.5 by tsi.   
&emsp;<code class="code_accent">pm_10_tsi</code> : Fine dust data read pm10 by tsi.   

<h4><b>Example</b></h4>

<details>
	<summary>simple example</summary>

~~~python
from pop import Dust
import time 

dust = Dust()
while True:
	dust.read()
	print("PM 1.0 GRIM  : %u ㎍/㎥"%dust.pm_1p0_grimm)
	print("PM 2.5 GRIM  : %u ㎍/㎥"%dust.pm_2p5_grimm)
	print("PM 10  GRIM  : %u ㎍/㎥"%dust.pm_10_grimm)
	time.sleep(0.5)
~~~

</details>
<br>

---

## <span class="title">Class</span> <span class="title_accent">**PwmController**</span>    
<blockquote class="desc">I2C communication allows PWM signals to be generated by issuing control commands to the PWM control module, specifying the desired frequency and desired duty cycle for each outputable channel.<br>
This class is used in AIoT Home, AI Mavin, SensorPack option.</blockquote><br>   

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">PwmController(addr)</code> : PwmController object <br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`addr` : I2c slave address. default 0x5e.   

<h4><b>Methods</b></h4>  

&emsp;<code class="code_accent">init()</code> : initialize PwmController.<br>

&emsp;<code class="code_accent">setChannel(channel)</code> : Set the PWM Channel for control.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`channel` : channel value. (0 ~ 15)    

&emsp;<code class="code_accent">setDuty(percent)</code> : Specifies the duty cycle of pwm.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`percent` : Specifies the duty ratio as a percentage. (0 ~ 100)    

&emsp;<code class="code_accent">setFreq(freq)</code> : Specifies the pwm frequency.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`freq` : Frequency. ex) 50 -> 50Hz     

&emsp;<code class="code_accent">setInvertPulse()</code> : Invert the output PWM signal.  

<h4><b>Example</b></h4>

<details>
	<summary>simple example</summary>

~~~python
from pop import PwmController
import time

pwm = PwmController()
pwm.init()
pwm.setChannel(0)
pwm.setFreq(50)
for i in range(10):
	pwm.setDuty(i*10)
	time.sleep(0.5)
~~~

</details>
<br>

---

## <span class="title">Class</span> <span class="title_accent">**Audio**</span>    
<br>

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">Audio(blocking=True, cont=False)</code> : Audio object<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`blocking` : If `True`, working in blocking mode. Else non-blocking mode. Default is `True`.    
&emsp;&emsp;&emsp;`cont` : If `True`, repeat playing file. Else play one time. This is working in only non-blocking mode. Default is `False`.    

<h4><b>Methods</b></h4>

&emsp;<code class="code_accent">stop()</code> : Stop playing if in non-blocking mode. This method is used in subclass like 'AudioPlay'.    
&emsp;<code class="code_accent">close()</code> : Clear audio resources explicitly. This method is used in subclass like 'AudioPlay'.    

<br>

---

## <span class="title">Class</span> <span class="title_accent">**AudioPlay**</span>    
<br>

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">AudioPlay(file, blocking=True, cont=False)</code> : AudioPlay object<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`file` : Name of WAV file to play.    
&emsp;&emsp;&emsp;`blocking` : If `True`, working in blocking mode. Else non-blocking mode. Default is `True`.    
&emsp;&emsp;&emsp;`cont` : If `True`, repeat playing file. Else play one time. This is working in only non-blocking mode. Default is `False`.    

<h4><b>Methods</b></h4>

&emsp;<code class="code_accent">run()</code> : Start playing the file.    
&emsp;<code class="code_accent">isPlay()</code> : Return playing status. True means playing now, False means stopped.    

<h4><b>Example</b></h4> 

<details>
	<summary>simple example</summary>

~~~python
from pop import AudioPlay
import time 

with AudioPlay("/usr/share/sounds/alsa/Side_Left.wav", False, True) as play:   
	play.run()
	print("Start Play...")
	for _ in range(12):  
		time.sleep(1)

	play.stop()
	print("Stop play...")
~~~

</details>
<br>

---

## <span class="title">Class</span> <span class="title_accent">**AudioPlayList**</span>    
<br>

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">AudioPlayList(files, blocking=True, cont=False)</code> : AudioPlayList object<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`files` : Names of WAV file to play. (list type)    
&emsp;&emsp;&emsp;`blocking` : If `True`, working in blocking mode. Else non-blocking mode. Default is `True`.    
&emsp;&emsp;&emsp;`cont` : If `True`, repeat playing file. Else play one time. This is working in only non-blocking mode. Default is `False`.    

<h4><b>Methods</b></h4> 

&emsp;<code class="code_accent">isPlay()</code> : Return playing status. `True` means playing now, `False` means stopped.    
&emsp;<code class="code_accent">run(pos=0)</code> : Start playing the file.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`pos` : Index of WAV file in playing list. Default is 0.    

<h4><b>Example</b></h4>

<details>
	<summary>simple example</summary>

~~~python
from pop import AudioPlayList
import time 

playlist = ["/usr/share/sounds/alsa/Front_Center.wav", "/usr/share/sounds/alsa/Side_Left.wav", "/usr/share/sounds/alsa/Side_Right.wav"]

with AudioPlayList(playlist) as play:
	print("Start PlayList...") 
	play.run()
~~~

</details>
<br>

---

## <span class="title">Class</span> <span class="title_accent">**AudioRecord**</span>    
<br>

<h4><b>Initialization</b></h4>
&emsp;<code class="code_accent">AudioRecord(file, sFormat=8, sChannel=1, sRate=48000, sFramePerBuffer=1024)</code> : AudioRecord object. Only non-blocking mode is supported.<br>

&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`file` : Name of WAV file to save.    
&emsp;&emsp;&emsp;`sFormat` : Sampling type. 8 is paInt16, 2 is paInt32, 1 is pa Float32. Default is 8. (int type)    
&emsp;&emsp;&emsp;`sChannel` : Number of channel. Default is 1.    
&emsp;&emsp;&emsp;`sRate` : Sampling rate(Hz). Default is 48000.    
&emsp;&emsp;&emsp;`sFramePerBuffer` : Frame per buffer. Default 1024.    

<h4><b>Methods</b></h4>   

&emsp;<code class="code_accent">run()</code> : Start recording.   

<h4><b>Example</b></h4>

<details>
	<summary>simple example</summary>

~~~python
from pop import AudioRecord
import time 

with AudioRecord("my_record.wav") as record:
	record.run()
	print("Start Recording...") 

	for _ in range(5):
		time.sleep(1)

	record.stop()
	print("Stop Recording...") 
~~~

</details>
<br>

---

## <span class="title">Class</span> <span class="title_accent">**Tone**</span>    
<br>

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">Tone(tempo=100, volume=.5, rate=48000, channels=1)</code> : Tone object<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`tempo` : Tempo of melody. Default is 100.    
&emsp;&emsp;&emsp;`volume` : Volume of meldy. Default is 0.5. (0 ~ 1)    
&emsp;&emsp;&emsp;`rate` : Sampling rate(Hz). Default is 48000.    
&emsp;&emsp;&emsp;`channels` : Number of channels. Default is 1.    

<h4><b>Methods</b></h4>  

&emsp;<code class="code_accent">close()</code> : Clear audio resources explicitly.<br>
&emsp;<code class="code_accent">setTempo(tempo)</code> : Set the tempo of melody.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`tempo` : Value of tempo.<br> 
&emsp;<code class="code_accent">rest(duration)</code> : Intervals of silence.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`duration` : Duration of silence. (4, 2, 1, 1/2, 1/4, ...)<br>
&emsp;<code class="code_accent">play(octave, pitch, duration)</code> : Play the melody.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`octave` : Octave of melody. (1 ~ 8)    
&emsp;&emsp;&emsp;`pitch` : Pitch of melody. ("DO", "DO#", "RE", "RE#", "MI", "FA", "SOL", "SOL#", "RA", "RA#", "SI")    
&emsp;&emsp;&emsp;`duration` : Duration of melody.    

<h4><b>Example</b></h4>  

<details>
	<summary>simple example1</summary>

~~~python
from pop import Tone
import time 

with Tone() as tone:
	for n in [1, 3, 5, 7, 8, 10, 12]:
		tone.play(3, n, 4)
~~~

</details>

<details>
	<summary>simple example2</summary>

~~~python
from pop import Tone

schoolBell1 = ((4, "SOL", 1/4), (4, "SOL", 1/4), (4, "RA", 1/4), (4, "RA", 1/4), (4, "SOL", 1/4), (4, "SOL", 1/4), (4, "MI", 1/2), (4, "SOL", 1/4), (4, "SOL", 1/4), (4, "MI", 1/4), (4, "MI", 1/4), (4, "RE", 1/2 + 1/4))
schoolBell2 = (*schoolBell1[:7], (4, "SOL", 1/4), (4, "MI", 1/4), (4, "RE", 1/4), (4, "MI", 1/4), (4, "DO", 1/2 + 1/4))

with Tone() as tone:
	tone.setTempo(200)

	for n in schoolBell1:
		tone.play(*n)
	tone.rest(1/4)

	for n in schoolBell2:
		tone.play(*n)
	tone.rest(1/4)
~~~

</details>
<br>

---

## <span class="title">Class</span> <span class="title_accent">**SoundMeter**</span>    
<br>

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">SoundMeter(sampleFormat=pyaudio.paInt16, channelNums=1, framesPerBuffer=1024, sampleRate=48000)</code> : SoundMeter object<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`sampleFormat` : Sampling type. Default is pyaudio.paInt16.    
&emsp;&emsp;&emsp;`channelNums` : Number of channel. Default is 1.    
&emsp;&emsp;&emsp;`framesPerBuffer` : Frame per buffer. Default 1024.    
&emsp;&emsp;&emsp;`sampleRate` : Sampling rate(Hz). Default is 48000.    

<h4><b>Methods</b></h4>  

&emsp;<code class="code_accent">stop()</code> : Stop measurement and clear audio resources explicitly.    
&emsp;<code class="code_accent">setCallback(func, *args)</code> : Set user callback method and start measurement.<br>
&emsp;&emsp;**Params**   
&emsp;&emsp;&emsp;`func` : User callback method.    
&emsp;&emsp;&emsp;`*args` : Argument to be conveyed to user callback method. (skippable)    

<h4><b>Example</b></h4>  

<details>
	<summary>simple example</summary>

~~~python
import time
from pop import SoundMeter

sm = SoundMeter()

def onSoundMeter(rms, inData):
	if(rms>600):
		print(rms)

sm.setCallback(onSoundMeter)

input("input something")

sm.stop()
~~~

</details>
<br>
