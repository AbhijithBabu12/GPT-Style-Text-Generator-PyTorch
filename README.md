# 💻 TinyGPT — A Transformer-based Text Generator Built From Scratch

This project implements a **mini GPT-style Transformer** built entirely from scratch using **PyTorch**.  
It includes every core component of a modern decoder-only LLM:

- Custom **tokenizer**
- Vocabulary building (stoi/itos)
- Positional encoding
- Multi-head self-attention
- Feedforward blocks
- Stacked Transformer decoder layers
- Causal masking
- Training loop with cross-entropy loss
- Text generation using **temperature** + **top-k sampling**
- Model saving/loading for inference

The goal of the project is to deeply understand how GPT-like models work internally by reconstructing the architecture step-by-step.

---

## 🚀 Features
- Fully custom Transformer architecture (no HuggingFace, no shortcuts)
- Training from scratch on your own dataset
- Generates text from a custom prompt
- Supports:
  - Temperature sampling
  - Top-k filtering
  - max_new_tokens
- Clean inference pipeline for generating new text

---

## 📁 Project Structure

├── Text_generation.ipynb # Main training + inference notebook

├── requirements.txt

├── README.md

---

## 🧩 How It Works

### 1️⃣ Tokenization
The input text is split using a custom tokenizer.  
It builds:
- `stoi` (string → index)
- `itos` (index → string)

### 2️⃣ Model Architecture
The model contains:
- Embedding layer  
- Positional encoding  
- Multi-head scaled dot-product attention  
- Feedforward network  
- LayerNorm + residual connections  
- Final linear layer to predict next token  

### 3️⃣ Training
Cross-entropy loss on next-token prediction.
loss = criterion(pred, target)
loss.backward()
optimizer.step()

### 4️⃣ Text Generation
out_idx = model.generate(
prompt_ids,
max_new_tokens=50,
temperature=1.0,
top_k=50
)

## ❤️ Sample Predictions

```text
Prompt: David was a farmer who loved his family more than anything
Generated Text:
david was a farmer who loved his family more than anything and not wanting to do anything to pay it.
in the , jim is the one who won ' t win the first time , he was going back.
when the local gangster ' s car arrives , george ' s partner ' s body was left.
  
```
---

## 👨‍💻 Author

Abhijith Babu
Passionate about ML & AI 🚀

📌 GitHub: [https://github.com/AbhijithBabu12]

📌 LinkedIn: [https://www.linkedin.com/in/abhijith-babu-856170201/]
