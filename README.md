# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 library and upload the image or capture an image.

### Step2:
Read the saved image using cv2.imread("filename.jpg").

### Step3:
Convert the image into the given color transformation using cv2.cvtColor(image, cv2.BGR2YCrCb) and similarly for other color formats.

### Step4:
Split and merge the image using cv2.split(hsv) and cv2.merge([h,s,v])
### Step5:
Output the image using cv2.imshow("OUTPUT", image)
## Program:
```
Developed By:Mourise jane
Register Number:212222230085
```
# i) Convert BGR and RGB to HSV and GRAY
## BGR TO HSV
```
import cv2
image =cv2.imread('N-1.PNG')
cv2.imshow('original',image)
b_h=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR_HSV',b_h)
cv2.waitKey(0)
cv2.destroyAllWindows
```
## BGR TO GRAY
```
import cv2
image =cv2.imread('N-1.PNG')
cv2.imshow('original',image)
r_h=cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB_HSV',r_h)
cv2.waitKey(0)
cv2.destroyAllWindows
```
## RGB TO HSV
```
import cv2
image =cv2.imread('N-1.PNG')
cv2.imshow('original',image)
r_g=cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB_GRAY',r_g)
cv2.waitKey(0)
cv2.destroyAllWindows
```
## RGB TO GRAY
```
import cv2
image =cv2.imread('N-1.PNG')
cv2.imshow('original',image)
b_g=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR_GRAY',b_g)
cv2.waitKey(0)
cv2.destroyAllWindows
```
```

import cv2
img= cv2.imread('N-2.PNG')
hsv=cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imwrite('hsv-n1.png',hsv)
```

# ii)Convert HSV to RGB and BGR
## HSV TO RGB
```
import cv2
ori=cv2.imread('hsv-n1.png')
cv2.imshow('Original',ori)
h_r=cv2.cvtColor(ori,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV_RGB',h_r)
cv2.waitKey(0)
cv2.destroyAllWindows
```
## HSV TO BGR
```
import cv2
ori=cv2.imread('hsv-n1.png')
cv2.imshow('Original',ori)
h_b=cv2.cvtColor(ori,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV_BGR',h_b)
cv2.waitKey(0)
cv2.destroyAllWindows
```


# iii)Convert RGB and BGR to YCrCb
## RGB TO YCrCb
```
import cv2
ori=cv2.imread('N-3.PNG')
YCrCb_image = cv2.cvtColor(ori, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB_YCRCB',YCrCb_image)
cv2.waitKey(0)
cv2.destroyAllWindows
```
## BGR TO YCrCb
```
import cv2
image1=cv2.imread('N-3.PNG')
YCrCb_image = cv2.cvtColor(image1, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR_YCRCB',YCrCb_image)
cv2.waitKey(0)
cv2.destroyAllWindows
```

# iv)Split and Merge RGB Image
```
import cv2
img = cv2.imread("N-1.PNG")
img1= cv2.resize(img, (270,190))
cv2
b,g,r = cv2.split(img1)
cv2.imshow("RED MODEL", r)
cv2.imshow("GREEN MODEL", g)
cv2.imshow("BLUE MODEL ", b)
merger = cv2.merge([b,g,r])
cv2.imshow("MERGED IMAGE", merger )
cv2.waitKey(0)
cv2.destroyAllWindows()
```



# v) Split and merge HSV Image
```
import cv2
img = cv2.imread("N-2.PNG")
img1= cv2.resize(img, (270,190))
hsv = cv2.cvtColor(img1 , cv2.COLOR_BGR2HSV)
cv2.imshow("INITIAL_HSV ", hsv)
h,s,v = cv2.split(hsv)
cv2.imshow("RED MODEL", h)
cv2.imshow("GREEN MODEL", s)
cv2.imshow("BLUE MODEL ", v)
merger = cv2.merge([h,s,v])
cv2.imshow("MERGED IMAGE", merger )
cv2.waitKey(0)
cv2.destroyAllWindows()



```
## Output:
### i) BGR and RGB to HSV and GRAY
![OP-1(3)](https://github.com/MOHAMED-FAREED-22001617/COLOR-CONVERSION/assets/121412904/a11edc7c-bfe9-4ba7-b4e4-5bef152006fa)
![OP-2](https://github.com/MOHAMED-FAREED-22001617/COLOR-CONVERSION/assets/121412904/c5f4aa65-567c-4770-bd8c-196759b94cba)
![OP-3](https://github.com/MOHAMED-FAREED-22001617/COLOR-CONVERSION/assets/121412904/74aede14-2da2-43c9-8a97-b5860b52be3d)
![OP-4](https://github.com/MOHAMED-FAREED-22001617/COLOR-CONVERSION/assets/121412904/5da6d14f-ba9f-40f0-a0c4-d081f3421eec)


### ii) HSV to RGB and BGR
![OUT-5](https://github.com/MOHAMED-FAREED-22001617/COLOR-CONVERSION/assets/121412904/a63ceedb-ae1f-4c4a-bf66-85108e9c8e5d)
![OUT-6](https://github.com/MOHAMED-FAREED-22001617/COLOR-CONVERSION/assets/121412904/95a73533-de0c-47d8-88fc-ad81685b0324)


### iii) RGB and BGR to YCrCb
![OP-07](https://github.com/MOHAMED-FAREED-22001617/COLOR-CONVERSION/assets/121412904/bab711d4-ebf9-4ffd-8134-9e1dc784e971)
![OP-08](https://github.com/MOHAMED-FAREED-22001617/COLOR-CONVERSION/assets/121412904/b34eebc1-79e9-4192-8b6a-bb7811af7dec)



### iv) Split and merge RGB Image
![OUTP-09](https://github.com/MOHAMED-FAREED-22001617/COLOR-CONVERSION/assets/121412904/42d30783-4205-4830-b7df-f98e11048b68)


### v) Split and merge HSV Image
![OUTP-10](https://github.com/MOHAMED-FAREED-22001617/COLOR-CONVERSION/assets/121412904/75f87c50-af48-4e62-a512-f445d8c56d9f)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
