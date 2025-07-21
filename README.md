# 🧠 AI-Powered Trading Code Generator

This project is a Python-based interface that lets you generate trading strategy code using state-of-the-art language models. Users provide a strategy description, and the app uses either **Claude Sonnet** or **CodeQwen 1.5-7B** to produce Python functions that implement the strategy and suggest improvements.

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/RalphMaa/trade_code_generator.git
cd trade_code_generator
```

### 2. Install Dependencies

```bash
!pip install -q gradio huggingface_hub transformers anthropic
```

### 3. Add API Keys

Create a `.env` file or use the environment directly in your code. You need:

- `ANTHROPIC_API_KEY` for Claude access (get it from [Anthropic](https://www.anthropic.com))
- `HF_TOKEN` for Hugging Face access (get it from [https://huggingface.co/settings/tokens](https://huggingface.co/settings/tokens))

In a Jupyter/Colab notebook or terminal:

```python
import os
os.environ["ANTHROPIC_API_KEY"] = "your_claude_api_key"
os.environ["HF_TOKEN"] = "your_huggingface_api_key"
```

### 4. Run the App

Just open the notebook `Week4 Challenge.ipynb` and run all cells. A Gradio UI will appear where you can:

- Describe your trading strategy in a text box
- Select your preferred model (`Claude` or `CodeQwen`)
- View the generated Python code for two trading functions

## 🤖 Models Used

- **Claude Sonnet 4 (20250514)** via Anthropic API
- **CodeQwen1.5-7B-Chat** via Hugging Face endpoint:  
  👉 `https://huggingface.co/Qwen/CodeQwen1.5-7B-Chat`
(Set up an enpoint for this model using https://endpoints.huggingface.co/new?repository=Qwen/CodeQwen1.5-7B-Chat or through other cloud service providers)
  
## 🧩 How It Works

- Takes user input: a trading strategy description
- Formats the input using a custom prompt for code generation
- Uses the selected LLM (Claude or Qwen) to generate:
  - One function implementing your strategy
  - One improved version based on the model's expertise
- Returns the generated code in a readable format using Gradio

## 💡 Example UI

<img width="1903" height="651" alt="image" src="https://github.com/user-attachments/assets/dda10985-5adb-4a82-8c22-445d0ff85082" />

---

Enjoy coding smarter trading strategies with the power of LLMs!
