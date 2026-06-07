# 🇹🇳 Tunisian Law Fine-Tuned LLMs

This repository contains links and resources for fine-tuned Large Language Models specialized in Tunisian Law.

The models were trained using Unsloth on Kaggle notebooks.

---

#  Project Goal

The objective of this project is to develop domain-specific Small Language Models (SLMs) specialized in Tunisian Law through QLoRA fine-tuning.

The models were trained on a synthetic legal instruction dataset generated using a teacher LLM. The dataset contains approximately 1,660 high-quality legal conversation examples grounded in real Tunisian legal texts and contextual legal documents.

The training data follows a conversational instruction-tuning format composed of:

- System prompts defining the legal assistant behavior
- User legal questions with supporting legal context/documents
- Structured assistant answers citing legal articles and sources

The models were fine-tuned to perform legal reasoning and legal question answering based strictly on provided legal context.

# Main Objectives

The goal of these Tunisian Law SLMs is to enable:

- Legal question answering grounded in legal documents
- Tunisian legal document understanding
- Arabic/French/Derja legal reasoning
- Efficient local inference using GGUF
- Scalable inference using vLLM
- Lightweight legal AI systems deployable on consumer hardware

---

#  Dataset Characteristics

The dataset contains multilingual Tunisian legal conversations in:

- Arabic
- Tunisian Arabic (Derja)
- French

Each example is designed to simulate realistic legal assistant interactions for the E-Tafakna legal platform.

Example capabilities include:

- Context-aware legal question answering
- Article and source citation
- Legal document understanding
- Multilingual legal reasoning
- Retrieval-style grounded responses
- Structured legal explanations

---

# Models

## 🔹 Qwen3 8B Models

Versions fine-tuned du modèle Qwen3 8B sur des datasets de droit tunisien.  
Deux configurations d'entraînement sont disponibles :
- **2 époques**
- **3 époques**

---

### 🔸 Qwen3 8B — 2 époques

#### LoRA Adapter
- Hugging Face :  
  [Hedi-Bk/qwen3_8B-tunisian-law-lora-2epochs](https://huggingface.co/Hedi-Bk/qwen3_8B-tunisian-law-lora-2epochs?utm_source=chatgpt.com)

#### GGUF Quantized Version
- Hugging Face :  
  [Hedi-Bk/qwen3_8B-tunisian-law-gguf-2-epochs](https://huggingface.co/Hedi-Bk/qwen3_8B-tunisian-law-gguf-2-epochs?utm_source=chatgpt.com)

---

### 🔸 Qwen3 8B — 3 époques

#### LoRA Adapter
- Hugging Face :  
  [Hedi-Bk/qwen3_8B-tunisian-law-lora-3epochs](https://huggingface.co/Hedi-Bk/qwen3_8B-tunisian-law-lora-3epochs?utm_source=chatgpt.com)

#### GGUF Quantized Version
- Hugging Face :  
  [Hedi-Bk/qwen3_8B-tunisian-law-gguf-3epochs](https://huggingface.co/Hedi-Bk/qwen3_8B-tunisian-law-gguf-3epochs?utm_source=chatgpt.com)

---

## **🔹 Gemma 4B Models**

Versions fine-tuned du modèle Gemma 4B sur des datasets de droit tunisien.

> **Note importante :** Bien qu'une version à 3 époques ait été entraînée, nous avons constaté que **2 époques sont largement suffisantes**. En effet, la perte finale après 2 époques était déjà très faible (**0.1075**). Chercher une perte encore plus faible augmenterait significativement le risque de **surapprentissage (overfitting)**. Nous avons donc choisi de nous arrêter à 2 époques pour un meilleur équilibre entre performance et généralisation.

---

### **🔸 Gemma 4B — 2 époques (uniquement)**

### **LoRA Adapter**

- **Hugging Face :** [Hedi-Bk/gemma-4b-tunisian-law-lora-2epochs](https://huggingface.co/Hedi-Bk/gemma-4b-tunisian-law-lora-2epochs)

### **GGUF Quantized Version**

- **Hugging Face :** [Hedi-Bk/gemma-4b-tunisian-law-gguf-2epochs](https://huggingface.co/Hedi-Bk/gemma-4b-tunisian-law-gguf-2epochs)

---

## Résumé

- **Qwen3 8B** : versions LoRA et GGUF (2 et 3 époques)
- **Gemma 4B** : versions LoRA et GGUF (2 époques)

Ces modèles sont disponibles publiquement aux adresses suivantes :

- https://huggingface.co/Hedi-Bk/qwen3_8B-tunisian-law-lora-2epochs
- https://huggingface.co/Hedi-Bk/qwen3_8B-tunisian-law-lora-3epochs
- https://huggingface.co/Hedi-Bk/qwen3_8B-tunisian-law-gguf-3epochs
- https://huggingface.co/Hedi-Bk/gemma-4b-tunisian-law-lora-2epochs
- https://huggingface.co/Hedi-Bk/gemma-4b-tunisian-law-gguf-2epochs

---

## 🔧 Correction : Réentraînement de Qwen3

Le modèle Qwen3 a été réentraîné car l'entraînement initial utilisait un mauvais chat template (pas celui de Qwen3). Les versions corrigées sont disponibles ci-dessous :

- [Hedi-Bk/qwen3-8b-tunisian-law-lora-CORRECTION-2epochs](https://huggingface.co/Hedi-Bk/qwen3-8b-tunisian-law-lora-CORRECTION-2epochs)
- [Hedi-Bk/qwen3_8B-tunisian-law-lora-CORRECTION-3epochs](https://huggingface.co/Hedi-Bk/qwen3_8B-tunisian-law-lora-CORRECTION-3epochs)
- [Hedi-Bk/qwen3_8B-tunisian-law-gguf-CORRECTION-3epochs](https://huggingface.co/Hedi-Bk/qwen3_8B-tunisian-law-gguf-CORRECTION-3epochs)

#  Fine-Tuning Notebooks

## Qwen3 8B Fine-Tuning Notebook
Kaggle:
[https://www.kaggle.com/code/bkhedi/unsloth-qween3-8b
](https://www.kaggle.com/code/bkhedi/qween3-8b-3epochs)
## Gemma 4 E4B Fine-Tuning Notebook
Kaggle:
https://www.kaggle.com/code/bkhedi/gemma4-e4b-3epochs

---

# Technologies Used

- Unsloth
- Hugging Face Transformers
- PEFT : QLoRA
- Ollama
- Kaggle
- GGUF Quantization
- Kaggle GPUs

---

# Project Goal

The objective of this project is to build domain-specific Tunisian Law language models capable of:

- Legal question answering
- Tunisian legal document understanding
- Arabic/French legal reasoning
- Efficient local inference using GGUF
- High-performance serving using vLLM

---

# 📜 License

This project is open-source and available under the MIT License.
