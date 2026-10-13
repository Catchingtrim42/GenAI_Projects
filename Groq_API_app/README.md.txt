# 🚀 Prompt Engineering Playground

An interactive web-based playground built with **Gradio** and powered by the **Groq API** (`openai/gpt-oss-20b`), designed for testing, structuring, and managing LLM prompt templates.

---

## Features

* **Quiz Generator:** Automatically creates customized quiz questions by specifying a topic and difficulty level.
* **Sentiment Analyzer:** Evaluates text sentiment and outputs structured JSON data containing the sentiment, confidence level, and reasoning.
* **Leave Letter Generator:** Dynamically drafts customizable leave letters based on user-defined tone, recipient, reason, length, and dates.
* **Reusable Prompt Library & Templates:** Includes programmatic classes (`PromptLibrary` and `PromptTemplate`) for rapid prompt structuring and reusability.

---

## Requirements

1. Python
2. Groq
3. Gradio

---

## Installation & Setup

1. Clone or download the repository/notebook.
2. Install the required dependencies:
```bash
pip install -q groq gradio

```


3. Set up your Groq API key as an environment variable or via Google Colab secrets:
* Key name: `GROQ_API_KEY`



---

## Usage

Run the script or notebook cells sequentially to initialize the Groq client and launch the interactive Gradio web interface. The app will generate a temporary public URL for testing directly in your browser.