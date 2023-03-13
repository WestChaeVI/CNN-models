# CNN models
 Comparison of model performance
--------------------------------------------------------------------------------------------------------------------------------------------------------------

## Image Classification

#### Dataset   
+ Object Class : 3 (Dolphin, shark, whale)   
+ total : 1312 images   
+ trainset : 70%   
+ validset : 20%   
+ testset : 10%   
![돌상고](https://user-images.githubusercontent.com/104747868/224483448-880732f0-bbe5-40de-9317-0a134e3498da.jpg)

--------------------------------------------------------------------------------------------------------------------------------------------------------------

### [VGGNet](https://arxiv.org/pdf/1409.1556.pdf)(2014)   

+ Model   
Using ```tensorflow.keras``` , I made the vgg19 model myself and brought the prepared dataset to learn(train).

+ Fine Tuning   
In the original VGG19 model FC layer, it was changed to **3(n_classes) instead of 1000** in the Softmax stage.   

![0312011037308459](https://user-images.githubusercontent.com/104747868/224495143-30c14185-0a50-4453-b031-03be02aafb69.jpg)   

+ Results of an Experiment   
> Epochs : **100**   
> best epoch point : **68 epoch**   
> best epoch accuracy : **72.6 %**   

The Vgg19 model is obviously a great model, but the architecture of VggNet seems to have not been effectively applied to the datasets I prepared because it was based on a large dataset.   

[colab code](https://github.com/WestChaeVI/CNN-models/blob/main/models/VGGnet(72_6%25).ipynb)
![image](https://user-images.githubusercontent.com/104747868/224492827-2ec7913c-7eb0-4da5-b125-83ef8dd4916d.png)


### **GoogLeNet(2014)**
[paper](https://arxiv.org/pdf/1409.4842.pdf)

+ Model   
Using ```torchvision.models``` , I made the GoogLeNet model and Inception Architecture myself and brought the prepared dataset to learn(train).

+ Fine Tuning   
In the original GoogLeNet model FC layer, it was changed to **3(n_classes) instead of 1000** in the Softmax stage.   

![0312011037308459](https://user-images.githubusercontent.com/104747868/224495143-30c14185-0a50-4453-b031-03be02aafb69.jpg)   

+ Results of an Experiment   
> Epochs : **100**   
> best epoch point : **84 epoch**   
> best epoch accuracy : **91.5 %**   

GoogleNet certainly seems to have shown good performance in Accuracy and Loss, unlike VggNet.   

[colab code](https://github.com/WestChaeVI/CNN-models/blob/main/models/GoogLeNet(91.5%25).ipynb)


### **ResNet(2015)**
[paper](https://arxiv.org/pdf/1512.03385.pdf)


### **SENet(2017)**
[paper](https://arxiv.org/pdf/1709.01507.pdf)


--------------------------------------------------------------------------------------------------------------------------------------------------------------

## Segmentation

### **FCN(2015)**
[paper](https://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Long_Fully_Convolutional_Networks_2015_CVPR_paper.pdf)

### **U-Net(2015)**
[paper](https://arxiv.org/pdf/1505.04597.pdf)

### **MobileNet(2017)**
[paper](https://arxiv.org/pdf/1704.04861.pdf)

### **PSPNet(2017)**
[paper](https://arxiv.org/pdf/1612.01105.pdf)

### **DeepLabV3(2018)**
[paper](https://arxiv.org/pdf/1802.02611.pdf)


--------------------------------------------------------------------------------------------------------------------------------------------------------------

## GAN

--------------------------------------------------------------------------------------------------------------------------------------------------------------

## Object Dictection




