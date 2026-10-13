# Text Language Translator

A lightweight, efficient text translation application that translates text between multiple languages in real time. Powered by automated language detection and API-based translation models, this tool makes cross-language communication fast and seamless.

---

## Features

* **Multi-Language Support**: Translate text between over 100 languages.
* **Auto-Language Detection**: Automatically identifies the source language if unspecified.
* **Batch Translation**: Translate single sentences, paragraphs, or full document streams.
* **CLI & API Interface**: Flexible usage via command line interface or programmatic API calls.
* **Copy & Export**: Easy mechanisms to output translations to JSON, TXT, or stdout.

---

## Tech Stack & Dependencies

* **Language**: Python 3.8+ / JavaScript (Node.js 18+)
* **Libraries / Packages**:
* `requests` / `axios` — HTTP client for API requests
* `googletrans` / `@google-cloud/translate` or `deepl-node` — Translation provider bindings
* `python-dotenv` / `dotenv` — Environment configuration management



---

## Prerequisites

Before running the project, ensure you have:

* [Python 3.8+](https://www.python.org/downloads/) or [Node.js 18+](https://nodejs.org/) installed.
* An API Key from your translation provider (*Google Cloud Translation, DeepL, or OpenAI API*) if required by your setup.

---

## Installation & Setup

1. **Clone the Repository**
```bash
git clone https://github.com/your-username/text-language-translator.git
cd text-language-translator

```


2. **Create a Virtual Environment** *(Python)*
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

```


3. **Install Dependencies**
```bash
pip install -r requirements.txt

```


*For Node.js projects:*
```bash
npm install

```


4. **Environment Configuration**
Copy the `.env.example` file to `.env` and add your credentials:
```bash
cp .env.example .env

```


Inside `.env`:
```env
TRANSLATION_API_KEY=your_api_key_here
DEFAULT_TARGET_LANG=es

```



---

## Quick Start & Usage

### 1. Command Line Interface (CLI)

Translate text directly from the terminal:

```bash
python main.py --text "Hello, world!" --target es

```

**Output:**

```
Source (en): Hello, world!
Target (es): ¡Hola, mundo!

```

### 2. Python API Usage

```python
from translator import TextTranslator

# Initialize translator
translator = TextTranslator(target_lang="fr")

# Translate text
result = translator.translate("Welcome to our project!")

print(f"Original: {result.original}")
print(f"Translated: {result.translated}")
print(f"Detected Source: {result.source_lang}")


---

## Running Tests

Run the unit test suite to verify everything is working as expected:

```bash
pytest

```

*Or for Node.js:*

```bash
npm test

```

---

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

---

## License

Distributed under the **MIT License**. See `LICENSE` for more details.