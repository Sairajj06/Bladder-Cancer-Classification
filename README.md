Bladder Cancer Classification using Deep Learning
This project focuses on the classification of bladder cancer medical images using deep learning techniques. The objective is to assist medical image analysis by training convolutional neural network models capable of identifying different bladder cancer categories from medical imaging data.
Two deep learning models were used and compared in this project:
- EfficientNetB4
- ConvNext

Problem Statement
Bladder cancer diagnosis often relies on the visual analysis of medical images by experts. However, manual interpretation can be time-consuming and may vary depending on experience.
Deep learning models can assist in automated analysis of medical images by learning visual patterns associated with different cancer types. This project explores how modern convolutional neural networks can be applied to classify bladder cancer images into multiple categories.

Dataset
The dataset used in this project consists of bladder cancer medical images categorised in 4 classes 
Dataset is split intto Training, Validation and Test with a split ratio of 70:20:10.

Models
ConvNext 
Why we used ConvNext?
- ConvNeXt is capable of learning rich spatial features, which helps detect subtle visual patterns in medical images.
- It has shown strong performance in medical image classification and biomedical vision tasks
- ConvNeXt models provide high accuracy and robust feature learning for complex image datasets
- ConvNeXt has been used in multiple medical imaging studies and competitions for tasks such as tumor detection and radiology image classification
- Research reference paper-
  - Zhou, Y., et al.
   “Exploring ConvNeXt for Medical Image Classification.”
    IEEE Access, 2023

EfficientNetB4
Why we used EfficientNetB4?
- EfficientNet models are known for high accuracy and efficiency in image classification tasks
- They use compound scaling, which improves feature extraction without greatly increasing model complexity
- EfficientNet performs very well in medical image analysis tasks, especially when datasets are limited
- Using transfer learning from ImageNet helps the model learn medical features even with smaller datasets
- EfficientNet can capture fine visual patterns, which is important for detecting cancer-related structures in medical images
- Research reference paper-
  -Mingxing Tan and Quoc V. Le,
   “EfficientNet: Rethinking Model Scaling for Convolutional Neural Networks”
   Proceedings of ICML 2019

Model files are not uploaded due to GitHub file size limitations.
The notebooks contain full training code and evaluation results.

Training Approach
The models were trained using transfer learning techniques.
Key training steps included:
- Images were preprocessed and mormalised before training
- Data augumentation was applied to generate more training variations. But no changes in color and image contrast to maintain the medical conditions.
- A pretrained ConvNext model was used and fined tuned on the bladder cancer dataset
- The model was trained using Adam optimizer and categorical cross-entropy loss.
- Trainng progress was continously monitored and also at last was visualised using accuracy loss graph, to ensure no Overfitting and Underfitting of model.

Results:
Both models were evaluated using classification metrics and visualization techniques.
EfficientNetB4 Performance
-Accuracy: ~90%
ConvNeXt Performance
-Accuracy: ~97–98%

Technologies Used-
-Python
-TensorFlow / Keras
-NumPy
-OpenCV
-Matplotlib
-Seaborn
-Scikit-learn

Repository Sturucture-
Bladder-Cancer-Classification
│
├── README.md
├── dataset
│   └── dataset_info.txt
│
├── notebooks
│   ├── efficientnetb4-bladder-cancer-4-classes.ipynb
│   └── convnext-bladder-cancer-4-classes.ipynb
│
├── models
│   └── model_info.txt
│
├── results
│   ├── confusion_matrix.png
│   ├── accuracy_plot.png
│   └── loss_plot.png
│
└── requirements.txt

Author-
Sairaj Jagtap
B.Tech Computer Science ( Artificial Intiligence and Machine Learning)
Sanjivani University
