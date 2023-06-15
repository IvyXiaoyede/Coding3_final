# Coding3_final
reference：https://www.tensorflow.org/tutorials/generative/dcgan?hl=zh-cn
video：
dataset：
### Description of work:
I used the DCGAN algorithm to process images from the Oxford Flowers 102 （https://www.robots.ox.ac.uk/~vgg/data/flowers/102/ ） database and generate images with floral patterns. I trained the algorithm for several iterations, 500, 2000 and 4000 iterations respectively.
By gradually increasing the number of iterations, I found that the resulting images became progressively more distinct and realistic. As the number of iterations increased, the adversarial training between the generator and discriminator was further enhanced, resulting in an improvement in the quality of the generated images. The generated flower patterns became sharper, more detailed, and closer to the appearance of real flowers.
This phenomenon can be attributed to the properties of the DCGAN algorithm. The generative adversarial network optimises the model through mutual confrontation between the generator and discriminator during training, allowing the generator to gradually learn to generate images better. As the number of iterations increases, the model better understands the features and distribution of the floral images in the training dataset, resulting in the generation of more realistic and high-quality images.

## Training process:
### Replacing the database:
First, I tried referencing the Oxford Flowers 102 database directly from the link to the Colab environment. However, a number of problems were encountered. The sheer size of the database caused it to run particularly slowly, while the resulting images appeared disorganised.
To solve these problems, I decided to download the database locally and select some of the images for training. In order to increase the run rate, control the training data and generate high quality images. By using a subset of the local database for training, I managed to solve the problems of slow running and poor image quality caused by the oversized original database. (Image)
