# Fake-news-Detection-98%-Accuracy-

![Fake News Detection](https://img.shields.io/badge/Flask-v2.0.3-blue.svg) ![PyTorch](https://img.shields.io/badge/PyTorch-v1.12.1-orange.svg) ![Transformers](https://img.shields.io/badge/Transformers-v4.24.0-green.svg)

This project implements a **Fake News Detection** system using a fine-tuned **BERT (Bidirectional Encoder Representations from Transformers)** model. The goal of the project is to classify news headlines as either **Real News** or **Fake News**. The model is deployed using **Flask** as a web application, where users can input a news headline and receive a prediction.

---

## **Features**

- Fine-tuned BERT model for text classification.
- Flask-based web application for user interaction.
- Simple and clean user interface with a responsive design.
- Dynamic display of predictions (Real or Fake).
- Supports both CPU and GPU environments for inference.

---

## **Technologies Used**

### **Backend**

- **Python**: Programming language.
- **PyTorch**: Used for fine-tuning the BERT model.
- **Hugging Face Transformers**: For pre-trained BERT models and tokenization.
- **Flask**: Micro web framework for deploying the application.

### **Frontend**

- **HTML**: Structure of the web page.
- **CSS**: Styling for the user interface.
- **JavaScript**: For interactivity and handling form submissions.

---

## **Project Structure**

```
fake-news-detection-project/
│
├── app.py               # Flask application
├── saved_model/         # Folder containing the fine-tuned BERT model and tokenizer
│   ├── config.json
│   ├── model.safetensors
│   ├── special_tokens_map.json
│   ├── tokenizer_config.json
│   └── vocab.txt
│
├── templates/           # HTML template for the web app
│   └── index.html
│
├── static/              # Static files (CSS, JS)
│   └── style.css
│
└── requirements.txt     # List of Python dependencies
```

---

## **Setup and Installation**

Follow these steps to set up the project locally and run the Flask app:

### **1. Clone the Repository**

```bash
git clone https://github.com/your-username/fake-news-detection.git
cd fake-news-detection
```

### **2. Create and Activate a Virtual Environment**

- On **Windows**:
  ```bash
  python -m venv venv
  venv\Scripts\activate
  ```

- On **Linux/Mac**:
  ```bash
  python3 -m venv venv
  source venv/bin/activate
  ```

### **3. Install Dependencies**

```bash
pip install -r requirements.txt
```

### **4. Run the Flask App**

```bash
python app.py
```

The app will be running at `http://127.0.0.1:5000/`. Open this URL in your browser.

---

## **How to Use the Application**

1. Open the app in your browser at `http://127.0.0.1:5000/`.
2. Enter a news headline in the provided text box.
3. Click the **"Check News"** button.
4. The app will display whether the headline is **Real News** or **Fake News**.

---

## **Dataset**

The dataset used for training the BERT model is from the [Fake and Real News Dataset](https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset) on Kaggle, which contains two CSV files:
- **Fake.csv**: Contains fake news headlines.
- **True.csv**: Contains real news headlines.

---

## **Training the Model**

To train the BERT model, follow these steps:

1. Load the dataset (`Fake.csv` and `True.csv`) and label the data (0 for fake, 1 for real).
2. Tokenize the news headlines using the **BERT tokenizer**.
3. Fine-tune a pre-trained **BERT base model** for binary classification using **PyTorch**.
4. Save the fine-tuned model and tokenizer using:
   ```python
   model.save_pretrained("saved_model")
   tokenizer.save_pretrained("saved_model")
   ```

---

## **Example Prediction**

Here’s a sample input and the corresponding prediction:

- **Input**: `"President announces new economic reforms to boost the economy."`
- **Prediction**: `Real News`

- **Input**: `"Aliens have landed on Earth and taken over the government."`
- **Prediction**: `Fake News`


## **Future Enhancements**

- Add support for longer news articles (beyond headlines).
- Improve the UI/UX with animations and real-time feedback.
- Deploy the app on cloud platforms like **Heroku** or **AWS** for public access.

---

## **License**

This project is licensed under the **MIT License**.


This README file should be sufficient for your GitHub repository. It provides a detailed explanation of the project, setup instructions, and usage guide. Make sure to replace placeholders like `"your-username"` and `"your-email@example.com"` with your actual information.

Let me know if you need further modifications!
