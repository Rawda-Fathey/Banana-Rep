# 🍌 Banana Ripeness Detection Using Deep Learning

A lightweight deep learning model for detecting banana ripeness using a fine-tuned [MobileNetV2](https://arxiv.org/abs/1801.04381) architecture. This model classifies bananas into four stages: **Unripe**, **Partially Ripe**, **Ripe**, and **Overripe**, achieving **92% accuracy** and enabling real-time deployment on mobile and edge devices.

## 📊 Project Highlights

- 🔍 **Model**: Fine-tuned MobileNetV2 (transfer learning with ImageNet weights)
- 🏷️ **Classes**: Class A (Unripe), Class B (Partially Ripe), Class C (Ripe), Class D (Overripe)
- 📈 **Accuracy**: 92% on 699 real test samples
- 🧠 **Optimizer**: Adam with learning rate of `5e-5`
- 📦 **Input**: 224×224 RGB images
- ⚡ **Inference Time**: 8.20 ms/sample (0.56 GFLOPS)
- 📱 **Deployment Ready**: Lightweight for edge/mobile usage

## 📂 Dataset

The dataset is based on a combination of real and synthetic banana images:

- 📸 **Real images**: 2,400 (600 per class)
- 🧪 **Synthetic images**: 1,200 (300 per class)
- 📈 **Augmented training set**: ~12,000 images
- 🗂️ **Image size**: 224×224 pixels

🔗 **[Download Dataset on GitHub](https://github.com/luischuquim/BananaRipeness)**

## 🛠️ Data Preprocessing

- Rescaling pixel values to [0, 1]
- Extensive augmentation:
  - Rotation (±30°)
  - Width & height shift (±30%)
  - Zoom (±30%)
  - Shear (±0.3)
  - Brightness variation (0.8–1.2)
  - Horizontal & vertical flipping

## 🧪 Training Setup

- Frameworks: TensorFlow 2.x, Keras 3.8.0
- GPU: NVIDIA Tesla T4 (Colab)
- Epochs: 50 (early stopping with patience=5)
- Batch Size: 32
- Loss Function: Categorical Crossentropy (with class weights)
- Validation strategy with checkpoints for best model

## 🧠 Model Architecture


