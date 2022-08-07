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
<li><b>Tech used</b>: Image Augmentation (creating data from existing data) and Transfer Learning Techniques (storing knowledge gained while solving one problem and applying it to a different but related problem). The model for object detection with no adverse conditions was trained on ImageNet dataset. This is fine tuned using various ML algorithms to train it in adverse conditions as well.</li>
<li><b>ML models</b>: Various models like SSD (Resnet 101 FPN), SSD (Resnet 50 FPN), Yolo v4, Faster RCNN (Resnet 50 FPN) and  were used to get the results, SSD (Resnet 50 FPN) giving the best results.</li>
</ul>

## Dataset
<ul>
<li>DAWN dataset (1000 images of both vehicles(major) and humans)</li>
<li>Real world images under various adverse weather conditions like rain, snow, fog and sand storm comprises a collection of 1000 images. </li>
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
  <li> Data Augmentation and neglecting the Humans' image</li>
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


## Predicting the vehicles in Adverse Conditions using YOLOV4
![1](https://user-images.githubusercontent.com/68558847/183274338-c7870ec4-b6e9-4259-8e95-309e12e9c384.jpg)

## Predicting the vehicles in Adverse Conditions using Faster RCNN
![50](https://user-images.githubusercontent.com/68558847/183274755-d2ccfb3f-85ee-4f79-baec-aa27c7e3cdbb.png)

## Predicting the vehicles in Adverse Conditions using SSD (RESNET 50)
![1](https://user-images.githubusercontent.com/68558847/183274539-7bfc7681-5e50-4883-a29d-33495efd2675.png)

## References
<ul>
<li> DAWN Dataset Citation: KENK, Mourad (2020), “DAWN”, Mendeley Data, V3, doi: 10.17632/766ygrbt8y.3</li>
<li> Additional Material: </li>
</ul>
  
  
  




