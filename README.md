# Obect-Detection
In this problem we try to detect Car and persons present in the images or datasets.
We have used Yolov5 as our detection algorithm(https://github.com/ultralytics/yolov5.git).
# Dataset
The annotations were present in the COCO format so we converted the COCO format to YOLO format. We used https://github.com/ssaru/convert2Yolo.git repository for conversion.
# Training
I trained the model with given image datasets using the converted YOLO labels. I kept 2000 images for training and 239 images for validation.
# Inference 
You can directly use default Yolov5 weights for object detection by just mentioning the classes or else you can just use the trained weights.
