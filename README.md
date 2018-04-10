# GraspGAN_DA
Using GraspGAN to do domain adaptation between simulation and real world as described in "Using Simulation and Domain Adaptation to Improve Efficiency of Deep Robotic Grasping"

# Network Architecture
## G network:
  A convolutional neural network that follows a U-Net architecture. Key techeniques: average pooling for downsampling; bilinear upsampling; concatenation and 1x1 convolutions for the U-Net skip connections and instance normalization.
  
## D network:
  A patch-based(pix2pix) CNN with 5 convolutional layers. It is fully convolutional on 3 scales(472x472, 236x236, and 118x118) of the two input images-they are stacked into a 6 channel inputs which are used to produce domain estimates for all patches. 

![GraspGAN](GraspGAN.png)


