# Fashion Attribute Classification using MobileNet

This project builds a **Fashion Attribute Classification System** that predicts:

* Gender (Men / Women)
* Sleeve Type (Full / Half / Sleeveless, etc.)

The model uses **Transfer Learning with MobileNet** and includes a **User Interface** for easy predictions.

---

# Project Structure

```
fashion-classifier/
│
├── gender_dataset/
│   ├── train/
│   └── val/
│
├── sleeve_dataset/
│   ├── train/
│   └── val/
│
├── gender_model.h5
├── sleeve_model.h5
│
├── train.py
├── app.py
├── requirements.txt
└── README.md
```

---

# Features

* Transfer Learning using MobileNet
* Overfitting reduction (Dropout + Augmentation)
* Separate Gender & Sleeve Models
* Simple User Interface
* High accuracy predictions

---

# Installation

## 1. Clone Repository

```
git clone https://github.com/yourusername/fashion-classifier.git
cd fashion-classifier
```

---

## 2. Create Virtual Environment (Recommended)

```
python -m venv venv
```

Activate:

Windows:

```
venv\Scripts\activate
```

Mac/Linux:

```
source venv/bin/activate
```

---

## 3. Install Dependencies

```
pip install -r requirements.txt
```

---

# Requirements.txt

Create a `requirements.txt` file:

```
tensorflow
numpy
opencv-python
matplotlib
pillow
flask
```

---

# Dataset Structure

Gender Dataset:

```
gender_dataset/
 ├── train/
 │   ├── men/
 │   └── women/
 └── val/
     ├── men/
     └── women/
```

Sleeve Dataset:

```
sleeve_dataset/
 ├── train/
 └── val/
```

---

# Training the Model

Run:

```
python train.py
```

This will:

* Train Gender Model
* Train Sleeve Model
* Save models:

```
gender_model.h5
sleeve_model.h5
```

---

# Running User Interface

Run:

```
python app.py
```

Then open browser:

```
http://127.0.0.1:5000
```

Upload an image and get:

* Gender Prediction
* Sleeve Prediction

---

# Example Workflow

1. Train models

```
python train.py
```

2. Start UI

```
python app.py
```

3. Upload image

4. Get prediction

---

# Model Architecture

* Base Model: MobileNet (Pretrained ImageNet)

* Frozen Layers: 135

* Trainable Layers: Last 20 + Custom Layers

* Custom Layers:

* GlobalAveragePooling

* Dense(128)

* Dropout(0.5)

* Output Layer

---

# Overfitting Prevention

This project includes:

* Data Augmentation
* Dropout Layer
* Fine-Tuning Last 20 Layers
* Early Stopping
* Separate Validation Set

---

# Sample Output

```
Gender: Women
Sleeve Type: Half Sleeve
Confidence: 94%
```

---

# Future Improvements

* Add Color Classification
* Add Neck Type Detection
* Deploy on Streamlit
* Convert to Mobile App

---

# Author

Arun Kumar
IIT Kanpur — Aerospace Engineering
Machine Learning & Computer Vision

---

# License

This project is open source
