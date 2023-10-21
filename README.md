# EX-1 READ AND WRITE AN IMAGE
### AIM:
To write a python program using OpenCV to do the following image manipulations.
### Software Required:
- Anaconda - Python 3.7
### Algorithm:
- Step1: Choose an image and save it as a filename.jpg
- Step2: Use imread(filename, flags) to read the file.
- Step3: Use imshow(window_name, image) to display the image.
- Step4: Use imwrite(filename, image) to write the image.
- Step5: End the program and close the output image windows.
### Program:
```
Developed By: ROHIT JAIN D
Register Number: 212222230120
```
#### i) To Read,display the image
<table>
  <tr>
    <td width=50%>
      
    import cv2
    image=cv2.imread('blue.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('ROHIT JAIN',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()   
  </td>
  <td>
    <img src="https://github.com/ROHITJAIND/READ-AND-WRITE-IMAGE/assets/118707073/8929dcc6-55a7-4b6a-bd48-79ffa35aa244">
  </td>
  </tr>
</table>

#### ii) To write the image
<table>
  <tr>
    <td width=50%>
      
    import cv2
    image=cv2.imread('blue.jpg',0)
    cv2.imwrite('demo.jpg',image)
  </td>
  <td>
    <img src="https://github.com/ROHITJAIND/READ-AND-WRITE-IMAGE/assets/118707073/ee34c455-0e2a-4f8d-b395-df137426399f">
  </td>
  </tr>
</table>

#### iii) Find the shape of the Image
<table>
  <tr>
    <td width=50%>
      
    import cv2
    image=cv2.imread('blue.jpg',1)
    print(image.shape)  
  </td>
  <td>
    <img src="https://github.com/ROHITJAIND/READ-AND-WRITE-IMAGE/assets/118707073/c4de6d78-e6e3-4627-8865-a69664f76c32">
  </td>
  </tr>
</table>


#### iv) To access rows and columns

<table>
  <tr>
    <td width=30%>
      
    import random
    import cv2
    image=cv2.imread('blue.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)]
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
  </td>
  <td width="50%">
    <img src="https://github.com/ROHITJAIND/READ-AND-WRITE-IMAGE/assets/118707073/1792665b-5d6e-406b-8595-7635378a81a0">
  </td>
  </tr>
</table>

#### v) To cut and paste portion of image.


<table>
  <tr>
    <td width=50%>
      
    import cv2
    image=cv2.imread('blue.jpg',1)
    image=cv2.resize(image,(400,400))
    tag =image[150:200,110:160]
    image[110:160,150:200] = tag
    cv2.imshow('partimage1',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

  </td>
  <td>
    <img src="https://github.com/ROHITJAIND/READ-AND-WRITE-IMAGE/assets/118707073/c409c198-cb71-447e-bd57-a0d138265a2a">
  </td>
  </tr>
</table>

### Result:
Thus the images are read, displayed, and written successfully using the python program.
