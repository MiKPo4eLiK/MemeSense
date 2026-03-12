**MemeSense**

MemeSense is a multimodal AI system that automatically classifies memes into categories using 
both **image content** and **text extracted from the meme**.

The model combines computer vision and natural language processing
to understand memes more accurately.


## Features

- Upload a meme image through a web interface
- Automatic text extraction using OCR
- Multimodal neural network combining image and text features
- Meme classification into categories
- Confidence score for predictions
- Simple web interface built with Flask


## Model Architecture

The system uses a multimodal deep learning model:

- Image encoder: CNN (ResNet-based feature extractor)
- Text encoder: DistilBERT
- Fusion layer: combines image and text embeddings
- Classifier: predicts meme category

Pipeline:

1. User uploads a meme
2. OCR extracts text from the image
3. Image → CNN encoder
4. Text → DistilBERT encoder
5. Features are fused in a multimodal model
6. The model predicts the meme category


## Meme Categories

The model classifies memes into the following categories:

- "animal_meme"
- "dark_humor_meme"
- "reaction_meme"
- "screenshot_meme"
- "text_meme"


## Web Interface

The web interface allows users to:

- Upload a meme image
- Run AI classification
- See prediction results and confidence score

Built with:

- Python
- Flask
- HTML + CSS


##  Technologies Used

- Python
- PyTorch
- Transformers (HuggingFace)
- DistilBERT
- OpenCV / PIL
- Tesseract OCR
- Flask
- HTML / CSS


## Installation
⚠️ Important: Large Files (Git LFS)
This project uses Git LFS to store model weights (.pt and .pth files).
Before cloning, ensure you have Git LFS installed:

Download and install Git LFS.

Run git lfs install in your terminal.

--- Clone the repository

git clone https://github.com/yourusername/MemeSense.git
cd MemeSense
**Ensure large files are downloaded**
git lfs pull

--- Create a virtual environment

python -m venv venv
Activate it:

Windows:
venv\Scripts\activate

Mac/Linux:

source venv/bin/activate


---Install dependencies

pip install -r requirements.txt

---Install Tesseract OCR

Download Tesseract and install it.
Then set the path in the code:

pytesseract.pytesseract.tesseract_cmd = r"PATH_TO_TESSERACT\tesseract.exe"

--- Running the Application

Start the Flask server:

python app.py

Then open in your browser:

http://127.0.0.1:5000


## Interface

**Main Page**
![Main Page](screenshots/MemeSense_page_1.png)
![Main Page](screenshots/MemeSense_page_1(1).png)

**Result Page**
![Result Page](screenshots/MemeSense_page_2.png)

**Training vs Validation loss**
![Training vs Validation loss](screenshots/MemeSense_training_validation_loss.png)

**Validation accuracy**
![Validation accuracy](screenshots/MemeSense_validation_accuracy.png)


## 📁 Project Structure
MemeSense
├───.idea
│   └───inspectionProfiles
├───data
│   ├───test
│   │   ├───animal_meme
│   │   ├───dark_humor_meme
│   │   ├───reaction_meme
│   │   ├───screenshot_meme
│   │   └───text_meme
│   ├───train
│   │   ├───animal_meme
│   │   ├───dark_humor_meme
│   │   ├───reaction_meme
│   │   ├───screenshot_meme
│   │   └───text_meme
│   └───val
│       ├───animal_meme
│       ├───dark_humor_meme
│       ├───reaction_meme
│       ├───screenshot_meme
│       └───text_meme
├───ml
│   ├───fusion
│   │   └───__pycache__
│   ├───image
│   ├───preprocessing
│   ├───temporary
│   ├───text
│   │   └───__pycache__
│   └───__pycache__
├───screenshots
├───static
├───templates
└───venv
