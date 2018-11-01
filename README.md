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

- Yolov3 seems to have more accuracy than Fast Rcnn.
- Yolov3 execution Frames per second is far better than Fast RCNN.
- Yolov3 seems to detect small object precisely than larger object.
- Fast RCNN works great on high resolution pictures and is more accurate.
- For real time usage i think Yolov3 is better to implement in current scenario.(Although Faster RCNN can be used. we will try to cover it in future.)

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

**Please feel free to raise any issues, if anything is wrong in your concern.**

## Credit 
https://medium.com/@jonathan_hui/what-do-we-learn-from-single-shot-object-detectors-ssd-yolo-fpn-focal-loss-3888677c5f4d
https://medium.com/@jonathan_hui/object-detection-speed-and-accuracy-comparison-faster-r-cnn-r-fcn-ssd-and-yolo-5425656ae359
https://github.com/spmallick
