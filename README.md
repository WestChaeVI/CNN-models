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

[colab code](https://github.com/WestChaeVI/CNN-models/blob/main/models/VGGnet(72.6%25).ipynb)
![image](https://user-images.githubusercontent.com/104747868/224774082-bfa485cf-963b-4560-8549-73802231c75f.png)

--------------------------------------------------------------------------------------------------------------------------------------------------------------

### [**GoogLeNet**](https://arxiv.org/pdf/1409.4842.pdf)(2014)

+ Model   
I made the GoogLeNet model and Inception Architecture myself.    
I used ```torchvision.models``` to bring up the model, and trained it with the data set I had prepared.

+ Fine Tuning   
In the original GoogLeNet model FC layer, it was changed to **3(n_classes) instead of 1000** in the Softmax stage.   

![googlenet](https://user-images.githubusercontent.com/104747868/224735511-62674d01-c083-4233-9414-29c41c644a7c.jpg)

+ Results of an Experiment   
> Epochs : **100**   
> best epoch point : **84 epoch**   
> best epoch accuracy : **91.5 %**   

GoogleNet certainly seems to have shown good performance in Accuracy and Loss, unlike VggNet.   

[colab code](https://github.com/WestChaeVI/CNN-models/blob/main/models/GoogLeNet(91.5%25).ipynb)
![image](https://user-images.githubusercontent.com/104747868/224642095-5c895151-2318-496b-a75e-0cf012168909.png)

--------------------------------------------------------------------------------------------------------------------------------------------------------------

## [**ResNet**](https://arxiv.org/pdf/1512.03385.pdf)(2015)

+ Model   
I made the ResNet50 model and BottleNeck Architecture myself by using ```nn.Module```.    
I used ```torchvision.models``` to bring up the model, and trained it with the data set I had prepared.

+ Fine Tuning   
In the original ResNet model FC layer, it was changed to **3(n_classes) instead of 1000** in the Softmax stage.   

![resnet](https://user-images.githubusercontent.com/104747868/224752873-3bc238ef-20d8-42b4-9c75-8feedaa7bc1f.jpg)

+ Results of an Experiment   
> Epochs : **100**   
> best epoch point : **60 epoch**   
> best epoch accuracy : **91.04 %**   

In the case of the Resnet50 model, it showed good performance similar to GoogLeNet.   

[colab code](https://github.com/WestChaeVI/CNN-models/blob/main/models/ResNet50(91.04%25).ipynb)
![image](https://user-images.githubusercontent.com/104747868/224768444-901c1f0c-a616-46ab-bebc-c9215938a3da.png)

--------------------------------------------------------------------------------------------------------------------------------------------------------------

### [**SENet**](https://arxiv.org/pdf/1709.01507.pdf)(2017)



--------------------------------------------------------------------------------------------------------------------------------------------------------------

### [**DenseNet**](https://arxiv.org/pdf/1608.06993.pdf)(2017)

+ Model   
I made the DenseNet model and transition block myself by using ```nn.Module```.    
Then, I trained the model on a dataset that I prepared myself.   

+ Fine Tuning   
In the original DenseNet model FC layer, it was changed to **3(n_classes) instead of 1000** in the Softmax stage.   

![densenet](https://user-images.githubusercontent.com/104747868/225063696-51d93874-8d08-4df7-b4cb-bd38ce763c92.jpg)

+ Results of an Experiment   
> Epochs : **200**   
> best epoch point : **131 epoch**   
> best epoch accuracy : **64.45 %**   

On the first attempt, I trained with **'growth_rate : 12, epochs : 100, and batch : 8'**,    
but even trainset did not seem to learn properly,    
so I reset it to **'growth_rate : 24, epochs : 200, and batch : 32'**.   

As I implemented the model myself, it was based on the **Imagenet dataset**,    
so I changed the Architecture to fit my dataset as much as I could,    
but I don't think the performance came out as much as I wanted.   

[colab code](https://github.com/WestChaeVI/CNN-models/blob/main/models/DenseNet(64.45%25).ipynb)
![image](https://user-images.githubusercontent.com/104747868/225065009-371225b4-28a6-4f48-8b6b-1178a890c867.png)


--------------------------------------------------------------------------------------------------------------------------------------------------------------

## Segmentation

### **FCN(2015)**
[paper](https://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Long_Fully_Convolutional_Networks_2015_CVPR_paper.pdf)

--------------------------------------------------------------------------------------------------------------------------------------------------------------

### **U-Net(2015)**
[paper](https://arxiv.org/pdf/1505.04597.pdf)

--------------------------------------------------------------------------------------------------------------------------------------------------------------

### **MobileNet(2017)**
[paper](https://arxiv.org/pdf/1704.04861.pdf)

--------------------------------------------------------------------------------------------------------------------------------------------------------------

### **PSPNet(2017)**
[paper](https://arxiv.org/pdf/1612.01105.pdf)

--------------------------------------------------------------------------------------------------------------------------------------------------------------

### **DeepLabV3(2018)**
[paper](https://arxiv.org/pdf/1802.02611.pdf)


--------------------------------------------------------------------------------------------------------------------------------------------------------------

## GAN

--------------------------------------------------------------------------------------------------------------------------------------------------------------

## Object Dictection




