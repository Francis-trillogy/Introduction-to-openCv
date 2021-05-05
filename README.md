# Introduction to OpenCV
**OpenCV (Open Source Computer Vision Library)** is an open source computer vision and machine learning software library. OpenCV was built to provide a common infrastructure for computer vision applications and to accelerate the use of machine perception in the commercial products. 
Being a BSD-licensed product, OpenCV makes it easy for businesses to utilize and modify the code. The license implies that it is free to use for both academic and commercial use. 
It supports a couple of programming languages namely: python, java, c and C++. On the other hand, it supports Windows, Linux, Mac Os and even the Android operating systems.

##### Installation

Python
    • run command below:
    • pip install opencv-python
    
##### Conda Envirnment
    • run the following commands:
    • conda install -c conda-forge opencv
    • conda install -c conda-forge/label/gcc7 opencv
    • conda install -c conda-forge/label/broken opencv
    • conda install -c conda-forge/label/cf201901 opencv
    • conda install -c conda-forge/label/cf202003 opencv
    
### Simple operations on images using OpenCV
    • Using OpenCV, we can read an image, display it and after we are done with our operations for the day, save it.
Reading an Image in OpenCV:
We will use the OpenCV function cv2.imread().
    • The function cv2.imread() requires two arguments: the first is the path to the image itself and the second specifies the way the image should be read.
    • What are some of these specifications? Here we go:
    
    1. **cv2.IMREAD_COLOR** — this flag in particular is used to load a color image. It neglects the image transparency and is the default flag. It is mostly for 8-bit images that don’t have the alpha channel.
    2.. **cv2.IMREAD_GRAYSCALE** — it is responsible for loading our images in grayscale.
    3.. **cv2.IMREAD_UNCHANGED** — It loads an image using alpha channel(RGBA). You can also pass integers 1, 0, -1 respectively in place of the flags.

It is always a good idea to try printing the image so it doesn’t give us an error when the path or image is wrong. Otherwise you will end up with TypeErrors and have no idea where you went wrong. 
***Note***: This is one place you could go wrong. Always make sure that the path to the image and the image specified exists and that you used the right extension for the image.
1. cv2.waitkey(0) — in milliseconds. It waits for a key press to do an action.
2. cv2.destroyAllWindows() — It destroys all windows created.
3. cv2.destroyWindow() — destroys the exact window name passed as an argument.

### Saving an image with OpenCV
Now that we have our image. we need to store it. OpenCV’s **cv2.imwrite** function enables you to save images to the specified path.
The above command will save our image in the working directory.
