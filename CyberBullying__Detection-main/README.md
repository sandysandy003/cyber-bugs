# CyberBullying Detection Application

A text-based Python application that analyzes user-entered sentences to identify potentially harmful or cyberbullying content. The system utilizes Natural Language Processing (NLP) techniques and machine learning to generate a cyberbullying score, helping users understand the severity of harmful content in real time.

## Features
* **Real-Time Classification:** Instant evaluation of user-submitted sentences.
* **Harm Analysis:** Calculates a cyberbullying score/prediction based on text features.
* **Web UI Interface:** Built with a clean frontend (Flask/HTML templates) for accessible user interaction.
* **Modular Pipeline:** Distinct separation between data processing, model training, and application deployment.

## Architecture & Technologies
* **Language:** Python
* **Machine Learning & NLP:** Scikit-learn, Natural Language Processing, Feature Extraction (TF-IDF/Vectorization)
* **Classification Model:** Logistic Regression
* **Deployment & UI:** Flask (via `app.py` and HTML templates)

## Repository Structure
```text
├── data/              # Dataset files used for model training
├── models/            # Serialized machine learning models and pipelines
├── saved_models/      # Backups of trained classification models
├── templates/         # HTML frontend layouts for the web application
├── app.py             # Main Flask application script for execution
├── train_model.py     # Script to preprocess text and train the Logistic Regression model
├── requirements.txt   # File listing all required Python dependencies
└── pyvenv.cfg         # Virtual environment configuration setup
```

## Installation & Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com
   cd CyberBullying__Detection
   ```

2. **Set Up a Virtual Environment (Optional but Recommended):**
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

##  Usage

### 1. Training the Model
If you want to train or retrain the Logistic Regression classifier on your data, run:
```bash
python train_model.py
```
This script processes the text inside the `data/` directory, extracts features, trains the model, and saves the output to the `models/` or `saved_models/` folder.

### 2. Running the Application
To launch the interactive text-analysis web interface, execute:
```bash
python app.py
```
Open your web browser and navigate to the local host address provided in your terminal (usually `http://127.0.0`) to start analyzing text sentences.
