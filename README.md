# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
Step1:
Import the necessary libraries and read the original image and save it as a image variable.

Step2:

Translate the image using M=np.float32([[1,0,20],[0,1,50],[0,0,1]]) translated_img=cv2.warpPerspective(input_img,M,(cols,rows))??

Step3:

Scale the image using M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]]) scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))?

Step4:

Shear the image using M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]]) sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

Step5:

Reflection of image can be achieved through the code M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]]) reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

Step6:

Rotate the image using angle=np.radians(45) M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]]) rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))

Step7:

Crop the image using cropped_img=input_img[20:150,60:230]

Step8:

Display all the Transformed images and end the program.

## Program:

Developed By:G.Jayanth
Register Number:212221230030

##  )Image Translation

import numpy as np
import cv2
import matplotlib.pyplot as plt
inputImage=cv2.imread("sachin.png")
inputImage=cv2.cvtColor(inputImage, cv2.COLOR_BGR2RGB)
plt.axis("off")
plt.imshow(inputImage)
plt.show()
rows, cols, dim = inputImage.shape
M= np.float32([[1, 0, 100],
                [0, 1, 200],
                 [0, 0, 1]])
translatedImage =cv2.warpPerspective (inputImage, M, (cols, rows))
plt.imshow(translatedImage)
plt.show()


## ii) Image Scaling

rows, cols, dim = inputImage.shape
M = np. float32 ([[1.5, 0 ,0],
                 [0, 1.8, 0],
                  [0, 0, 1]])
scaledImage=cv2.warpPerspective(inputImage, M, (cols * 2, rows * 2))
plt.imshow(scaledImage)
plt.show()



## iii)Image shearing

matrixX = np.float32([[1, 0.5, 0],
                      [0, 1 ,0],
                      [0, 0, 1]])

matrixY = np.float32([[1, 0, 0],
                      [0.5, 1, 0],
                      [0, 0, 1]])
shearedXaxis = cv2.warpPerspective (inputImage, matrixX, (int(cols * 1.5), int (rows * 1.5)))
shearedYaxis = cv2.warpPerspective (inputImage, matrixY, (int (cols * 1.5), int (rows * 1.5)))
plt.imshow(shearedXaxis)
plt.show()
plt.imshow(shearedYaxis)
plt.show()
```



## iv)Image Reflection
```
matrixx=np.float32([[1, 0, 0],
                    [0,-1,rows],
                    [0,0,1]])
matrixy=np.float32([[-1, 0, cols],
                    [0,1,0],
                    [0,0,1]])
reflectedX=cv2.warpPerspective(inputImage, matrixx, (cols, rows))
reflectedY=cv2.warpPerspective(inputImage, matrixy, (cols, rows))
plt.imshow(reflectedY)
plt.show()



```
## v)Image Rotation
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
angle=np.radians(45)
inputImage=cv2.imread("sachin.png")
rows, cols, dim = inputImage.shape
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotatedImage = cv2.warpPerspective(inputImage,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotatedImage)
plt.show()
```

## vi)Image Cropping
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
angle=np.radians(45)
inputImage=cv2.imread("sachin.png")
CroppedImage= inputImage[20:150, 60:230]
plt.axis('off')
plt.imshow(CroppedImage)
plt.show()
```





## Output:
### i)Image Translation

<img width="387" alt="Screenshot 2023-09-13 131242" src="https://github.com/JayanthYadav123/IMAGETRANSFORMATION/assets/94836154/31b2b995-db35-44ff-8eb9-4e17eaf4afda">

### ii) Image Scaling
<img width="481" alt="2" src="https://github.com/JayanthYadav123/IMAGETRANSFORMATION/assets/94836154/9d483850-cfea-4d0d-80a5-92b98c8e1f40">



### iii)Image shearing

<img width="458" alt="3" src="https://github.com/JayanthYadav123/IMAGETRANSFORMATION/assets/94836154/90915e25-ef88-4e07-83b6-59e7515a18b2">

<img width="440" alt="3 1" src="https://github.com/JayanthYadav123/IMAGETRANSFORMATION/assets/94836154/8c4a4542-0f38-4df0-a26f-b538c4d908d0">


### iv)Image Reflection

<img width="434" alt="4" src="https://github.com/JayanthYadav123/IMAGETRANSFORMATION/assets/94836154/66a3dc48-3542-4ac4-b4ea-589d88fa2f2c">

### v)Image Rotation

<img width="401" alt="5" src="https://github.com/JayanthYadav123/IMAGETRANSFORMATION/assets/94836154/009fccd5-c9e1-47ac-957d-ad85eb8e0564">

### vi)Image Cropping

<img width="389" alt="6" src="https://github.com/JayanthYadav123/IMAGETRANSFORMATION/assets/94836154/b4a88958-a527-4cd5-89d9-21879bf08673">





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
