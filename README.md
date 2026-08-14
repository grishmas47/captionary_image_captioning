# Captionary

Captionary is an image captioning system that generates descriptive captions for images using **ResNet50**, **LSTM**, and an **attention mechanism**. The project uses a **Flask web interface** for image upload and caption generation.

## Technologies Used

* Python
* TensorFlow / Keras
* ResNet50
* LSTM
* Attention Mechanism
* Flask
* MS COCO 2014 Dataset

## Setup

### 1. Clone the repository

```bash
git clone <repository-url>
cd <repository-folder>
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

### 3. Activate the virtual environment

**Windows**

```bash
venv\Scripts\activate
```

**macOS/Linux**

```bash
source venv/bin/activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Add Model Files

Place the trained model/checkpoint files and tokenizer in the required project folders before running the application.

### 6. Run the Application

```bash
python app.py
```

Open:

```text
http://127.0.0.1:5000/
```

## How to Use

1. Open the application in your browser.
2. Upload an image.
3. Click **Generate Caption**.
4. The generated caption will be displayed with the uploaded image.

The model uses ResNet50 for feature extraction and an LSTM-based decoder with attention to generate captions. Beam search is used during inference.

