# Fine-Tuning LLMs on Medical Reasoning Dataset  

This repository contains the implementation and results of fine-tuning multiple Large Language Models (LLMs) on the **FreedomIntelligence/medical-o1-reasoning-SFT** dataset. The project evaluates models like **DeepseekR1-Qwen1.5B, DeepseekR1-Qwen7B, DeepseekR1-Llama8B, MistralAI-8B, and Llama3.1-8B**, comparing their performance using **loss** and **perplexity** metrics.  

## 🚀 Project Overview  
- Fine-tuned LLMs using **LoRA (Low-Rank Adaptation)** for parameter-efficient training.  
- Trained on **medical reasoning** dataset to improve contextual understanding.  
- Compared performance based on **loss** and **perplexity**.  
- Visualized results using **bar charts**.  

## 📂 Dataset  
The dataset used is **[FreedomIntelligence/medical-o1-reasoning-SFT](https://huggingface.co/datasets/FreedomIntelligence/medical-o1-reasoning-SFT)**, which consists of **medical-related reasoning questions and answers**.  

## 📊 Results  
The following models were fine-tuned, and their **loss and perplexity** values are:  

| Model                  | Loss  | Perplexity |
|------------------------|------:|----------:|
| DeepseekR1-Qwen1.5B    | 1.7   | 28        |
| DeepseekR1-Qwen7B      | 1.5   | 14        |
| DeepseekR1-Llama8B     | 1.3   | 8         |
| MistralAI-8B           | 1.2   | 7.9       |
| Llama3.1-8B            | 1.2   | 6.4       |

## 🛠️ Fine-Tuning Details  
The models were fine-tuned using **LoRA** with the following configurations:  

| Hyperparameter                | Value  |
|--------------------------------|--------|
| **LoRA Rank**                  | 16     |
| **LoRA Alpha**                 | 16     |
| **Batch Size per Device**       | 2      |
| **Gradient Accumulation Steps** | 4      |
| **Epochs**                      | 3      |
| **Max Steps**                   | 70     |
| **Learning Rate**               | 2e-4   |
| **Optimizer**                   | AdamW 8-bit |
| **Weight Decay**                | 0.01   |
