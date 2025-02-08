# RAG-for-Movie-Plot-Question-Answering
# Retrieval-Augmented Generation (RAG) for Movie Plot Question Answering

## 📌 Project Overview
This project implements a **Retrieval-Augmented Generation (RAG)** pipeline for answering questions about movie plots. It combines **FAISS** for efficient text retrieval and **DistilBERT** for answer generation. The system first retrieves the most relevant movie plots and then generates accurate responses based on the retrieved data.

🚀 **Live Demo:** [Colab Notebook](https://colab.research.google.com/drive/1irEsl-Ql_4_q1aoi6SqwOVcvQWsw0aej?usp=sharing)  
📂 **Dataset:** [Wikipedia Movie Plot Dataset](https://drive.google.com/file/d/1adAS8noPDqq5NfQPuBNJm7ejl-l8aNSL/view?usp=sharing)

---

## 🎯 Project Objective
- Build a system capable of answering questions related to **movie plots**.
- Utilize **FAISS** for fast and efficient text retrieval.
- Use **DistilBERT** to generate accurate answers based on retrieved data.
- Track performance using **Weights & Biases (W&B)** for model logging and evaluation.

---

## ⚙️ Pipeline Overview

1️⃣ **Data Preprocessing** 📝  
   - Cleaned and structured the dataset.
   - Removed unnecessary characters and standardized text formatting.

2️⃣ **Text Retrieval using FAISS** 🔍  
   - Used **MiniLM embeddings** to convert plots into vectors.
   - Indexed the dataset using **FAISS** for fast similarity search.
   - Retrieved relevant movie plots based on user queries.

3️⃣ **Answer Generation with DistilBERT** 🤖  
   - Used retrieved movie plots as context.
   - Applied **DistilBERT (fine-tuned on SQuAD)** for answer generation.

4️⃣ **Experimentation & Hyperparameter Tuning** ⚡  
   - Tuned learning rate, optimizer (Adam/SGD), and batch size.
   - Logged experiments using **Weights & Biases (W&B)**.

---

## 🛠️ Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/RAG-MovieQA.git
cd RAG-MovieQA
```

### 2️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 3️⃣ Run the Streamlit App (Optional UI)
```bash
streamlit run app.py
```

---

## 🖥️ Example Usage
### **Query:** _"What is the plot of a movie about space travel?"_
### **Response:**
> *The movie follows an astronaut stranded on Mars, struggling to survive and communicate with Earth while facing immense challenges...*

---

## 📊 Results & Findings
- **Learning Rate 0.0005** provided the best trade-off between speed and accuracy.
- **Adam Optimizer** performed better than SGD in terms of convergence speed.
- **Batch Size of 8** was optimal for efficient training.

---

## 🚀 Future Enhancements
- Integrate with **Gradio/Streamlit** for a better UI.
- Experiment with **ColBERT or BM25** for improved retrieval.
- Deploy as an API for real-time Q&A.

---

## 👨‍💻 Author
- **Abhisekh Kumaar**  
  [LinkedIn](https://www.linkedin.com/in/aveseq) | [GitHub](https://github.com/aveseq)

---

## 📝 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

📢 _Feel free to fork this repo, open issues, or submit PRs!_ 🎉

