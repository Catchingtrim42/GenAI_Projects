# AI Chatbot Web App

An interactive web-based conversational chatbot built with **Gradio** and powered by the Hugging Face Transformers model **Blenderbot** (`facebook/blenderbot-400M-distill`), designed to maintain context across multi-turn user conversations.

---

## Features

* **Conversational Memory:** Tracks message history dynamically across sessions to maintain context and provide coherent multi-turn replies.
* **Interactive Web Interface:** Clean layout featuring an adjustable height chatbox, text input field, send button, and a clear history control.
* **Public URL Generation:** Instantly launches a temporary public web link via Gradio for direct testing and sharing from Google Colab.

---

## Requirements

1. Python
2. Transformers (`facebook/blenderbot-400M-distill`)
3. PyTorch
4. Gradio

---

## Installation & Setup

1. Open the project notebook in Google Colab or clone the repository locally.
2. Install the required dependencies:
```bash
pip install -q transformers gradio

```



---

## Usage

Run the notebook cells sequentially to load the tokenizer and sequence-to-sequence model, initialize the chat handler function, and launch the interactive Gradio web interface.