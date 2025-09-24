# 🧠 Creating a NeuralNet from Scratch

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/13oSw_IH0qsj81Pzwae11NdgNt-GmmxRf?usp=sharing)

## 📂 Project Structure

The first step was building a base `Layer` class.  
From there, I created two specific types:  

- `Dense`  
- `ActivationLayer`  

Both inherit from `Layer`.  

Then comes the `Network` class, which is in charge of training the neural net.  

For optimization, I went with **ADAM**.  
It takes the gradients from `Network.train()` and updates parameters using their first and second moments.  

## 📊 Results & Interpretations

I trained two models—one for regression and one for binary classification.  

### 🔬 Classification Task
- Dataset: **Wisconsin Breast Cancer**  
- Goal: Predict if a tumor is benign or not.  
- Accuracy: **96.9% (Train)** & **97.7% (Test)** ✅  

### 🏡 Regression Task
- Dataset: **California Housing**  
- Goal: Predict housing prices from the dataset’s features.  
- Performance: *Mean Squared Error* of **0.4071**  
  - On average, predictions were off by about **$4,071** (prices are in units of **$100,000**).
