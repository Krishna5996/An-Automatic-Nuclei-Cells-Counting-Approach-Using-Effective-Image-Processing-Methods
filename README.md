Abstract—Manual counting of nuclei cells from histological images is considered tedious process, time-consuming and subjected to human errors. Therefore, automated the process of nuclei cells counting is become important and necessary for effective analyzing of  histological images. Current systems and approaches of nuclei cells counting are based on colour or greyscale images leading to inaccurate results and have several limitations. In this paper, we propose a novel accurate approach for automatic nuclei cells counting using effective image processing methods. The new techniques are designed based on image thresholding method, morphological image processing operations, and connected component algorithm. The new approach was evaluated experimentally on 37 images of a public data set of 100 histological images. The experimental results demonstrated that the approach achieved a high accuracy up to 89.5% compared with previous works. We concluded the effectiveness of the proposed approach for automatic counting of nuclei cells from histological images.

Histology: The study of the form of structures seen under the microscope. Histological sample image is 

![alt text](https://github.com/Krishna5996/An-Automatic-Nuclei-Cells-Counting-Approach-Using-Effective-Image-Processing-Methods/blob/master/images/histological.png?raw=true)

An image conatins pixles. Each pixel contains with their RGB (RED,GREEN,BLUE) value. only selecting RED values and printing the image means we are seelcting only RED Colord channel. so, we are Extacting each channel.

RED Channel

![alt text](https://github.com/Krishna5996/An-Automatic-Nuclei-Cells-Counting-Approach-Using-Effective-Image-Processing-Methods/blob/master/images/red_channel.png)

GREEN Channel

![alt text](https://github.com/Krishna5996/An-Automatic-Nuclei-Cells-Counting-Approach-Using-Effective-Image-Processing-Methods/blob/master/images/green.png)

BULE Channel

![alt text](https://github.com/Krishna5996/An-Automatic-Nuclei-Cells-Counting-Approach-Using-Effective-Image-Processing-Methods/blob/master/images/blue.png)

Thresholding an image:
Which means we are providing minimum and maximum threshold values of pixels. Means it will select the pixels with intensity provided by us .After applying threshold values we will get binary image and finally we are calculating nuclei(dots) in image using opencv library.Please refer the code.

![alt text](https://github.com/Krishna5996/An-Automatic-Nuclei-Cells-Counting-Approach-Using-Effective-Image-Processing-Methods/blob/master/images/binary.png)

Morphological operations 

Erosion :  we match our binary image(filter map) with structural component(filter) also known as kernel. Structural component  is a user defined matrix. In our project we have taken 3*3 matrix which contains all ones.
creating filter map after applying filter on binary  image with following values is called as Erosion
perfect match-1
some match-0
no match-0

Dilation-creating filter map after applying filter on binary image with following values is called as dialation

perfect match-1
some match-1
no match-0

Opening- perform first Erosion then Dilation
Closing-Perform first Dilation and then Erosion
The output at this stage is opening image because we applied opening morphological operation

![alt text]

Finally, we are are calculating the number of nuclei  by using findContours() function which provided by OPenCV  library. The final output will be total number of nuclei.   You can find the code in below link.
Thus, we have concluded the effectiveness of the proposed approach for automatic counting of nuclei cells from histological images.

