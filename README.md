# Adverse Weather Object Detection using Customized Models

## Why this Project?
<ul>
<li> Adverse weather-related fatalities constituted about 16 % of total fatalities. This model if implemented with a hardware device and equipped within a vehicle will help mitigating these accidents.</li>
<li> Self Drive Cars which are capable of cue assisstance during Taffic Jams, Collision Avoidance, etc. fail during conditions like heavy fog, rain, snow and sandstorms.</li>
<li> CCTV cameras are unable to work perfectly during adverse weather conditions.</li>
</ul>

## Abstract
<ul>
<li><b>Principle</b>: Utilized DAWN2020 dataset to check the efficiency of the already built object detection models to detect vehicles in adverse weather conditions.</li>
<li><b>Tech used</b>: Image Augmentation (creating data from existing data) and Transfer Learning Techniques (storing knowledge gained while solving one problem and applying it to a different but related problem). The model for object detection with no adverse conditions was trained on ImageNet dataset. This is fine tuned using various ML algorithms to train it in adverse conditions as well (adaptive learning rate).</li>
<li><b>ML models</b>: Various models like YOLO V4, SSD (Resnet 50 FPN), Faster RCNN (Resnet 50 FPN) and  were used to get the results, Faster RCNN (Resnet 50 FPN) giving the best results.</li>
</ul>

## Dataset
<ul>
<li>DAWN dataset (1027 images of both vehicles(major) and humans)</li>
<li>300 images of fog, 200 of rain, 323 of sand and 204 images of snow</li>
<li>The dataset is annotated using LabelMe for 6 types of vehicles(Bicycle, Bus, Car, MotorCycle, Train, Truck).</li></br>
</ul>

## Dawn Dataset Statistics
![image](https://user-images.githubusercontent.com/68558847/183251828-00364df9-0389-4e02-9a86-604f926b58c0.png)

## Sample images from Dawn dataset
![image](https://user-images.githubusercontent.com/68558847/183251366-f85a8922-a57f-4410-861c-a542dcb91988.png)

## Annotated images
![image](https://user-images.githubusercontent.com/68558847/183251774-9d1c42b7-4f4e-4808-8ff2-92059330c308.png)

## Phases
<ul>
  <li> Data Augmentation (via ImageDataGenerator Class): rotation, shearing, Zooming, cropping, flipping and changing the brightness level. Also, neglecting the Humans' image</li>
  <li> Data Preprocessing: the actual image size was large thus the images are scaled into 640*640*3 (RGB) so that computation can be reduced</li>
  <li> Dividing the dataset into train, validation and test </li>
  <li> Choosing the model</li>
  <li> Training and then Evaluating the model</li> 
  <li> Make Predictions</li>
</ul>

## Steps followed during the Vehicle Detection 
<ul>
    <li>Feature Extraction</li>
    <li>Feature Aggregation</li>
    <li>Bounding Box Prediction</li>
</ul>

## The path followed
<ul>
  <li> Studied various papers related to Object Detection and according to that tried different models one by one</li>
  <li> The result is found out on the basis of mean Average Precision (mAP) value of the different models. The same is shown with help of the graph, table and the sample test image below</li>
  <li> The GitHub link from which the models' zip file was extracted and some of the research papers studied link is in the refernces below</li>
  <li> As we progressed, we kept on doing hyperparameter tuning such as taking different initial learning rate, variance of learning rate, backpropagation process, number of layers, etc.</li>
</ul>

## Results
## Predicting the vehicles in Adverse Conditions using YOLOV4
![1](https://user-images.githubusercontent.com/68558847/183274338-c7870ec4-b6e9-4259-8e95-309e12e9c384.jpg)

## Predicting the vehicles in Adverse Conditions using SSD (RESNET 50)
![1](https://user-images.githubusercontent.com/68558847/183274539-7bfc7681-5e50-4883-a29d-33495efd2675.png)

## Predicting the vehicles in Adverse Conditions using Faster RCNN
![50](https://user-images.githubusercontent.com/68558847/183274755-d2ccfb3f-85ee-4f79-baec-aa27c7e3cdbb.png)

## Training Loss for various models

![SSD ResNet loss](https://user-images.githubusercontent.com/68558847/183293750-8ba6f7eb-fd9d-43d2-8be5-9178ab985a49.png)
![Faster RCNN loss](https://user-images.githubusercontent.com/68558847/183293754-41cefef7-3339-4bee-ade5-cd016fca7a20.png)

## Mean Average Precision (mAP) individual model result
![SSD ResNet 50](https://user-images.githubusercontent.com/68558847/183293794-68c5bae8-92ac-4a44-9cd9-f157cc6a1549.png)
![faster RCNN](https://user-images.githubusercontent.com/68558847/183293801-e44ac4a4-e421-4e3c-a337-e8bd58c5b38d.png)
![YOLO_Graphs](https://user-images.githubusercontent.com/68558847/183293798-f9adf632-baf0-4f53-81fd-f1f1d38535d5.png)

## mAP Overall comparison
![MAP value compare](https://user-images.githubusercontent.com/68558847/183293704-b6aad73e-ddc4-4e4d-aedb-7292e1ae112a.png)


## Improvement scope
<ul>
  <li>Different Dataset</li>
  <li>Hyperparameter tuning</li>
  <li>Choosing different models</li>
</ul>

## References
<ul>
<li> DAWN Dataset Citation: KENK, Mourad (2020), “DAWN”, Mendeley Data, V3, doi: 10.17632/766ygrbt8y.3</li>
<li> https://arxiv.org/pdf/2004.10934.pdf</li>
<li> https://proceedings.neurips.cc/paper/2015/file/14bfa6bb14875e45bba028a21ed38046-Paper.pdf</li>
<li> https://arxiv.org/pdf/1912.06319.pdf </li>
<li> https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md </li>
</ul>
