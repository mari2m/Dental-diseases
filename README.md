# Dental-diseases
Ai model for cellula internship 
Dental Disease Classification - Notebook
Overview
This repository contains a Jupyter Notebook focused on the classification of seven dental conditions using a deep learning model. The classes are:

OLP (Oral Lichen Planus): 540 samples
OC (Oral Cancer): 324 samples
Gum (Gingivitis): 360 samples
CaS (Caries Surface): 480 samples
CoS (Composite Surface): 450 samples
MC (Mucosal Change): 540 samples
OT (Other): 393 samples
Dataset
The dataset is divided into three folders for training, validation, and testing:

Training set: 3,087 files belonging to 7 classes.
Validation set: 1,028 files belonging to 7 classes.
Test set: 1,028 files belonging to 7 classes.
Model Architecture
This project utilizes ResNet50 as the backbone for the model:

Model: ResNet50(weights='imagenet', include_top=False, input_shape=(224, 224, 3))
Pretrained Weights: ImageNet
Customization: The top layers were excluded, and a custom classifier was added for fine-tuning the model on this dental classification task.
Performance Metrics
The model achieved the following results on the test set:

Class	Precision	Recall	F1-Score	Support
CaS    	0.97   	0.97	    0.97	    160
CoS    	0.99  	1.00    	0.99	    149
Gum    	0.95  	0.96	    0.95    	120
MC	    0.92  	0.95	    0.94    	180
OC	    0.98  	0.93	    0.95    	108
OLP	    0.96  	0.95	    0.96    	180
OT	    0.97  	0.97	    0.97    	131

Overall accuracy: 96%
Macro average: Precision: 0.96, Recall: 0.96, F1-Score: 0.96
Weighted average: Precision: 0.96, Recall: 0.96, F1-Score: 0.96

Repository Structure
notebook.ipynb: The main Jupyter Notebook containing code for data preprocessing, model training, evaluation, and visualizations.
dataset/: The directory containing the dental dataset.
models/: Saved model weights and architecture.
