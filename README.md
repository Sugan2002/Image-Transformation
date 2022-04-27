### Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

### Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step1: 
Import the necessary libraries and read the original image and save it a image variable.
<br>
### Step2: 
Translate the image using Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]]) Translated_image=cv2.warpPerspective(org_img,Translation_matrix,(col,row))
<br>

### Step3: 
Scale the image using Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]]) Scaled_image=cv2.warpPerspective(org_img,Scaling_Matrix,(col,row))
<br>

### Step4: 
Shear the image using Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]]) Sheared_image=cv2.warpPerspective(org_img,Shearing_matrix,(col2,int(row1.5)))
<br>

### Step5: 
Reflection of image can be achieved through the code Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]]) Reflected_image_row=cv2.warpPerspective(org_img,Reflection_matrix_row,(col,int(row)))
<br>
### Step6:
Rotate the image using Rotation_angle=np.radians(10) Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0], [np.sin(Rotation_angle),np.cos(Rotation_angle),0], [0,0,1]]) Rotated_image=cv2.warpPerspective(org_img,Rotation_matrix,(col,(row)))

### Step7:
Crop the image using cropped_image=org_img[10:350,320:560]

### Step8: 
Display all the Transformed images.

## Program:
```python
Developed By   : P.SUGANYA
Register Number: 212220230049

i)Image Translation

import cv2
import numpy as np
import matplotlib.pyplot as plt
org_img=cv2.imread("image.jpeg")
org_img=cv2.cvtColor(org_img,cv2.COLOR_BGR2RGB)
plt.axis("off")
plt.imshow(org_img)
row,col,dim=org_img.shape

i)Image Translation
Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]])
Translated_image=cv2.warpPerspective(org_img,Translation_matrix,(col,row))
plt.axis("off")
plt.imshow(Translated_image)

ii) Image Scaling
Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])
Scaled_image=cv2.warpPerspective(org_img,Scaling_Matrix,(col,row))
plt.axis("off")
plt.imshow(Scaled_image)

iii)Image Shearing
Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]])
Sheared_image=cv2.warpPerspective(org_img,Shearing_matrix,(col*2,int(row*1.5)))
plt.axis("off")
plt.imshow(Sheared_image)

iv)Image Reflection
Reflection_matrix_col=np.float32([[-1,0,col],[0,1,0],[0,0,1]])
Reflected_image_col=cv2.warpPerspective(org_img,Reflection_matrix_col,(col,int(row)))
plt.axis("off")
plt.imshow(Reflected_image_col)
Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]])
Reflected_image_row=cv2.warpPerspective(org_img,Reflection_matrix_row,(col,int(row)))
plt.axis("off")
plt.imshow(Reflected_image_row)

v)Image Rotation
Rotation_angle=np.radians(10)
Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0],
                                [np.sin(Rotation_angle),np.cos(Rotation_angle),0],
                                [0,0,1]])
Rotated_image=cv2.warpPerspective(org_img,Rotation_matrix,(col,(row)))
plt.axis("off")
plt.imshow(Rotated_image)

vi)Image Cropping
cropped_image=org_img[10:350,320:560]
plt.axis("off")
plt.imshow(cropped_image)
```
## Output:
### i)Image Translation
![o2](https://user-images.githubusercontent.com/77089743/165481910-16a85deb-adff-41b8-a054-6fabb4933962.PNG)
<br>
<br>
<br>
<br>

### ii) Image Scaling
### ii)Image Scaling
![o3](https://user-images.githubusercontent.com/77089743/165481954-96d410d2-aa29-4a84-a441-97a960cbf75f.PNG)
<br>
<br>
<br>
<br>


### iii)Image shearing
![o4](https://user-images.githubusercontent.com/77089743/165482011-26deb33f-3113-4b6f-bec9-dafbd9c0dd3f.PNG)
<br>
<br>
<br>
<br>


### iv)Image Reflection
![o5](https://user-images.githubusercontent.com/77089743/165482061-fb543907-f6e3-4e81-8473-6a7e400cb16e.PNG)
<br>
<br>
<br>
@@ -83,6 +125,7 @@ vi)Image Cropping


### v)Image Rotation
![o6](https://user-images.githubusercontent.com/77089743/165482135-1f161f3f-8f94-41ed-9263-2a7a581de8fe.PNG)
<br>
<br>
<br>
@@ -91,6 +134,7 @@ vi)Image Cropping


### vi)Image Cropping
![o8](https://user-images.githubusercontent.com/77089743/165482212-325c85ef-3052-4b82-8f44-05e035b324f2.PNG)
<br>
<br>
<br>

### Result:
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
