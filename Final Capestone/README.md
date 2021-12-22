### Face Mask detection 
In this project, a face mask detection model that can accurately detect whether a person is wearing a mask or not is proposed.
The original dataset used in this project was from Kaggle. Data set consists of 7553 images with 3(RGB) channels in 2 folders as with_mask and without_mask. Images are named as label with_mask and without_mask. There are 3725 images of faces with_mask and 3828 images of faces without mask. The image data input parameters are the number of images, image height, image width, number of channels, and the number of levels per pixel. Typically, we have 3 channels of data corresponding to the colors Red, Green, Blue (RGB) Pixel levels are usually [0,255].
## EDA
The image dimensions were 350 * 525, and the number of channels were 3(RGB). The below picture was randomly selected image from the data set. The image needed to be scaled down 
before building a model.
![image](https://user-images.githubusercontent.com/59039411/147049582-5c5ac28b-1507-4b28-b14d-288f2b4a2c13.png)
