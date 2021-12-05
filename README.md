# Obect-Detection
In this problem we try to detect Car and persons present in the images or datasets.
We have used Yolov5 as our detection algorithm(https://github.com/ultralytics/yolov5.git).
The notebook has the code with brief explanations.
# Dataset
The annotations were present in the COCO format so we converted the COCO format to YOLO format. We used https://github.com/ssaru/convert2Yolo.git repository for conversion.
Here you can find the model weights and inference datasets:https://drive.google.com/drive/folders/1z6srq14H8uZ-7kX9AAmzkQYKUCeJXWC6?usp=sharing
# Training
I trained the model with given image datasets using the converted YOLO labels. I kept 2000 images for training and 239 images for validation. The data.yaml contains the path for datasets and name of classes and yolo5s.pt is the default pretrained weight.
!python train.py --data data.yaml --weights yolov5s.pt 
# Inference 
You can directly use default Yolov5 weights for object detection by just mentioning the classes or else you can just use the trained weights.
!python detect.py --weights yolov5/runs/train/exp2/weights/best.pt --source yolov5/images/test --save-txt 
