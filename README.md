# Captionary

Captionary is an image captioning system that generates descriptive captions for images using **ResNet50**, **LSTM**, and an **attention mechanism**. It includes a **Flask web interface** for uploading images and generating captions.

## Technologies Used

* Python
* TensorFlow / Keras
* ResNet50
* LSTM
* Attention Mechanism
* Flask
* MS COCO 2014 Dataset

## Project Structure

```text
captionary_image_captioning/
├── coco_checkpoints/   # Trained model checkpoint files
├── static/             # CSS and frontend assets
├── templates/          # HTML templates
├── app.py              # Main Flask application
├── tokenizer.pkl       # Saved tokenizer
├── requirements.txt    # Project dependencies
├── .gitignore
└── README.md
```

> The `coco_checkpoints/` folder is not included in the repository. Download the required checkpoint files from the GitHub Releases page.

## Setup

### 1. Clone the Repository

```bash
git clone https://github.com/grishmas47/captionary_image_captioning.git
cd captionary_image_captioning
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

### 3. Activate the Virtual Environment

**Windows**

```bash
venv\Scripts\activate
```

**macOS/Linux**

```bash
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Add Model Files

Download the following files from the [Releases](../../releases) page:

* `checkpoint`
* `ckpt-100.index`
* `ckpt-100.data-00000-of-00001`

Create a `coco_checkpoints/` folder in the project root and place all three files inside it:

```text
coco_checkpoints/
├── checkpoint
├── ckpt-100.index
└── ckpt-100.data-00000-of-00001
```

### 6. Run the Application

```bash
python app.py
```

Open the application in your browser:

```text
http://127.0.0.1:5000/
```

## How to Use

1. Open the application in your browser.
2. Upload an image.
3. Click **Generate Caption**.
4. View the generated caption.

