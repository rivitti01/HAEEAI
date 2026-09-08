# 🌿 Leaf Health Classification (Healthy vs. Diseased Linden Tree Leaves)

This project provides a **machine learning model** to classify **linden tree leaves** as either **healthy** or **ill (diseased)**.  
The model was trained and optimized using **[Edge Impulse](https://www.edgeimpulse.com/)** and exported as an **Arduino library**.

The resulting model can run directly on **Arduino boards** that support TensorFlow Lite Micro.

---

## 🚀 Features

- Pre-trained **Edge Impulse** model for **Arduino-compatible MCUs**
- Classifies **healthy** vs. **ill linden leaves** in real-time
- Packaged as a ready-to-use **Arduino library**

---

## 🔧 Installation Tutorial: Deploying the Model on Arduino

Follow these steps to use the model on your Arduino board:

### 1. Install Arduino IDE

- Download and install the [Arduino IDE](https://www.arduino.cc/en/software).

### 2. Install Required Libraries

- Open Arduino IDE → **Sketch → Include Library → Manage Libraries…**
- Install:
  - **Arduino_TensorFlowLite** (official TensorFlow Lite Micro support)
  - **Arduino_LSM9DS1** or other sensor libraries (if required by your board)

### 3. Add the Edge Impulse Model Library

- Download **`mobile_160_035_8_05_97Test.zip`** from this repository.
- In Arduino IDE, go to **Sketch → Include Library → Add .ZIP Library…**
- Select the ZIP file.
- The model will now appear under:  
  **File → Examples → mobile_160_035_8_05_97Test**

### 4. Run Example Code

- Open: **File → Examples → mobile_160_035_8_05_97Test → ESP32 → ESP32_camera**
- Select your board (e.g., **ESP32S3 Dev Module**)
- Upload the sketch

### 5. Test the Model

- Provide input data (image or sensor pipeline as used in Edge Impulse).
- The model outputs:
  - `0` → Healthy Leaf
  - `1` → Diseased Leaf

---

## 🧪 Dataset

- Images of healthy and diseased **linden tree leaves**
- Preprocessed into input size **160×160** during Edge Impulse training

---

## ⚡ Model Details

- **Framework**: Edge Impulse (TensorFlow Lite Micro)
- **Architecture**: MobileNet (Tiny variant)
- **Input**: `160x160x3` RGB image
- **Output**: Binary classification (Healthy / Ill)
- **Deployment**: Optimized for low-power MCUs

---

## 📖 References

- [Edge Impulse Docs](https://docs.edgeimpulse.com/docs)
- [TensorFlow Lite for Microcontrollers](https://www.tensorflow.org/lite/microcontrollers)
- [Arduino + Edge Impulse Guide](https://docs.edgeimpulse.com/docs/development-platforms/officially-supported-mcu-targets/arduino-nano-33-ble-sense)

---

## 📌 Future Work

- Improve accuracy with more training data
- Extend classification to multiple tree species
- Add on-board image capture + preprocessing pipeline
