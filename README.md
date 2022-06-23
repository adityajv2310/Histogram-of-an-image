# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.

### Step3:
Display the histograms with their respective images.

### Step4:
Equalize the grayscale image.

### Step5:
Display the grayscale image.

## Program:
```python
# Developed By: Aditya JV
# Register Number: 212220230002

# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('Nature.jpg')
plt.imshow(Gray_image)
plt.show()
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

# Display the histogram of gray scale image and any one channel histogram from color image
Color_image=cv2.imread('Nature-photography.jpg')
plt.imshow(Color_image)
plt.show()
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

# Write the code to perform histogram equalization of the image. 
Gray_image=cv2.imread('Nature-photography.jpg',0)
equ=cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![Gray Image 23-06-2022 18_34_06](https://user-images.githubusercontent.com/75235386/175305694-7f92a2d8-1e1d-4fc2-bce9-af01cd6e9f1a.png)
![Histogram and Histogram Equalization of an image - Jupyter Notebook and 1 more page - Personal - Microsoft​ Edge 26-04-2022 20_18_36 (2)](https://user-images.githubusercontent.com/75235386/165332006-503c8527-8def-470a-a748-1b65f502b062.png)
![Histogram and Histogram Equalization of an image - Jupyter Notebook and 1 more page - Personal - Microsoft​ Edge 26-04-2022 20_15_35 (2)](https://user-images.githubusercontent.com/75235386/165332069-e310c086-922c-482a-9c6f-599bf617b8b4.png)

### Histogram of Grayscale Image and any channel of Color Image
![Histogram and Histogram Equalization of an image - Jupyter Notebook and 1 more page - Personal - Microsoft​ Edge 26-04-2022 20_15_35 (3)](https://user-images.githubusercontent.com/75235386/165332796-50b37dc4-2c57-48d6-af03-ba04da471eda.png)
![Histogram and Histogram Equalization of an image - Jupyter Notebook and 1 more page - Personal - Microsoft​ Edge 26-04-2022 20_18_36 (3)](https://user-images.githubusercontent.com/75235386/165332840-d6c8eefd-9b57-4f24-bf43-b92e288173b0.png)

### Histogram Equalization of Grayscale Image
![Gray Image 23-06-2022 18_34_06](https://user-images.githubusercontent.com/75235386/175305952-20bc232f-50de-4fd0-883a-27bf6768b298.png)
![Equalized Image 23-06-2022 18_34_18](https://user-images.githubusercontent.com/75235386/175306371-eb90d055-87f6-4fb8-85b0-f74efc1e3402.png)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
