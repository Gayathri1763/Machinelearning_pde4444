# Bottle Orientation Detection using MobileNetV2 (Transfer Learning)

## 📌 Project Overview
This project detects the orientation of a bottle using a deep learning model based on **MobileNetV2**. The system classifies whether a bottle is placed correctly (**PASS**) or incorrectly (**FAIL**) using real-time input from a laptop camera.

Unlike a basic CNN, this model uses **transfer learning with fine-tuning** to achieve better accuracy and faster training.

---

## 🎯 Objective
- Detect bottle orientation in real-time  
- Classify as:
  - **PASS** → Bottle is upright  
  - **FAIL** → Bottle is not upright  

---

## 🧠 Model Architecture

### 🔹 Base Model
- **MobileNetV2 (pre-trained on ImageNet)**
- Used as a feature extractor

### 🔹 Custom Layers Added
- Global Average Pooling Layer  
- Dense Layer (ReLU activation)  
- Output Layer (Sigmoid activation for binary classification)

---

## 🔄 Transfer Learning & Fine-Tuning

- Initially, all layers of MobileNetV2 were **frozen**
- Only the custom top layers were trained
- Later, **top layers of MobileNetV2 were unfrozen** for fine-tuning
- Fine-tuning performed using a **low learning rate**

---

## ⚙️ Training Details

- **Activation Function:** ReLU (best performance)
- **Optimizer:** Adam (faster convergence and higher accuracy)
- **Loss Function:** Binary Crossentropy
- **Image Size:** 224 x 224
- **Batch Size:** 32

---

## 📂 Dataset
- ~400+ images for **PASS**
- ~400+ images for **FAIL**
- Captured using laptop webcam
- Split into training and validation sets

---

## 📷 Real-Time Detection
- Uses OpenCV for webcam input  
- Captures live frames  
- Model predicts bottle orientation instantly  
- Displays result:
  - PASS → upright bottle  
  - FAIL → incorrect orientation  

---

## 🛠️ Technologies Used
- Python  
- TensorFlow / Keras  
- OpenCV  
- NumPy  

---

## 📊 Results
- Transfer learning significantly improved performance  
- Fine-tuning increased accuracy further  
- Adam optimizer outperformed SGD  
- ReLU performed best among tested activation functions  

---

## ⚠️ Limitations
- Dataset size is relatively small  
- Sensitive to lighting and background variations  
- Limited generalization to unseen bottle types  

---

## 🚀 Future Improvements
- Increase dataset size and diversity  
- Apply advanced data augmentation  
- Optimize model for embedded/IoT deployment  
- Improve robustness to real-world conditions  

---

## 👩‍💻 Author
Gayathri Satheesh.L
