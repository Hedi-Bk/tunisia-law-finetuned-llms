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

Fine-tuned versions of the Qwen3 8B model on Tunisian Law datasets.  
Two training configurations are available:
- **2 Epochs**
- **3 Epochs**

---

### 🔸 Qwen3 8B — 2 Epochs

#### LoRA Adapter
- Hugging Face:  
  [Hedi-Bk/qwen3_8B-tunisian-law-lora-2epochs](https://huggingface.co/Hedi-Bk/qwen3_8B-tunisian-law-lora-2epochs?utm_source=chatgpt.com)

#### GGUF Quantized Version
- Hugging Face:  
  [Hedi-Bk/qwen3_8B-tunisian-law-gguf-2-epochs](https://huggingface.co/Hedi-Bk/qwen3_8B-tunisian-law-gguf-2-epochs?utm_source=chatgpt.com)

#### vLLM Version
- Hugging Face:  
  [Hedi-Bk/qwen3_8B-tunisian-law-vllm-2epochs](https://huggingface.co/Hedi-Bk/qwen3_8B-tunisian-law-vllm-2epochs?utm_source=chatgpt.com)

---

### 🔸 Qwen3 8B — 3 Epochs

#### LoRA Adapter
- Hugging Face:  
  [Hedi-Bk/qwen3_8B-tunisian-law-lora-3epochs](https://huggingface.co/Hedi-Bk/qwen3_8B-tunisian-law-lora-3epochs?utm_source=chatgpt.com)

#### GGUF Quantized Version
- Hugging Face:  
  [Hedi-Bk/qwen3_8B-tunisian-law-gguf-3epochs](https://huggingface.co/Hedi-Bk/qwen3_8B-tunisian-law-gguf-3epochs?utm_source=chatgpt.com)

#### vLLM Version
- Hugging Face:  
  [Hedi-Bk/qwen3_8B-tunisian-law-vllm-3epochs](https://huggingface.co/Hedi-Bk/qwen3_8B-tunisian-law-vllm-3epochs?utm_source=chatgpt.com)

---

## 🔹 Gemma 4 E4B Models

Fine-tuned versions of the Gemma 4 E4B model on Tunisian Law datasets.  
Two training configurations are available for only **3 Epochs** which is more better tha 2 epohcs 

---

### 🔸 Gemma 4 E4B — 3 Epochs

#### LoRA Adapter
- Hugging Face:  
Soon
#### GGUF Quantized Version
- Hugging Face:  
Soonn
#### vLLM Version
- Hugging Face:  
Soon

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
- PEFT / LoRA
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
