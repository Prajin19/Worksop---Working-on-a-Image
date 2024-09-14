# Workshop:Working-on-a-Image
## AIM :
Load two images of the same size.
Divide each image into four equal regions (quadrants) based on specific row and column coordinates.
Save the eight individual regions, labeling them as R1, R2, R3, R4 for the first image and R5, R6, R7, R8 for the second image.
Swap the regions as follows:
R1 with R8
R2 with R7
Resize the final images to dimensions specified by the last four digits of your registration number, ensuring the number is even.
## Code :

```
import cv2
abc=cv2.imread('img1.jpg')
mnb=cv2.imread('img2.jpg')
cv2.imshow('Imgwindw',abc)
cv2.imshow('IMgwdw',mnb)
cv2.waitKey(0)
cv2.destroyAllWindows()
rm=250
rc=250
r1=abc[0:rm,0:rc]
r2=abc[0:rm,rc:500]
r3=abc[rm:500,0:rc]
r4=abc[rm:500,rc:500]
r5=mnb[0:rm,0:rc]
r6=mnb[0:rm,rc:500]
r7=mnb[rm:500,0:rc]
r8=mnb[rm:500,rc:500]
cv2.imwrite('R1.jpg',r1)
cv2.imwrite('R2.jpg',r2)
cv2.imwrite('R3.jpg',r3)
cv2.imwrite('R4.jpg',r4)
cv2.imwrite('R5.jpg',r5)
cv2.imwrite('R6.jpg',r6)
cv2.imwrite('R7.jpg',r7)
cv2.imwrite('R8.jpg',r8)
```
```
cv2.imshow('R1.jpg',r1)
cv2.imshow('R2.jpg',r2)
cv2.imshow('R3.jpg',r3)
cv2.imshow('R4.jpg',r4)
cv2.waitKey(0)
cv2.destroyAllWindows()
abc[0:250,0:250]=r8
mnb[250:500,250:500]=r3
cv2.imshow('Im',abc)
cv2.imshow('IM',mnb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT
![Screenshot 2024-09-14 104255](https://github.com/user-attachments/assets/c0690d94-2d39-451b-8f4a-24062526f941)
![Screenshot 2024-09-14 104333](https://github.com/user-attachments/assets/966a9bb1-3f18-47f8-80ef-665a18acf72f)
![Screenshot 2024-09-14 104425](https://github.com/user-attachments/assets/2b2a3c5c-84ed-4ab1-945f-7cb66a7c920d)
## RESULT
Working on a image is done and aim to swap regions of two images is done sucessfully.

