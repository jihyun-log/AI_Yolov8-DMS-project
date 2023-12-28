# Why did you use this model
- The YOLOv8 model is designed to be fast, accurate, and easy to use, making it an excellent choice for a wide range of object detection
- It will be used to create a model that will detect the driver's abnormal behavior
- we used Ultralytics' YOLOv8 and let them learn with our custom dataset


# Tip : User GPU Acceleration
- If you are running this notebook in Google Colab,
- navigate to Edit -> Notebook settings -> Hardware accelerator, set it to GPU, and then click Save.
- This will ensure your notebook uses a GPU, which will significantly speed up model training times.



# How to Train YOLOv8 Object Detection on a Custom Dataset
- Tutorial
  0. Google Mount
  1. Install YOLOv8
  2. Downloading the Dataset
  3. Load a pre-trained model
  4. Training with our custom dataset
  5. Validate
  6. Predict
  7. Export

# Important
- Routes in the code must be changed to suit your settings


# 0. Google Mount

# 1. Install YOLOv8
- Installing YOLOv8 and the libraries required to run YOLOv8
  
# 2. Downloading the Dataset
- We created a dataset using Roboflow Universe[Please refer to our technical note for the process of making a dataset using roboflow)](https://github.com/jihyun-log)
- And then, We prepare a custom dataset
- There are two ways to use the custom dataset
- Import from roboflow to preprocessed dataset code
- OR
- Place custom dataset on my drive and import to Google Mount

# 3. Load a pre-trained model

# 4. Training with our custom dataset
- In this process, We added a code that makes it easy to change the yaml file
- Based on the yolo model, which is the imported pretraind-model, learning proceeds

# 5. Validate
- Mean Average Precision (mAP): A value obtained by averaging the Average Precision for each class, which comprehensively represents performance for all classes
  - A high mAP indicates that the model has high precision and reproducibility for each class
- Box (Precision, Recall): Box-level precision and reproducibility for each class
  - High box-level precision and reproduction per class demonstrates how well the model senses that class
- mAP50, mAP50-95: mAP value when IoU (Intersection over Union) thresholds are different
  - High mAP50 and mAP50-95 indicate that the model performs well at various IoU thresholds.
- Precision, Recall: Model Precision and Reproducibility
  - High precision means that the model's predicted results are more likely to actually be correct
  - A high reproduction rate indicates how much the model has found out of all the real answers
  
# 6. Predict

# 7. Export
- Processes not required in DMS
