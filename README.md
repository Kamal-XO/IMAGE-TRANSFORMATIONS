# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>Import the necessary libraries and read the original image and save it as a image variable.



### Step2:
<br>Translate the image using a function warpPerpective()



### Step3:
<br>Scale the image by multiplying the rows and columns with a float value.



### Step4:
<br>Shear the image in both the rows and columns.



### Step5:
<br>Find the reflection of the image.



## Program:
```
Developed By: Kamalesh SV
Register Number: 212222240041
```
i)Image Translation

```
import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("/content/BIRD.webp")
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,50],  [0,1,100],  [0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
ii) Image Scaling
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("/content/color.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```


iii)Image shearing
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("/content/BIRD.webp")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()
```


iv)Image Reflection
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("/content/color.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()

```



v)Image Rotation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("/content/color.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```



vi)Image Cropping

```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("/content/BIRD.webp")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()


```
## Output:
### i)Image Translation


<br>![Screenshot 2024-03-19 113656](https://github.com/Aravindsamy04/IMAGE-TRANSFORMATIONS/assets/113497037/28adcf8c-3554-4249-8bad-ba649d2693fe)

<br>

### ii) Image Scaling
<br>

<br>![Screenshot 2024-03-19 113748](https://github.com/Aravindsamy04/IMAGE-TRANSFORMATIONS/assets/113497037/b6bbb61f-c759-470c-86c4-cda0b9c4cc27)



### iii)Image shearing

<br>![Screenshot 2024-03-19 113844](https://github.com/Aravindsamy04/IMAGE-TRANSFORMATIONS/assets/113497037/157b95cd-fea1-4e71-9a21-89f7c9fb203b)
<br>![Screenshot 2024-03-19 113856](https://github.com/Aravindsamy04/IMAGE-TRANSFORMATIONS/assets/113497037/9d7817b7-dd48-4403-a1fd-6fe9d6baa6bc)

<br>


### iv)Image Reflection
<br>![Screenshot 2024-03-19 113944](https://github.com/Aravindsamy04/IMAGE-TRANSFORMATIONS/assets/113497037/2f4aa893-bcc4-4ddf-b69c-0afae06087bc)

<br>![Screenshot 2024-03-19 113956](https://github.com/Aravindsamy04/IMAGE-TRANSFORMATIONS/assets/113497037/4bb115d4-b866-4710-b0b1-e1c8be4ee3c5)

<br>


### v)Image Rotation
<br>![Screenshot 2024-03-19 113327](https://github.com/Aravindsamy04/IMAGE-TRANSFORMATIONS/assets/113497037/710574d6-4120-4ac3-a5b5-1af2ad9b4ed3)

<br>![Screenshot 2024-03-19 113340](https://github.com/Aravindsamy04/IMAGE-TRANSFORMATIONS/assets/113497037/2dd01d96-7561-46f0-85ac-2cbb8a08d70b)
<br>
<br>



### vi)Image Cropping
<br>![Screenshot 2024-03-19 114602](https://github.com/Aravindsamy04/IMAGE-TRANSFORMATIONS/assets/113497037/609b5886-f3bf-47ae-99ac-b1dbf78a3221)



<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
