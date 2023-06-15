# Coding3_final
reference：https://www.tensorflow.org/tutorials/generative/dcgan?hl=zh-cn

video：https://youtu.be/1dSc9nnPfRc

dataset：https://www.robots.ox.ac.uk/~vgg/data/flowers/102/ 

### Description of work:
I used the DCGAN algorithm to process images from the Oxford Flowers 102 （https://www.robots.ox.ac.uk/~vgg/data/flowers/102/ ） database and generate images with floral patterns. I trained the algorithm for several iterations, 500, 2000 and 4000 iterations respectively.
By gradually increasing the number of iterations, I found that the resulting images became progressively more distinct and realistic. As the number of iterations increased, the adversarial training between the generator and discriminator was further enhanced, resulting in an improvement in the quality of the generated images. The generated flower patterns became sharper, more detailed, and closer to the appearance of real flowers.
This phenomenon can be attributed to the properties of the DCGAN algorithm. The generative adversarial network optimises the model through mutual confrontation between the generator and discriminator during training, allowing the generator to gradually learn to generate images better. As the number of iterations increases, the model better understands the features and distribution of the floral images in the training dataset, resulting in the generation of more realistic and high-quality images.

## Training process:
### Replacing the database:
First, I tried referencing the Oxford Flowers 102 database directly from the link to the Colab environment. However, a number of problems were encountered. The sheer size of the database caused it to run particularly slowly, while the resulting images appeared disorganised.
To solve these problems, I decided to download the database locally and select some of the images for training. In order to increase the run rate, control the training data and generate high quality images. By using a subset of the local database for training, I managed to solve the problems of slow running and poor image quality caused by the oversized original database. 
![image](https://github.com/IvyXiaoyede/Coding3_final/assets/119190967/ba40504d-dc93-4320-a203-708d49805473)

<img width="436" alt="image" src="https://github.com/IvyXiaoyede/Coding3_final/assets/119190967/d494c0a6-61c9-402f-9e65-49a2996065da">


### Changing the RGB channels:
After replacing the database, you have processed the training content and one of the important changes is the change of image channels. Whereas the images in the original database were single-channel black and white images, after replacing the database you converted the images to colour channels, i.e. three-channel images. This channel change also provides your model with a richer set of input features. In the original single-channel image, the model can only rely on the grey scale values to learn the features of the image. Whereas in a colour image, the model can use the interactions and differences between the different channels to capture more of the image features. 

![image](https://github.com/IvyXiaoyede/Coding3_final/assets/119190967/36adf6da-8ee2-4639-9de3-08cccb10d589)

![image](https://github.com/IvyXiaoyede/Coding3_final/assets/119190967/6cb93120-f60a-4dba-9387-013174dc336d)



### Changing the precision of training:
I made adjustments to the accuracy of the training, mainly focusing on the input size of the image and the number of times the generator was generated. Firstly, the size of the original image can be relatively small and I chose a larger input image size (500*750). By increasing the size of the input image, you provide the model with more image detail. Secondly, a smaller image size was chosen for the first two training sessions. It was to speed up the training and to explore the behaviour of the model. Smaller image sizes reduce the computational load of each batch and converge faster to an initial solution. For the final training, a larger image size (128x128 pixels) was chosen and the number of generators generated was increased. This was done to obtain a single image with a more pronounced training effect.


## Problems encountered:
-Channel problem, the image itself is a monochrome channel, I was unable to match the channel to the training channel when processing the image, finally with the help of Chatgpt, I reduced the channel to make the image single channel output.
-The generated gif could not be played in the Colab, the file was too big to solve, so I downloaded it and played it.
-The change in the image did not appear, and with the help of Jasper, it was found that the wrong layer was running.

Result：
FFFFinal_2_py.ipynb
https://youtu.be/Pa-0_m-2rUo
