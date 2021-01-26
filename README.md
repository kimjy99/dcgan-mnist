DCGAN (Deep Convolutional GAN) with MNIST
=============

## Model
### Generator:  
> Conv #1: ConvT(nz, 4ngf, 4, 1, 0) → BatchNorm → ReLU  
> Conv #2: ConvT(4ngf, 2ngf, 3, 2, 1) → BatchNorm → ReLU  
> Conv #3: ConvT(2ngf, ngf, 4, 2, 1) → BatchNorm → ReLU  
> Conv #4: ConvT(ngf, nc, 4, 2, 1) → Tanh  
(nz: dimension of latent vector, ngf: # of features of genetator, nc: # of channels)  
  
### Discriminator:  
> Conv #1: Conv(nc, ndf, 4, 2, 1) → LeakyReLU(0.2)  
> Conv #2: Conv(ndf, 2ndf, 4, 2, 1) → BatchNorm → LeakyReLU(0.2)  
> Conv #3: Conv(2ndf, 4ndf, 3, 2, 1) → BatchNorm → LeakyReLU(0.2)  
> Conv #4: Conv(4ndf, 1, 4, 1, 1) → Sigmoid  
(ndf: # of features of discriminator)  

### Gan Loss: CrossEntrophy (= Vanilla GAN)
  
------------------
## Output Images  
![output_img](./images/DCGAN_1.png)  

------------------
## Loss  
![loss_img](./images/DCGAN_2.png)  

------------------
## How Generator improved  
![improved_img](./images/DCGAN_3.png)  
