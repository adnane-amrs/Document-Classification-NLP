🚀 Intelligent Document Classification (NLP)

An End-to-End Natural Language Processing solution designed to automatically categorize documents into four strategic themes: Medicine, Space, Computer Graphics, and Automotive. Developed as part of the Master D3SI (Data Science and Information Systems Security) at Université Sultan Moulay Slimane.

📌 Project Overview

This project implements a 1D Convolutional Neural Network (CNN) for text classification. Unlike traditional statistical models, this architecture captures local semantic patterns (n-grams), providing high performance with a balanced trade-off between complexity and computational cost.

Key Features:

Dual Format Support: Classifies both raw .txt files and .pdf reports.

Interactive UI: A modern web interface built with Gradio for real-time predictions.

Performance: Achieved ~83% accuracy on the test set using a curated subset of the 20 Newsgroups dataset.

Preprocessing Pipeline: Full linguistic normalization (lower-casing, regex cleaning, and stop-word removal).

🛠️ Tech Stack

Deep Learning: TensorFlow / Keras (CNN 1D Architecture)

Linguistics: NLTK (Stopwords), Regex

Data Science: Scikit-Learn, Pandas, NumPy

PDF Extraction: PyPDF

UI/Deployment: Gradio

Environment: Jupyter Notebook / Python 3.10+

📁 Repository Structure

nlp-document-classification/
├── data/                         # Test samples (.pdf and .txt)
├── notebooks/                    
│   └── document_classification.ipynb  # Full research, training, and evaluation
├── src/                          
│   └── app.py                    # Standalone Gradio application script
├── rapport_mini_project_nlp.pdf  # Full academic report (French)
├── requirements.txt              # List of dependencies
└── README.md                     # Project documentation


🏗️ Model Architecture

The CNN model consists of the following layers:

Embedding Layer: Maps 10,000 unique words into 100-dimensional dense vectors.

1D Convolution Layer: 128 filters with a kernel size of 5 to detect local keywords.

Global Max Pooling: Reduces dimensionality by keeping only the most significant features.

Dropout (0.5): Prevents overfitting by randomly deactivating neurons during training.

Softmax Output: Provides a probability distribution over the 4 classes.

🚀 Installation & Usage

1. Clone the repository

git clone [https://github.com/your-username/nlp-document-classification.git](https://github.com/adnan-amrs/nlp-document-classification.git)
cd nlp-document-classification


2. Install dependencies

pip install -r requirements.txt


3. Run the Gradio App

python src/app.py


📊 Results

The model shows strong robustness in distinguishing technical vocabularies. The confusion matrix indicates high precision in the sci.space and sci.med categories due to highly specific technical terms.

🎓 Academic Context

University: Université Sultan Moulay Slimane, Béni Mellal

Program: Master Data Science et Sécurité des Systèmes d'information (D3SI)

Student: Adnane AMROUSS

Supervisor: Pr. ISMAIL KICH

Academic Year: 2025-2026

This project was completed as a Mini-Project for the Natural Language Processing (NLP) module.
