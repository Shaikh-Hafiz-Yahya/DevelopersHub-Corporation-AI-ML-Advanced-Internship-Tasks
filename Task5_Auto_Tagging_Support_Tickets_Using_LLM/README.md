# 🎫 Task 5: Auto Tagging Support Tickets Using LLM

## 📝 Project Overview
The objective of this task was to automate the classification of customer support tickets using a **Large Language Model (LLM)**. By leveraging **Prompt Engineering** and **Zero/Few-Shot Learning**, we transformed unstructured text into structured, actionable tags.

---

## 🚀 Technical Implementation

### 1. Model Selection
- **Model:** `TinyLlama-1.1B-Chat-v1.0`
- **Why?** Runs locally on Google Colab's T4 GPU, bypassing external API provider errors and task-compatibility issues.

### 2. Learning Techniques
- **Zero-Shot Learning:** Instructions provided via System Prompts.
- **Few-Shot Learning:** Enhanced accuracy using in-context examples.
- **Prompt Engineering:** Structured output for top 3 probable tags.

---

## 🛠️ Tech Stack & Environment
- **Platform:** Google Colab (T4 GPU)
- **Frameworks:** `transformers`, `torch`, `LangChain`

---

## 📂 How to Execute
1. Open the `.ipynb` file in **Google Colab**.
2. Set Runtime to **T4 GPU**.
3. Use your own Hugging Face token:
   ```python
   os.environ["HUGGINGFACEHUB_API_TOKEN"] = "ENTER_YOUR_TOKEN_HERE"
