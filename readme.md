### ECE-GY 7123 Introduction to Deep Learning Mini-Project

- This is the Mini-Project for ECE-GY 7123 Introduction to Deep Learning. The goal of this mini-project is to construct an improved Residual Network (ResNet) architecture with high test accuracy on the CIFAR-10 dataset, and has less than 5M parameters.

**contributor**
- Lorenzo Schellack
- Siddharth Shah
- Sikang Yang

### Abstract

In this project, we propose two modified ResNet architectures, one small
and one large, with less than 5 million parameters, designed
to achieve high accuracy on the CIFAR-10 dataset. After 40
epochs of training, the experimental results demonstrate that
the large model achieved an accuracy of 89 percent, while
the small model achieved an accuracy of roughly 80 percent.
Notably, the large model achieved similar accuracy as the
ResNet-18 framework, while using a smaller amount of parameters, making it more computationally efficient. Greater
performance could be achieved by increasing the number of
training epochs, or incorporating additional techniques such
as data augmentation
                    
| Model  |  optimizer  | Number of Parameters  | Training Accuracy | Testing Accuracy |
| :------------ |:---------------:|:---------------:| -----:|-----:|
| Lite(small)      | SGD + Momentum |78,042 | 79.12% | 79.87%|
| Improved(large) | SGD  + Momentum | 4,903,242 | 94.65%   | 89.68% |
| Improved(large) | Adam | 4,903,242 | 98.42%   | 91.52% |

## Lite(small) ResNet summary
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================

        Conv2d-1               [-1, 16, 32, 32]            432
       BatchNorm2d-2           [-1, 16, 32, 32]              32
            Conv2d-3           [-1, 16, 32, 32]           2,304
       BatchNorm2d-4           [-1, 16, 32, 32]              32
            Conv2d-5           [-1, 16, 32, 32]           2,304
       BatchNorm2d-6           [-1, 16, 32, 32]              32
               RBL-7           [-1, 16, 32, 32]               0
            Conv2d-8           [-1, 32, 16, 16]           4,608
       BatchNorm2d-9           [-1, 32, 16, 16]              64
           Conv2d-10           [-1, 32, 16, 16]           9,216
      BatchNorm2d-11           [-1, 32, 16, 16]              64
           Conv2d-12           [-1, 32, 16, 16]             512
      BatchNorm2d-13           [-1, 32, 16, 16]              64
              RBL-14           [-1, 32, 16, 16]               0
           Conv2d-15             [-1, 64, 8, 8]          18,432
      BatchNorm2d-16             [-1, 64, 8, 8]             128
           Conv2d-17             [-1, 64, 8, 8]          36,864
      BatchNorm2d-18             [-1, 64, 8, 8]             128
           Conv2d-19             [-1, 64, 8, 8]           2,048
      BatchNorm2d-20             [-1, 64, 8, 8]             128
              RBL-21             [-1, 64, 8, 8]               0
AdaptiveAvgPool2d-22             [-1, 64, 1, 1]               0
           Linear-23                   [-1, 10]             650
----------------------------------------------------------------

Total params: 78,042
Trainable params: 78,042
Non-trainable params: 0
----------------------------------------------------------------

Input size (MB): 0.01
Forward/backward pass size (MB): 1.53
Params size (MB): 0.30
Estimated Total Size (MB): 1.84
----------------------------------------------------------------

## Improved(Large) ResNet summary

----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================

            Conv2d-1           [-1, 64, 32, 32]           1,728
       BatchNorm2d-2           [-1, 64, 32, 32]             128
            Conv2d-3           [-1, 64, 32, 32]          36,864
       BatchNorm2d-4           [-1, 64, 32, 32]             128
            Conv2d-5           [-1, 64, 32, 32]          36,864
       BatchNorm2d-6           [-1, 64, 32, 32]             128
               RBL-7           [-1, 64, 32, 32]               0
            Conv2d-8          [-1, 128, 16, 16]          73,728
       BatchNorm2d-9          [-1, 128, 16, 16]             256
           Conv2d-10          [-1, 128, 16, 16]         147,456
      BatchNorm2d-11          [-1, 128, 16, 16]             256
           Conv2d-12          [-1, 128, 16, 16]           8,192
      BatchNorm2d-13          [-1, 128, 16, 16]             256
              RBL-14          [-1, 128, 16, 16]               0
           Conv2d-15            [-1, 256, 8, 8]         294,912
      BatchNorm2d-16            [-1, 256, 8, 8]             512
           Conv2d-17            [-1, 256, 8, 8]         589,824
      BatchNorm2d-18            [-1, 256, 8, 8]             512
           Conv2d-19            [-1, 256, 8, 8]          32,768
      BatchNorm2d-20            [-1, 256, 8, 8]             512
              RBL-21            [-1, 256, 8, 8]               0
           Conv2d-22            [-1, 512, 4, 4]       1,179,648
      BatchNorm2d-23            [-1, 512, 4, 4]           1,024
           Conv2d-24            [-1, 512, 4, 4]       2,359,296
      BatchNorm2d-25            [-1, 512, 4, 4]           1,024
           Conv2d-26            [-1, 512, 4, 4]         131,072
      BatchNorm2d-27            [-1, 512, 4, 4]           1,024
              RBL-28            [-1, 512, 4, 4]               0
AdaptiveAvgPool2d-29            [-1, 512, 1, 1]               0
           Linear-30                   [-1, 10]           5,130
----------------------------------------------------------------

Total params: 4,903,242
Trainable params: 4,903,242
Non-trainable params: 0
----------------------------------------------------------------

Input size (MB): 0.01
Forward/backward pass size (MB): 6.57
Params size (MB): 18.70
Estimated Total Size (MB): 25.28
----------------------------------------------------------------
----
### End




