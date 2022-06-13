# 3D-Object-Detection-using-Complex-YOLOv4-LiDAR-Dataset
3D Object Detection using Complex YOLOv4| LiDAR Dataset
### 3D Object Detection
3D object detection is an active research problem for Perceptiom of Autonomous vehicles. 2D prediction only provides 2D bounding boxes but with 3D Object detection, we can know various details of that object like size of an object, position of that object and orientation of that object. And we can use them in variety of applications in robotics, self-driving vehicles, augmented reality. There are various 3D datasets available which are related to street scenes due to the popularity of research into self-driving cars. Those datasets are created by 3D capture sensors like LIDAR.

### Getting Started
### Clone the repository
https://github.com/maudzung/Complex-YOLOv4-Pytorch

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

### How to run

#### visualize the dataset(both BEV images from LiDAR and camera images)

cd src/data_process

python kitti_dataloader.py --output-width 608

#### Training

python train.py --gpu_idx 0 --batch_size <N> --num_workers <N>...
  
 #### Testing
  
  python test.py --pretrained_path --gpu_idx 0 
  
  #### Inference
  python test.py --gpu_idx 0 --pretrained_path ../checkpoints/complex_yolov4/complex_yolov4_mse_loss.pth --cfgfile ./config/cfg/complex_yolov4.cfg --show_image
  
  #### Evaluation
  
  python evaluate.py --gpu_idx 0 --pretrained_path <PATH> --cfgfile <CFG> --img_size <SIZE> --conf-thresh <THRESH> --nms-thresh <THRESH> --iou-thresh <THRESH>
  
  #### Tensorboard
  To track the training progress, go to the logs/ folder and
  
  cd logs/<saved_fn>/tensorboard/
  tensorboard --logdir=./
  
  Then go to http://localhost:6006/:

  
  
  ### Folder Structure

![1](https://user-images.githubusercontent.com/50706192/173327562-d8ceb29a-6d8a-4c11-80b1-746b1ed32317.png)






