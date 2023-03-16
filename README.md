# READ AND WRITE AN IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.
i) Read, display, and write an image.
ii) Access the rows and columns in an image.
iii) Cut and paste a small portion of the image.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
## Program:
### Developed By: MITTA BHAVISHYA REDDY
### Register Number: 212221230061

i) #To Read,display the image
```
import cv2
from google.colab.patches import cv2_imshow
a = cv2.imread('/content/sealink.jpg',1)
cv2_imshow(a)
cv2.waitKey(0) 
```
ii) #To write the image
```
colorImage = cv2.imread('/content/sealink.jpg',1)
cv2.imwrite('written.jpg',colorImage)
writtenImage = cv2.imread('written.jpg',1)
cv2_imshow(writtenImage)
cv2.waitKey(0)
```
iii) #Find the shape of the Image
```
colorImage = cv2.imread('/content/sealink.jpg',1)
print(colorImage.shape)
```
iv) #To access rows and columns
```
import random
colorImage = cv2.imread('/content/written.jpg',1)
for i in range(100):
    for j in range(colorImage.shape[1]):
        colorImage[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)]
cv2_imshow(colorImage)
cv2.waitKey(0)
```
v) #To cut and paste portion of image
```
color_img = cv2.imread('/content/written.jpg',1)
tag = color_img[200:400,300:500]
color_img[200:400,100:300] = tag
cv2_imshow(color_img)
cv2.waitKey(0)
```

## Output:

### i) Read and display the image
![image](https://user-images.githubusercontent.com/94679395/225554457-25c4843a-da6a-46a0-a413-11b7d9308c9f.png)


### ii)Write the image
![image](https://user-images.githubusercontent.com/94679395/225554489-1e54c6d4-e546-4ed8-8554-c4d9e28cd230.png)


### iii)Shape of the Image
<img width="280" alt="image" src="https://user-images.githubusercontent.com/94679395/225554616-56e19544-ffba-4c70-b03a-f79eb2f665ad.png">


### iv)Access rows and columns
![image](https://user-images.githubusercontent.com/94679395/225554671-8fcb57e2-415c-4967-96f1-c9aeee831740.png)


### v)Cut and paste portion of image
![image](https://user-images.githubusercontent.com/94679395/225554719-f83dfa3e-4945-48f7-a1cd-dce3e37b66df.png)


## Result:
Thus the images are read, displayed, and written successfully using the python program.


