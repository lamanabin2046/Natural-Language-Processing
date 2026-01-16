# 🧠 Word Embeddings & Semantic Search Engine  
## Assignment 1 – Natural Language Processing

This repository contains **Assignment 1** for the **Natural Language Processing** course.  
The project focuses on **training word embedding models from scratch**, **evaluating them using standard NLP benchmarks**, and **deploying them in a Flask-based semantic search engine**.

---

## Project Structure

NLP/  
├── Assignment1/  
│   ├── code/
           ├── app.py
           ├── templates
               ├──index.html
           
        
│   ├── model/  
│   ├── data/  
│   ├── templates/  
│   ├── static/  
│   └── README.md  
│  
└── Assignment2/ *(to be added later)*  

- 🔹 Git is initialized at the **Assignment/** level  
- 🔹 **Assignment2** will be added later without affecting **Assignment1**

---

## How to Run the Project

### Step 1: Navigate to Assignment1
cd Assignment1



### Step 2: Run the Flask App
python app.py

shell
Copy code

### Step 3: Open in Browser
http://127.0.0.1:5000



## Web Interface Preview

<img width="784" height="864" alt="Web Interface" src="https://github.com/user-attachments/assets/23d9266f-84ac-4678-b446-44e93480701f" />

---

## Experimental Results

### 🔹 Model Comparison

| Model | Window Size | Training Loss | Training Time (sec) | Syntactic Accuracy | Semantic Accuracy |
|------|------------|---------------|---------------------|-------------------|------------------|
| Skip-gram | 2 | 8.0564 | 433.89 | 3.33% | 0.00% |
| Skip-gram (NEG) | 2 | 14.3561 | 474.58 | 0.00% | 0.00% |
| GloVe (Scratch) | 2 | 9.5779 | 98.30 | 0.00% | 0.00% |
| GloVe (Gensim) | – | – | – | 55.45% | 93.87% |

---

### 🔹 Spearman Correlation (Word Similarity)

| Model | Spearman Correlation |
|------|---------------------|
| Skip-gram | 0.1058 |
| Skip-gram (NEG) | 0.0241 |
| GloVe (Scratch) | 0.0510 |
| GloVe (Gensim) | 0.53 |

---

## Observations

- All **scratch-trained models** performed poorly on syntactic and semantic analogy tasks.
- This behavior is expected due to:
  - Small corpus size  
  - Low embedding dimensions  
  - Limited context window  
- **Pretrained GloVe (Gensim)** embeddings significantly outperformed all scratch models.
- Near-zero Spearman correlations indicate weak alignment with human similarity judgments for scratch models.

---

## Why Scratch Models Perform Poorly

Training word embeddings from scratch is challenging because:

- Word embedding models require **large corpora** to learn meaningful relationships.
- Limited data leads to **noisy and unreliable embeddings**.

Pretrained models benefit from:
- Billions of training tokens  
- Carefully tuned hyperparameters  
- Optimized training pipelines  

---

## Conclusion

This assignment demonstrates:

- Strong conceptual understanding of **word embedding algorithms**
- Practical challenges in **training embeddings from scratch**
- Model evaluation using **standard NLP benchmarks**
- Deployment of embeddings in a **real-world semantic search engine**
- Clear performance gap between **scratch and pretrained models**

---

## Future Improvements

- Increase corpus size  
- Increase embedding dimension  
- Tune learning rate and number of epochs  
- Use **FastText** for subword embeddings  
- Extend search from **word-level** to **sentence-level similarity**  
- Add **Assignment 2** in a separate folder  

---

## Important Notes

- `model_gensim.pkl` is excluded from the repository due to **GitHub file size limits**
- The pretrained model can be regenerated using **Gensim** during runtime

---

## Author

- **Name:** Nabin Gangtan Lama
- **Course:** Natural Language Processing  
- **Semester:** Second Semester  
- **University:** Asian Institute of Technolog, Master in Data Science and Artificial Intelligence  


