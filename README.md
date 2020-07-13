# DCGAN
Generation of Fake images using Pytorch

It was first described by Radford et. al. in the paper https://arxiv.org/pdf/1511.06434.pdf .Here two models are trained simultaneously by an adversarial process. A generator learns to create images that look real, while a discriminator learns to tell real images apart from fakes.
### Datasets:

Here we used the Celeb-A Faces dataset which can be downloaded at https://s3-us-west-1.amazonaws.com/udacity-dlnfd/datasets/celeba.zip.
### GAN Structure:
![](https://developers.google.com/machine-learning/gan/images/gan_diagram.svg)

### How it works: 

Here this concept is so simple.
1. DCGANs actually comes under *Unsupervised Learning* and here there are two models i.e Generator and Discriminator.
2. Generator:the name itself says that it generates images.We never show the real faces to the generator, instead we add noise to the real images and give input to the Generator.
3. The job of discriminator is to detect the real faces. Here the discriminator has two inputs (a)fake images from generator (b)real images from user.
4. Then the discriminator detects which are real images and which are fake. Then we get the discriminator loss and Generator loss.
5. So, D(G(z)) is the probability (scalar) that the output of the generator G is a real image. As described in Goodfellow’s paper, D and G play a minimax game in which D tries to     maximize the probability it correctly classifies reals and fakes (logD(x)), and G tries to minimize the probability that D will predict its outputs are fake (log(1−D(G(x)))).     From the paper, the GAN loss function is

   ![](https://i.stack.imgur.com/hsGm2.gif)

### References:
[1] https://pytorch.org/tutorials/beginner/dcgan_faces_tutorial.html#

[2] https://arxiv.org/pdf/1511.06434.pdf
