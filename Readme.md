# Instruction-Tuned Language Model with SFT and DPO

This repository contains code and experiments for fine-tuning a language model using Supervised Fine-Tuning (SFT) and Direct Preference Optimization (DPO) techniques. The project leverages LoRA for parameter-efficient training, was run entirely on Kaggle's free GPU T4 environment, and integrates a simple API via FastAPI.

## 📦 Features

- Supervised Fine-Tuning (SFT) with instruction data
- Direct Preference Optimization (DPO) with paired comparisons
- LoRA-based fine-tuning to reduce memory usage
- Model evaluation using BLEU scores
- Inference API using FastAPI connected to the best fine-tuned model
- Frontend integration for real-time user queries

## 🧪 Experiments

All training was conducted on Kaggle with:
- **GPU**: NVIDIA T4 (16 GB)
- **RAM**: Limited to under 15 GB
- **Environment**: Python 3.10
- **Training Time**:
  - SFT: ~170–200 minutes per trial
  - DPO: ~195–235 minutes per trial (with occasional out-of-memory errors handled via batch size/lr adjustments)

We used unsloth for training but encountered version compatibility issues on Kaggle. The final setup required multiple attempts to stabilize.

## 🚀 API Usage

A FastAPI-based server was set up locally to serve the best performing model. The API was then connected to a custom-built frontend for user interaction.

## 📂 Project Structure
├── sft-training.ipynb # Supervised fine-tuning notebook
├── dpo-training.ipynb # Direct Preference Optimization notebook
├── requirements.txt # Dependencies
└── README.md # Project readme


## 📁 Repository

The full codebase is available in this repository. For reproducibility, notebooks for SFT and DPO are provided with markdown explanations and training logs.

## 📬 Contact

For any issues or inquiries, please open an issue in the GitHub repo.
