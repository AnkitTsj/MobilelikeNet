#Custom_Object_Detection_Model
This repository contains a custom object detection model built using PyTorch. The model is inspired by MobileNet and trained on a custom dataset with over 66k+ images featuring a wide variety of objects, including makeup kits, animals, and other miscellaneous items.

Model Overview
The main idea was to implement a custom model that utilises deptwise separable convolutions and train model on single batch size to see if the model can detect object over a wide range of objects, the model has been trained over 66k+ images.
Wheer the custom data was used with interpolated images of size 640 x 640 x 3, the rgb choice of data was to enable model to extract contrasting features but due to limited compute i could not train such big network properly,
However the beginning layers have been observed to extrat some insightful features like separating the object from other non-trained objects.
I have spent 3 weeks trying and observing different close structures with single batch size, this results in violent loss but the performance is quite good.
The object detection model uses a MobileNet-inspired architecture with a focus on optimizing for speed and efficiency. It has been trained to detect certain objects in the dataset, although it's still in its early stages and requires further fine-tuning to achieve higher accuracy across more categories.

Key Features:
Custom Dataset: Trained on a large dataset containing diverse object types and annotations.
MobileNet-Inspired Architecture: Prioritizes lightweight, efficient inference, making it suitable for edge devices and real-time detection tasks.
Checkpoint-Saving Mechanism: The training loop incorporates a mechanism to save model checkpoints, allowing for resumed training and experimentation with different configurations.
Current Progress
The model successfully detects some objects, but there’s still room for improvement in terms of accuracy and generalization.
Only basic object localization is supported at the moment.
Dataset
The dataset includes a wide range of images, from crowds to animals, with varied and sometimes 'dirty' annotations (e.g., partial object annotations like a human tie without the whole person). The dataset is structured in the COCO format with keys for images and annotations.
dataset- https://www.kaggle.com/c/imagenet-object-localization-challenge
