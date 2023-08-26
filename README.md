# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 and save an image as scolor.jpeg.

### Step2:
Use imread to read and display the image.

### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:
Split and merge the image using cv2.split and cv2.merge commands.


### Step5:
End the program and view the output image windows.

## Program:
```python
# Developed By:GURUMOORTHI R
# Register Number:212222230042
# READ AND DISPLAY THE IMAGE
import cv2
scolor=cv2.imread('aa.jpeg')
cv2.imshow('Original Image',scolor)
cv2.waitKey(0)
cv2.destroyAllWindows()

# i) Convert BGR and RGB to HSV and GRAY
#BGR2HSV
hsvimg=cv2.cvtColor(scolor,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsvimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#BGR2GRAY
grayimg=cv2.cvtColor(scolor,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',grayimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB2HSV
hsvimg2=cv2.cvtColor(scolor,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvimg2)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB2GRAY
grayimg2=cv2.cvtColor(scolor,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayimg2)
cv2.waitKey(0)
cv2.destroyAllWindows()


# ii)Convert HSV to RGB and BGR
#HSV TO RGB
rgbimg=cv2.cvtColor(scolor,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB',rgbimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#HSV TO BGR
bgrimg=cv2.cvtColor(scolor,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR',bgrimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iii)Convert RGB and BGR to YCrCb
#BGR TO YCrCb
ybgr=cv2.cvtColor(scolor,cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb',ybgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB TO YCrCb
yrgb=cv2.cvtColor(scolor,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb',yrgb)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iv)Split and Merge RGB Image
# SPLIT AND MERGE RGB IMAGE

blue=scolor[:,:,0]
green=scolor[:,:,1]
red=scolor[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()

# v) Split and merge HSV Image
# SPLIT AND MERGE HSV IMAGE
hsv = cv2.cvtColor(scolor, cv2.COLOR_BGR2HSV)
h,s,v=cv2.split(hsv)
cv2.imshow("Hue-image",h)
cv2.imshow("Saturation-image",s)
cv2.imshow("Gray-image",v)
Merged_HSV=cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()



```
## Output:
### i) BGR and RGB to HSV and GRAY

![WhatsApp Image 2023-08-26 at 12 57 51](https://github.com/gururamu08/COLOR-CONVERSION/assets/118707009/0a62d499-a1cf-4090-8a28-4c621653e7b9)

![WhatsApp Image 2023-08-26 at 12 57 50](https://github.com/gururamu08/COLOR-CONVERSION/assets/118707009/cd9ad2ec-5f47-4882-8d90-561c4fbe990c)

![WhatsApp Image 2023-08-26 at 12 57 56](https://github.com/gururamu08/COLOR-CONVERSION/assets/118707009/cb4c7e59-402f-40ae-b48e-765391a68213)

![WhatsApp Image 2023-08-26 at 12 57 56](https://github.com/gururamu08/COLOR-CONVERSION/assets/118707009/d0ed7927-a3b0-4a7a-905e-37673a14218f)

### ii) HSV to RGB and BGR

![WhatsApp Image 2023-08-26 at 12 57 51](https://github.com/gururamu08/COLOR-CONVERSION/assets/118707009/e13aa958-bdbc-4586-92fb-0aab13044a55)

![WhatsApp Image 2023-08-26 at 12 57 50](https://github.com/gururamu08/COLOR-CONVERSION/assets/118707009/0d30bf4a-0f7e-4e9a-9679-551ed016c183)


### iii) RGB and BGR to YCrCb

![WhatsApp Image 2023-08-26 at 12 57 56](https://github.com/gururamu08/COLOR-CONVERSION/assets/118707009/2529efba-a713-4ada-8caa-0568e8fc65dd)

![WhatsApp Image 2023-08-26 at 12 57 56](https://github.com/gururamu08/COLOR-CONVERSION/assets/118707009/9c789e36-ed48-4f04-a27f-e888e8744845)

### iv) Split and merge RGB Image

![WhatsApp Image 2023-08-26 at 12 57 56](https://github.com/gururamu08/COLOR-CONVERSION/assets/118707009/b0a8b551-deef-4567-b3f6-9fc844aca469)


### v) Split and merge HSV Image

![WhatsApp Image 2023-08-26 at 12 57 50](https://github.com/gururamu08/COLOR-CONVERSION/assets/118707009/e72fb268-fc68-40fa-ae89-753a9c83cd73)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
