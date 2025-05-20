# IMAGE-TRANSFORMATIONS
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules
<br>

### Step2:
Choose an image and save it as filename.jpg
<br>

### Step3:
Use imread to read the image
<br>

### Step4:
Use cv2.warpPerspective(image,M,(cols,rows)) to translation the image
<br>

### Step5:
Use cv2.warpPerspective(image,M,(cols2,rows2)) to scale the image
<br>

## Program:

Developed By:Himavath M
Register Number:212223240053

i)Image Translation
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread("/content/bird.png")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim=input_image.shape
M=np.float32([[1,0,100],[0,1,200],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
print("Image Translation:")
plt.imshow(translated_image)
plt.show()
```

ii) Image Scaling

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('/content/bird.png')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim=input_image.shape
M=np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
print("Image Scaling:")
plt.imshow(translated_image)
plt.show()
```
iii)Image shearing
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('/content/bird.png')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim=input_image.shape
M1=np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M2=np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols*1.5),int(rows*1.5)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
print("Image Shearing:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()
````
iv)Image Reflection
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim=input_image.shape
M1=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M2=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols),int(rows)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols),int(rows)))
plt.axis('off')
print("Image Reflection:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()

```
v)Image Rotation
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim=input_image.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
print("Image Rotation:")
plt.imshow(translated_image)
plt.show()
```
vi)Image Cropping
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("/content/bird.png")
h, w, _ = image.shape
cropped_face = image[int(h*0.2):int(h*0.8), int(w*0.3):int(w*0.7)]
cv2.imwrite("cropped_pigeon_face.jpg", cropped_face)
plt.imshow(cv2.cvtColor(cropped_face, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()


```
## Output:
### i)Image Translation
![image](https://github.com/user-attachments/assets/8d8008cb-fb2d-413e-a832-5264742f4f39)

### ii) Image Scaling
![image](https://github.com/user-attachments/assets/7ab21581-7ad8-4429-a603-e6d30d2f953a)

### iii)Image shearing
![image](https://github.com/user-attachments/assets/9acbba3b-501a-4aad-8a5b-58e005ef601e)

### iv)Image Reflection
![image](https://github.com/user-attachments/assets/cdedcd7b-6501-4462-b8e8-658b402cb7c8)

### v)Image Rotation
![image](https://github.com/user-attachments/assets/6df0a6ce-c1ff-4660-8fca-d6b3b94d3514)


### vi)Image Cropping
![image](https://github.com/user-attachments/assets/433538f6-b297-48de-b835-a584ec8c785b)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
