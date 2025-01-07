


<h1 align="center">RT-DETR for Ripeness Detection of Strawberries in Complex Environments</h1>


<div align="center">



  ![](https://img.shields.io/badge/python-3.8.16-red)
  [![](https://img.shields.io/badge/pytorch-1.13.1-red)](https://pytorch.org/)
  [![](https://img.shields.io/badge/torchvision-0.14.1-red)](https://pypi.org/project/torchvision/)
  [![](https://img.shields.io/badge/RT-DETR-red)](https://github.com/lyuwenyu/RT-DETR)
  
  

  [🛠️Installation Dependencies](https://github.com/lyuwenyu/RT-DETR) |
  [🎤Introduction](https://github.com/lyuwenyu/RT-DETR) |
 
  [👀Download Dataset](https://pan.baidu.com/s/11E3HcrAptlONr5ujbL-JdQ?pwd=DSRD )) |
  
  [🌊Strawberries Detection](https://github.com/lcurryh/orbital.github.io) |
  [🚀Remote Sensing](https://github.com/lcurryh/orbital.github.io) |
  [🤔End-to-End](https://github.com/lcurryh/orbital.github.io) |
 

</div>



This is the official implementation of papers 
- [DETRs Beat YOLOs on Real-time Object Detection](https://arxiv.org/abs/2304.08069)


## Introduction

**The purpose of this repository is to**:

Combining the advantages of single-stage and end-to-end networks, this approach is designed to perform ripeness detection of strawberries with high efficiency and accuracy. By leveraging the simplicity and speed of single-stage networks alongside the precise feature modeling and comprehensive representation capabilities of end-to-end architectures, the proposed method effectively addresses the challenges of detecting strawberry ripeness in complex environments.


**The DSRD-Dataset includes more than 7700 photos of strawberries of different ripenness**：

The DSRD dataset we created is a comprehensive image collection consisting of 7,700 images. It is compiled by combining the self-collected CaptStraw dataset, the publicly available StrawDI_Db1 dataset, and the StrawberryNet dataset. 

The extraction code for the DSRD dataset is DSRD.

      

## How to use
Before training the network on the DSRD dataset, make sure to download the [RT-DETR](https://github.com/lyuwenyu/RT-DETR) code, clone this repository into the target folder, and then use the commands below to train the RT-DETR network.


```
# Clone RT-DETR repo and install requirements.txt
git clone https://github.com/lyuwenyu/RT-DETR  # clone
pip install -r requirements.txt  # install
```


## 📍 Implementations
- 🔥 RT-DETR 
  - paddle: [code&weight](./rtdetr_paddle)
  - pytorch: [code&weight](./rtdetr_pytorch)



## 🦄 Performance

### 🏕️ Complex Scenarios
<div style="text-align: center;">
  <a href="https://sm.ms/image/Q4rDLewmOipT8g1" target="_blank">
    <img src="https://s2.loli.net/2025/01/07/Q4rDLewmOipT8g1.jpg" width="800" alt="Image">
  </a>
</div>

## Feature enhancementh
To improve the generalization ability of the model, we utilized the popular Albu library to enhance the diversity of training samples. This library provides more than 70 types of advanced image augmentation techniques, offering extensive flexibility in data preprocessing. By applying transformations such as rotation, cropping, flipping, and scaling, we effectively minimize the risk of overfitting. Moreover, techniques like brightness and contrast adjustments, noise addition, and color alterations allow the model to better adapt to various lighting conditions and complex environments. Additionally, specific augmentations such as elastic deformation and grid distortion simulate different perspectives and scale variations, further improving the accuracy of strawberry detection. The goal is to enable the strawberry detection algorithm to perform effectively across a wider range of training scenarios. The techniques used include:

1）RGB Shift: Randomly alters the order of the image color channels, enhancing the model's adaptability to color variations.

2）Shift Scale Rotate: Applies affine transformations to images, including translation, scaling, and rotation, enhancing the model's robustness to changes in target position and scale.
	
3）Hue Saturation Value: Randomly adjusts the hue and saturation of images, helping the model better adapt to different environments and scenes.

4）	Random Brightness Contrast: Randomly adjusts the brightness and contrast of images to improve the model's adaptability to various lighting conditions.

5）Channel Shuffle: Randomly shuffles the RGB channels of images, adjusting the color distribution to help the model better recognize different color display methods.

6）Elastic Transform: Simulates the effect of images being distorted by elastic materials, aiding the model in learning to recognize non-rigid deformations that may be encountered in practical applications.

7）Grid Distortion: Distorts images by periodically or randomly moving grid points, simulating camera lens distortions or other visual distortions, and training the model to identify objects in deformed visual inputs.
