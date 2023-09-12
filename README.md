# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
import the required file in the program

### Step2:
load the image file in the program

### Step3:
use the techiniques for Translation ,scaling,shearing,reflection,rotation and cropping using opeanCV and python


### Step4:
display the modified image output

### Step5:
end the program

## Program:
```
Developed By: sharmila A
Register Number: 212221230094

import cv2
import numpy as np
import matplotlib.pyplot as plt
img=cv2.imread('spi.jpg')
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(img)
plt.show()
rows,cols,dim=img.shape

i)Image Translation

m=np.float32([[1,0,100],[0,1,200],[0,0,1]])
t_img=cv2.warpPerspective(img,m,(cols,rows))
plt.axis('off')
plt.imshow(t_img)
plt.show()


ii) Image Scaling

n=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])
s_img=cv2.warpPerspective(img,n,(cols*2,rows*2))
plt.axis('off')
plt.imshow(s_img)


iii)Image shearing

o_x=np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
p_y=np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sh_x=cv2.warpPerspective(img,o_x,(int(cols*1.5),int(rows*1.5)))
sh_y=cv2.warpPerspective(img,p_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sh_x)
plt.imshow(sh_y)
plt.show()



iv)Image Reflection

rows,cols,dim=img.shape
q_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
q_y=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
r_img=cv2.warpPerspective(img,q_x,(int(cols),int(rows)))
r_img1=cv2.warpPerspective(img,q_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(r_img)
plt.show()
plt.imshow(r_img1)
plt.show()

v)Image Rotation

angle=np.radians(40)
r=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
ro=cv2.warpPerspective(img,r,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(ro)
plt.show()


vi)Image Cropping

c_img = img[120:600,120:600]
plt.axis('off')
plt.imshow(c_img)
plt.show()
```
## Output:
![WhatsApp Image 2023-09-12 at 12 11 13 PM](https://github.com/Sharmilasha/IMAGETRANSFORMATION/assets/94506182/031cdab4-184b-4253-80a2-c20fe2258447)

### i)Image Translation
![image](https://github.com/Sharmilasha/IMAGETRANSFORMATION/assets/94506182/71173ae8-fd39-4359-a8ac-8394c84ec5ab)


### ii) Image Scaling
![image](https://github.com/Sharmilasha/IMAGETRANSFORMATION/assets/94506182/b65d6b71-8b68-473f-a1f4-01ed87516e3d)


### iii)Image shearing
![image](https://github.com/Sharmilasha/IMAGETRANSFORMATION/assets/94506182/20dbdb84-e982-4ccd-80e9-6db6a0e19c69)



### iv)Image Reflection
![image](https://github.com/Sharmilasha/IMAGETRANSFORMATION/assets/94506182/27de7681-b557-4592-9313-1b6d06b540b9)



### v)Image Rotation
![image](https://github.com/Sharmilasha/IMAGETRANSFORMATION/assets/94506182/166f3fd3-849a-4a65-ab52-eb7dec29adca)




### vi)Image Cropping
![image](https://github.com/Sharmilasha/IMAGETRANSFORMATION/assets/94506182/9f24e37e-c217-4513-b068-03469743f724)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
