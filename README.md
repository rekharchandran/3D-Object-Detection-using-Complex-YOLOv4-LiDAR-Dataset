# 3D-Object-Detection-using-Complex-YOLOv4-LiDAR-Dataset
3D Object Detection using Complex YOLOv4| LiDAR Dataset
### 3D Object Detection
3D object detection is an active research problem for Perceptiom of Autonomous vehicles. 2D prediction only provides 2D bounding boxes but with 3D Object detection, we can know various details of that object like size of an object, position of that object and orientation of that object. And we can use them in variety of applications in robotics, self-driving vehicles, augmented reality. There are various 3D datasets available which are related to street scenes due to the popularity of research into self-driving cars. Those datasets are created by 3D capture sensors like LIDAR.

### Getting Started
#### Requirement
pip install -U -r requirements.txt

### Data Preparation
The dataset is collected from KITTI vision benchmark suite, which has been captured from VW station wagon for use in mobile robotics and autonomous driving research. The 3D object detection benchmark consists of 7481 training images and 7518 test images as well as the corresponding point clouds, comprising a total of 80.256 labeled objects.                                                                                                                                                                  
Download the 3D KITTI detection dataset from [here](http://www.cvlibs.net/datasets/kitti/eval_object.php?obj_benchmark=3d)

The downloaded data includes:

Velodyne point clouds (29 GB): input data to the Complex-YOLO model
Training labels of object data set (5 MB): input label to the Complex-YOLO model
Camera calibration matrices of object data set (16 MB): for visualization of predictions
Left color images of object data set (12 GB): for visualization of predictions

Please make sure that you construct the source code & dataset directories structure as below.

${ROOT}
└── checkpoints/                                                                                                                                                       
    └── complex_yolov4/                                                                                                                                                                                                                                                                                              
    └── dataset/                                                                                                                                                       
└── kitti
├── ImageSets                                                                                                                                                           
│   ├── test.txt                                                                                                                                                       
│   ├── train.txt                                                                                                                                                       
│   ├── val.txt                                                                                                                                                         
├── training                                                                                                                                                           
│   ├── calib                                                                                                                                                           
│   ├── image_2                                                                                                                                                          │   ├── velodyne                                                                                                               
├── training                                                                                                                                                           
│   ├── calib                                                                                                                                                                
│   ├── image_2  

│   ├── label_2

│   ├── velodyne                                                                                                                                                                                                                



