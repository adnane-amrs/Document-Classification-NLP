# **Document Classification with NLP and Deep Learning**

This project implements a Natural Language Processing (NLP) solution to classify textual documents into four thematic categories. By leveraging a 1D Convolutional Neural Network (CNN 1D) and an interactive interface, it allows for the rapid analysis of raw files, text files, or PDF documents.

---

## 🚀 Project Overview

The objective is to build a classifier capable of distinguishing specific themes from unstructured documents. The project follows a complete pipeline: data cleaning, vectorization, deep learning model training, and deployment.

---

## 📊 Dataset

We use the "20 Newsgroups" dataset, a standard reference in NLP. For this project, we focus on 4 target classes:

- **Medicine** (`sci.med`)
- **Space** (`sci.space`)
- **Computer Graphics** (`comp.graphics`)
- **Automobile** (`rec.autos`)

---

## 🛠️ Project Steps

## 1️⃣ Text Preprocessing

The raw text is cleaned via a custom function that performs:

- Lowercasing  
- Removal of punctuation and special characters (Regex)  
- Elimination of stop words (Stopwords) via the NLTK library  

---

## 2️⃣ Text Representation (Word Embeddings)

To transform the text into numerical data exploitable by the model:

- **Tokenization**: Creation of a 10,000-word vocabulary  
- **Sequencing**: Conversion of sentences into lists of integers  
- **Padding**: Standardization of document lengths to 200 words  

---

## 3️⃣ Model Architecture (CNN 1D)

The model uses a 1D convolutional neural network, which is effective for detecting local patterns in word sequences:

- **Embedding Layer**: Dimension of 100  
- **1D Convolution**: 128 filters with a kernel size of 5  
- **Global Max Pooling**: Extraction of the most important features  
- **Dropout (0.5)**: To prevent overfitting  
- **Dense Layer**: Final output layer with Softmax activation for the 4 classes  

---

## 4️⃣ Evaluation

The model achieves an accuracy of over **82%** on the test set.

Performance is visualized via:

- A classification report (Precision, Recall, F1-score)  
- A confusion matrix to identify potential overlaps between classes  

---

## 🌐 Deployment

The project includes a deployment interface developed with **Gradio**.

This interface allows the user to:

- Upload a `.txt` or `.pdf` file  
- Automatically extract text (using **pypdf** for PDFs)  
- Instantly obtain the thematic prediction and associated confidence scores  

### 📸 Deployment Interface Preview

<!-- Replace the path below with your actual image path -->
<img width="954" height="508" alt="image" src="https://github.com/user-attachments/assets/c21d4097-d6b9-429d-8845-53fc6037ebf5" />


---

## 📦 Installation

To run this project locally, install the necessary dependencies:

```bash
pip install numpy pandas matplotlib seaborn tensorflow nltk gradio pypdf
```

Then, launch the notebook:

```bash
jupyter notebook notebooks/document_classification.ipynb
```

---

## 📂 Repository Structure

```
project-root/
│
├── notebooks/
│   └── document_classification.ipynb
│
├── data/
│   ├── example1.pdf
│   ├── example2.txt
│
├── requirements.txt
└── README.md
```

---

## 👨‍💻 Technologies Used

- Python  
- TensorFlow / Keras  
- NLTK  
- Gradio  
- NumPy  
- Pandas  
- Matplotlib / Seaborn  

---

## 📌 Future Improvements

- Hyperparameter tuning  
- Use of pretrained embeddings (GloVe, Word2Vec)  
- Deployment on Hugging Face Spaces or cloud platforms  
- Model optimization for faster inference  

---

## 📜 License

This project is for educational and research purposes.

