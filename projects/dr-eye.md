# Dr.eye 

**Project Type**: Machine learning


---

## Table of Contents

1. [Introduction](#introduction)
3. [Retinopathy diabetic](#retinopathy-diabetic)
6. [Dataset](#dataset)
7. [Model Architecture / System Design](#model-development)
8. [Results](#results)
8. [Model deployment](#model-deployment)
5. [Technologies Used](#technologies-used)
8. [Next steps](next-steps)
8. [Installation](#installation)
9. [Resources](#contributing)

---

## Introduction

In certain rural African villages, accessing an ophthalmologist is a luxury. Individuals suffering from eye diseases often lack proper treatment due to the scarcity of specialists, leading to a worsening of their conditions and frequently resulting in blindness, particularly for those with diabetic retinopathy. This project propose an AI system capable of automatically detecting stages of retinopathy from fundus images.

- Take eye fondus with a specific tool and send it to server
- The eye fondus follow some processing and then give to the model to get the corresponding Retinopathy stage
- Return the response to the user

## Retinopathy diabetic

Diabetic Retinopathy (DR) is a diabetes-related eye disease that damages the blood vessels in the retina, the light-sensitive tissue at the back of the eye.

It is one of the leading causes of blindness among working-age adults worldwide.

| **Stage**                                      | **Description**                                                                                           | **Symptoms**                            |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------|
| **Mild Non-Proliferative Diabetic Retinopathy** | Early stage where small areas of balloon-like swelling (microaneurysms) occur in the retina's blood vessels. | Usually no symptoms or mild blurred vision. |
| **Moderate Non-Proliferative Diabetic Retinopathy** | Blood vessels become more damaged, potentially leading to poor blood flow and swelling in the retina.        | Some blurring or vision changes may occur. |
| **Severe Non-Proliferative Diabetic Retinopathy** | A larger portion of the retina's blood vessels are blocked, leading to deprivation of blood flow.            | More noticeable vision changes, risk of progression to advanced stages. |
| **Proliferative Diabetic Retinopathy (PDR)**    | The most advanced stage where abnormal blood vessels grow on the retina, which can rupture and cause bleeding. | Blurred vision, dark spots, vision loss, potential retinal detachment. |

---
## Dataset

- **Dataset**: Retinopathy is obtained from Kaggle: [APTOS 2019 Blindness Detection](https://www.kaggle.com/competitions/aptos2019-blindness-detection/data)

## Model Development

- **Model architecture**: CNNs based model (VGG16, Resnet, custom CNNS RetNet)
- **Metrics evaluation**: Accuracy, precision, Recall
- **Model training**: On local computer and Google Colab using the free GPU access.

## Results

This benchmark compares the performance of various CNN architectures, including a custom architecture named **RetNet**, on three key metrics: accuracy, precision, and recall. The models evaluated are **VGG16**, **ResNet50**, **InceptionV3**, **MobileNetV2**, and **RetNet**.

| Model         | Accuracy (%) | Precision (%) | Recall (%) |
|---------------|--------------|---------------|------------|
| **VGG16**     | 88.50        | 85.75         | 87.00      |
| **ResNet50**  | 91.25        | 89.10         | 90.50      |
| **InceptionV3**| 93.40       | 92.00         | 92.50      |
| **MobileNetV2**| 89.75       | 88.20         | 88.50      |
| **RetNet (Custom)**| 94.10   | 93.30         | 93.90      |

- **RetNet** achieves the highest performance in all three metrics, outperforming even the state-of-the-art models like **InceptionV3** and **ResNet50**.
- **InceptionV3** is the second-best performer, showing excellent accuracy and recall.
- **VGG16** and **MobileNetV2** show slightly lower performance but are still competitive.

## Model deployment
- The model is accessible through a Flask API endpoint
- The frontend is in React 
## Technologies Used
- Python, PyTorch, Flask, OpenCV etc.

## Next steps
- Running Model on the smartphone
- Adapt lense to take the eye fundus with smartphone.

## Installation

Step-by-step instructions on how to install and run your project locally.

```bash
# Clone the repository
git clone https://github.com/abari111/dr-eye.git

# Change directory into the project folder
cd dr-eye

# Install dependencies
pip install -r requirements.txt 

