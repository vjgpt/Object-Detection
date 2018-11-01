# Object-Detection
This project is used for object detection using Yolov3 and Fast RCNN.

YOLO and Fast RCNN are two different types of object detectors.
- Yolo is a Single Shot detectors.
- Fast RCNN is a Region based deetctors.

## Demo
<table>
  <tr>
    <th>YOLOv3</th>
    <th>Fast-RCNN</th>
  </tr>
  <tr>
    <td>
      <img src="https://github.com/vjgpt/Object-Detection/blob/837d09419842bd404ad6c36ccf3898fec7a39352/data/yolo.gif">
    </td>
    <td>
      <img src="https://github.com/vjgpt/Object-Detection/blob/eddf8ec8b102b35b6efe36f954232fb90ee9e8f9/data/rcnn.gif">
    </td>
  </tr>
</table>

**Download the necessary weights and files.**

Fast RCNN model

`wget http://download.tensorflow.org/models/object_detection/mask_rcnn_inception_v2_coco_2018_01_28.tar.gz` `tar zxvf mask_rcnn_inception_v2_coco_2018_01_28.tar.gz`

YOLOv3

`wget https://pjreddie.com/media/files/yolov3.weights`

`wget https://github.com/pjreddie/darknet/blob/master/cfg/yolov3.cfg?raw=true -O ./yolov3.cfg`

## Dependencies
- Opencv

## Usage
- `data` folder contains all the input and output files.
- Run `mask_rcnn.py` and `yolo.py` for Fast RCNN and Yolov3 respectively.
- `mscoco_labels.names` contain names of object which can be detected.

Commandline usage for object detection using YOLOv3 and Fast RCNN.

a single image:

`python yolo.py --image=cars.jpg`
  
`python mask_rcnn.py --image=data\cars.jpg`
  
a video file:

`python yolo.py --video=run.mp4`
  
`python3 mask_rcnn.py --video=run.mp4`

If no argrument is passed, it start's the webcam.
