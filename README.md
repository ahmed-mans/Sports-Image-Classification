# Sports Image classification

## 🏅 Project Overview
This project demonstrates how to train a __fine tune a pre-trained model__ to classify sports images into __73 distinct categories__ such as :

```
swimming,  
skydiving,  
speed_skating,
rugby,
arm_wrestling,
rings,
bowling,
crikcket,
etc.
```
### 🧪 Implementation

The full training and implementation process is contained in the notebook `sport_image_classification.ipynb`.

It includes:
- Dataset preprocessing
- Fine tuning<br>
- Training and evaluation of the model.

## 🗂️ Dataset Description
The dataset contains a total of __11,146 images__ categorized into __73 sports classes__.

To train the CNN model effectively, the original training set was divided into two subsets:<br>
- __80%__ for training<br>
- __20%__ for validation.

The image below showcases a few sample classes from the training set, along with the __number of images per class__ indicated in brackets.
![image](https://github.com/user-attachments/assets/973aa41f-ea67-42ae-95a9-27651a6168d5)<br>
[Reference](https://www.kaggle.com/competitions/open-cv-tf-project-2-image-classification-round-3/data)

- 📥 **Dataset Download**:  
  [73 classes sports images dataset](https://www.kaggle.com/competitions/open-cv-tf-project-2-image-classification-round-3/data)


## 🧠 CNN Model Architecture

This project features a **fine tuned efficientnetB3 model** tailored for this classification task.

- The architecture includes consists of the efficienctnetb3 model for which only the last 30 layers of the convolutional base are trainable.<br>
- The extracted features are then passed through **two fully connected (Dense) layers**, ending with a **final output layer** using `softmax` activation to produce class probabilities across the **73 sports classes**.

## ⚙️ Training HyperParameters

- Epochs: __50__
- Optimizer: __SGD__
- Initial Learning Rate: __0.001__
- Batch size: __8__

## 📉 Model Training Progress

The following graphs illustrate the evolution of the model's **accuracy** and **loss** throughout the training process.

![image](https://github.com/user-attachments/assets/f3160d89-1217-4f48-a258-5cb312fad15f)


## 📤 Inference on the test set
The visualization below showcases the model’s predictions on 20 images from the test set. Each image includes both the predicted class as well as the prediction probabiliy.

![image](https://github.com/user-attachments/assets/9732a483-fed1-4fa6-a7d7-4b350bb69ade)


## ✅ Test Set Accuracy

After training with the defined configuration, the model achieved 92% accuracy on the test set, as evaluated on Kaggle's leaderboard.

![image](https://github.com/user-attachments/assets/944c7a60-5e1c-4382-ab2f-fc059f0b2120)

