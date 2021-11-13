# Hazardous Object Detection System
**Project Group: hods-iss-group8**

## YOLOv5 (Linux Environment)
### - Before you Start 
1. Clone the repo and install *requirement.txt* in a Python >=3.6.0 environment (including PyTorch >=1.7)  
Type the following commands in a Terminal:
```
$ git clone https://github.com/ultralytics/yolov5
$ cd yolov5
$ pip install -r requirements.txt
```

### Train Custom Data
1. Download the yolov5 images dataset
2. Split the dataset by running the python script *"train_test_split.py"*
(You can skip this step and download the custom_dataset) 
3. Copy the YAML file to yolov5/data *"group8.yaml"* 
4. Select pretrained model to start training (yolov5s, yolov5m, yolov5l, yolov5x)
5. Train a YOLOv5 model (for example using yolov5s):
```
$ python train.py --img 640 --batch xx --epochs yy --data group8.yaml weights yolov5s.pt
```

### Deploy on Output Images
1. Download the output_images dataset
2. Do object detection on trained YOLOv5 model (for example using yolov5s)
```
$ python detect.py --save-txt --weights {trained model directory.pt} --source {output_images directory}
```

## Faster R-CNN and RetinaNet (COLAB Environment)
### Before you Start
1. Download the detectron2 image dataset
2. Create /detectron folder on google drive and upload the detectron2 image dataset
(detectron/coco_test folder, detectron/coco_train folder, and detectron/output folder)

### Train on Custom Data
1. Upload detectron2_faster_rcnn.ipynb into COLAB Environment and run step by step to generate the trained model for Faster R-CNN
2. Upload detectron2_retinanet.ipynb into COLAB Environment and run step by step to generate the trained model for RetinaNet


