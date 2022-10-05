<h1> Pop.Util </h1>
Pop.Util is an easy and fast training library for robot control.
<br><br>

<!-- # Class & Method Description-->
<hr/>

## <span class="title">Function</span> <span class="title_accent">**imshow**</span>   

The code to use the imshow method :

``` python
from pop.Util import imshow
```

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">imshow(title, image, width=300, height=300, mode='BGR')</code> : display image<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`title` : image title<br>
&emsp;&emsp;&emsp;`image` : image file name<br>
&emsp;&emsp;&emsp;`width` : width for show<br>
&emsp;&emsp;&emsp;`height` : height for show<br>
&emsp;&emsp;&emsp;`mode` : mode for show. ('BGR' or 'rgb')<br>

<br>

---

## <span class="title">Function</span> <span class="title_accent">**enable_imshow**</span>   

The code to use the enable_imshow method :

``` python
from pop.Util import enable_imshow
```

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">enable_imshow()</code> : enable imshow method<br>

<br>

---

## <span class="title">Function</span> <span class="title_accent">**toMFCC**</span>   

The code to use the toMFCC method :

``` python
from pop.Util import toMFCC
```

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">toMFCC(file_path, duration=1., rate=8000)</code> : Convert to MFCC data<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`file_path` : Path of the file that convert to MFCC data<br>
&emsp;&emsp;&emsp;`duration` : Duration of the file<br>
&emsp;&emsp;&emsp;`rate` : Rate of the file<br>

<br>

---

## <span class="title">Function</span> <span class="title_accent">**one_hot**</span>   

The code to use the one_hot method :

``` python
from pop.Util import one_hot
```

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">one_hot(num, maxlen)</code> : one-hot encoding<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`num` : A Tensor of indices.<br>
&emsp;&emsp;&emsp;`maxlen` : A scalar defining the depth of the one hot dimension<br>

<br>

---

## <span class="title">Function</span> <span class="title_accent">**gstrmer**</span>   

The code to use the gstrmer method :

``` python
from pop.Util import gstrmer
```

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">gstrmer(width=640, height=480, fps=30, flip=0)</code> : Framework used to access the camera<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`width` : camera width. default 640<br>
&emsp;&emsp;&emsp;`height` : camera height. default 480<br>
&emsp;&emsp;&emsp;`fps` : frame per second. default 30<br>
&emsp;&emsp;&emsp;`flip` : image flip method. default 0<br>

<br>

---

## <span class="title">Function</span> <span class="title_accent">**createIMG**</span>   

The code to use the createIMG method :

``` python
from pop.Util import createIMG
```

<h4><b>Initialization</b></h4> 

&emsp;<code class="code_accent">createIMG(filename="img")</code> : Create image file<br>
&emsp;&emsp;**Params**    
&emsp;&emsp;&emsp;`filename` : Name of the file<br>
