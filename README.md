# Captionary

Captionary is an image captioning system that generates descriptive captions for uploaded images using ResNet50, LSTM, and an attention mechanism.

## Technologies Used

- Python
- TensorFlow / Keras
- ResNet50
- LSTM
- Flask
- MS COCO Dataset

## Setup

### 1. Clone the repository

git clone <repository-url>
cd <repository-folder>

### 2. Create a virtual environment

python -m venv venv

Activate it:
venv\Scripts\activate

### 3. Install dependencies

pip install -r requirements.txt

### 4. Add the trained model files

Place the trained model/checkpoint and tokenizer files in their required directories.

### 5. Run the application

python <main-flask-file>.py

Open the local URL shown in the terminal in your browser.

## How to Use

1. Open the application in your browser.
2. Upload an image.
3. Click **Generate Caption**.
4. The system processes the image using ResNet50.
5. The LSTM decoder generates a caption.
6. The generated caption is displayed with the uploaded image.

## Model

The system uses ResNet50 for extracting image features and an LSTM-based decoder with attention to generate captions word by word. Beam search is used during inference to improve caption generation.
