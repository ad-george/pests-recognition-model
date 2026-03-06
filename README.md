# 🌿 Agricultural Pest Detection using Deep Learning

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Deep%20Learning-orange)
![CNN](https://img.shields.io/badge/Model-MobileNetV2-green)
![Gradio](https://img.shields.io/badge/UI-Gradio-red)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

An **AI-powered agricultural pest recognition system** built using **Convolutional Neural Networks (CNN)** and **Transfer Learning**.
The model classifies pest images and provides predictions through an **interactive web interface built with Gradio**.

This project demonstrates how **deep learning can assist farmers and agricultural experts** in quickly identifying pests and taking appropriate action to protect crops.


# 🎯 Project Overview

Agricultural pests cause **significant crop losses worldwide**. Manual identification of pests is often slow and requires expert knowledge.

This project builds an **automated pest recognition system** that:

* Uses **Deep Learning (CNN)** for image classification
* Applies **Transfer Learning with MobileNetV2**
* Provides **real-time predictions through a web interface**
* Displays **top pest predictions with confidence scores**

The system can be used as a **decision-support tool for smart agriculture**.


# ✨ Features

### 🧠 AI-Based Pest Recognition

* Image classification using **MobileNetV2**
* Recognizes **12 different pest types**
* Uses **transfer learning for higher accuracy**

### 📊 Automated Data Processing

* Dataset loading using TensorFlow pipelines
* Automatic **image resizing and normalization**
* **Train-validation split**


# 🧱 System Architecture

```
User Image
     │
     ▼
Image Preprocessing
(Resize + Normalize)
     │
     ▼
MobileNetV2 CNN Model
     │
     ▼
Prediction Layer
     │
     ▼
Top 3 Pest Predictions
     │
     ▼
Gradio Web Interface
```

---

# 🗂 Dataset

The model is trained on an **Agricultural Pest Image Dataset** containing labeled images of different pest categories.

| Property         | Value         |
| ---------------- | ------------- |
| Total Images     | ~6000         |
| Classes          | 12 Pest Types |
| Image Size       | 224 × 224     |
| Training Split   | 80%           |
| Validation Split | 20%           |

### Dataset Structure

```
dataset/
│
├── aphids/
│   ├── image1.jpg
│   ├── image2.jpg
│
├── armyworm/
│   ├── image1.jpg
│   ├── image2.jpg
│
├── beetle/
│   ├── image1.jpg
│   ├── image2.jpg
│
└── ...
```

Each folder represents a **pest class label**.


# 🧠 Model Architecture

This project uses **Transfer Learning with MobileNetV2**, a lightweight convolutional neural network optimized for image recognition tasks.

### Model Pipeline

```
Input Image (224x224)
        │
        ▼
Image Rescaling
        │
        ▼
MobileNetV2 (Pretrained on ImageNet)
        │
        ▼
Global Average Pooling
        │
        ▼
Dense Layer
        │
        ▼
Softmax Output (12 Classes)
```

### Why MobileNetV2?

* Lightweight architecture
* Fast training
* High accuracy
* Suitable for deployment on low-resource devices


# 📊 Training Configuration

| Parameter     | Value                           |
| ------------- | ------------------------------- |
| Image Size    | 224 × 224                       |
| Batch Size    | 64                              |
| Epochs        | 10                              |
| Optimizer     | Adam                            |
| Loss Function | Sparse Categorical Crossentropy |
| Framework     | TensorFlow / Keras              |


# 🔎 Prediction Process

When a user uploads an image:

1. Image is resized to **224 × 224**
2. Converted into a **NumPy array**
3. Passed through the **trained CNN**
4. Model outputs **class probabilities**
5. System returns **top 3 pest predictions**

### Example Output

```
Armyworm — 0.87
Aphids — 0.09
Beetle — 0.04
```


## Installation

Clone the repository:

```bash
git clone https://github.com/ad-george/agricultural-pest-detection.git
cd agricultural-pest-detection
```

Install dependencies:

```bash
pip install tensorflow numpy gradio
```


## Run the Project

Start the notebook:

```bash
jupyter notebook
```

Run all cells to:

1. Load dataset
2. Train the CNN model
3. Launch the Gradio interface


# 🌐 Web Interface (Gradio)

The project includes a **Gradio UI** where users can upload pest images and receive predictions.

After running the notebook, a link will appear:

```
Running on: https://2f3af1ca0ad2b1b4b2.gradio.live
```

Open the link and test the model by uploading an image.


# 📈 Future Improvements

Potential improvements for this project include:

* Adding **more pest classes**
* Increasing dataset size
* Improving model accuracy
* Deploying the model with **FastAPI or Flask**
* Converting the model to **TensorFlow Lite for mobile applications**
* Adding **pest treatment recommendations**
* Integrating with **smart agriculture platforms**


# 🌍 Real World Applications

This system can help:

* Farmers identify pests quickly
* Reduce crop damage
* Improve agricultural productivity
* Support **precision agriculture systems**

AI-based pest detection can significantly **improve food security and sustainable farming**.


# 🤝 Contributing

Contributions are welcome!

Steps to contribute:

1. Fork the repository
2. Create a new branch

```
git checkout -b feature/new-feature
```

3. Commit your changes

```
git commit -m "Add new feature"
```

4. Push to GitHub

```
git push origin feature/new-feature
```

5. Open a Pull Request

# 📜 License

This project is licensed under the **MIT License**.

# 👨‍💻 Author

**Onyango George**

AI / Machine Learning Enthusiast
Interested in building intelligent systems for **agriculture, AI systems**.

GitHub: [https://github.com/ad-george](https://github.com/ad-george)


⭐ **If you find this project useful, please give it a star!**
