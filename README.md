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

Download the following files from the [Releases](https://github.com/grishmas47/captionary_image_captioning/releases) page:

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

## Dataset and Evaluation

The model was trained on the **MS COCO dataset**, containing over **80,000 annotated images**. It was evaluated using the **BLEU metric**, achieving:

* **BLEU-1:** 0.4411
* **BLEU-2:** 0.1644
* **BLEU-3:** 0.0552
* **BLEU-4:** 0.0268

The results show that the model can recognize key visual elements and generate meaningful captions.

## Limitation

The model performs better on simple scenes but may generate less accurate or less fluent captions for complex images with multiple objects and relationships. The low **BLEU-4 score of 0.0268** also indicates limited phrase-level fluency.

