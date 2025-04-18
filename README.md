# YOLO Defect Detection Report
## Introduction

In modern manufacturing, product quality control is a critical component in ensuring production efficiency and customer satisfaction. With the widespread adoption of industrial automation, traditional manual inspection methods can no longer meet the increasing production demands.

Manual inspection is not only time-consuming and labor-intensive but also prone to subjective factors, leading to inconsistent results. To overcome these challenges, computer vision technology has gradually been introduced into product quality inspection.

However, early computer vision systems primarily relied on feature engineering-based methods, which showed clear limitations when dealing with complex scenarios and diverse product defects.

In recent years, with the rapid development of deep learning technology, particularly the widespread application of convolutional neural networks (CNNs), significant progress has been made in product defect detection technology.


****YOLO (You Only Look Once)****, as a deep learning-based object detection algorithm, has gained considerable attention for its high speed and accuracy. YOLO can simultaneously perform object detection and classification tasks in a single neural network forward pass, making it uniquely advantageous in real-time detection scenarios.

<img width="468" alt="Picture1" src="https://github.com/user-attachments/assets/77802937-06f3-4195-9734-30902de86d1b" />


> ****Objective****: The primary objective of this study is to explore how to utilize the YOLO algorithm to detect and classify defects in product images in industrial production. Through experiments on multiple industrial datasets, we aim to validate the effectiveness of the YOLO algorithm in product quality inspection.

## Dataset Preparation

The image dataset used encompasses various types of defects in different machine parts to effectively train and test the YOLO model.

- ****Sources****: Industrial production lines and laboratory simulations
- ****Content****: Common machine parts such as bearings, gears, and bolts
- ****Capture Conditions****: Controlled environments using high-resolution cameras and standardized lighting

Since the region of interest (RoI) could not be clearly distinguished, the entire image was labeled uniformly for defect type. This annotation was converted into a format required by the YOLO model.

## Data Splitting

- ****Training set****: 80%
- ****Testing set****: 20%

Ensured even distribution of different parts and their defect types across both sets.
![Picture2](https://github.com/user-attachments/assets/f8e1d33b-d80c-42e7-8324-8fdb90e6c5dd)

## Preprocessing and Augmentation

- ****Standardization****: Resizing and grayscale conversion
- ****Augmentation Techniques****:
  - Rotation
  - Scaling
  - Translation
  - Mirroring
  - Color jittering

These steps enhanced the model’s robustness and adaptability to varying lighting and environmental conditions.

## Network Training and Optimization

After preparing the dataset and designing the model architecture, network training and optimization became critical for efficient machine part defect detection.

### Strategies Implemented

- Hyperparameter tuning using ****grid search****
- Application of ****data augmentation****
- Selection of ****optimizers****
- Loss function design
- Training strategy adjustments

These strategies improved both ****accuracy**** and ****generalization****.

### Final Hyperparameters

- ****Learning Rate****: 0.001
- ****Batch Size****: 16
- ****Weight Decay****: 0.0005

Hyperparameters were dynamically adjusted based on early training performance to ensure fast convergence and avoid local minima.

## Performance Evaluation of the Model on the Test Set

*Details of model performance evaluation on test set can be inserted here (accuracy, mAP, confusion matrix, etc.)*![image](https://github.com/user-attachments/assets/3d9d247f-15d4-49f7-9d69-170de8888e14)

![Picture3](https://github.com/user-attachments/assets/c89dae5b-995c-4ac6-8fb9-0e2363b8ecd6)

![Picture4](https://github.com/user-attachments/assets/1216b4fd-b54b-48d8-8729-da1ef0a8f097)


## Conclusion

Experimental results demonstrated that the model maintains high accuracy and good real-time performance even in complex scenarios, showing strong potential for application in industrial production environments.

Although there is some performance trade-off when handling high-resolution images, the model can effectively balance detection precision and speed through appropriate configuration and optimization.

## References

1. Li, Zhenglin, et al. "Stock market analysis and prediction using LSTM: A case study on technology stocks." _*Innovations in Applied Engineering and Technology*_ (2023): 1-6.
2. Mo, Yuhong, et al. "Large Language Model (LLM) AI Text Generation Detection based on Transformer Deep Learning Algorithm." _*International Journal of Engineering and Management Research*_ 14.2 (2024): 154-159.
3. Li, Shaojie, Yuhong Mo, and Zhenglin Li. "Automated pneumonia detection in chest x-ray images using deep learning model." _*Innovations in Applied Engineering and Technology*_ (2022): 1-6.
4. Mo, Yuhong, et al. "Password complexity prediction based on roberta algorithm." _*Applied Science and Engineering Journal for Advanced Research*_ 3.3 (2024): 1-5.
5. Song, Jintong, et al. "A comprehensive evaluation and comparison of enhanced learning methods." _*Academic Journal of Science and Technology*_ 10.3 (2024): 167-171.
