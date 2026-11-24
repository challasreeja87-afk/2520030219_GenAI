# Week 2 – Provider-Agnostic LLM Client

## Aim

To develop a provider-independent Large Language Model (LLM) client that supports multiple AI providers through a common interface.

## Introduction

In this experiment, I developed a Python application that can communicate with two different LLM providers: Google Gemini and Ollama.

Instead of writing separate application logic for each provider, I created a common interface using Python's Abstract Base Class (ABC). This allows the application to switch between providers without changing the main client logic.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| Google Gemini API | Cloud-based LLM provider |
| Ollama | Runs LLMs locally |
| Llama 3.2 | Local language model |
| Requests | Sends HTTP requests to Ollama |
| python-dotenv | Loads API credentials |
| unittest | Tests the client functionality |

## Files Included

- `main.py` – Takes the provider selection and user prompt, then displays the generated response.
- `llm_client.py` – Contains the common interface, Gemini provider, Ollama provider and LLM client.
- `test_client.py` – Contains a unit test using a fake provider.
- `requirements.txt` – Lists the required Python packages.
- `.env` – Stores the Gemini API key locally and is excluded from GitHub.
- `.gitignore` – Prevents sensitive and unnecessary files from being tracked by Git.

## Implementation

### 1. Common Interface

Created an abstract class called `LLMProvider` using Python's `ABC` module. It defines the abstract `generate()` method that the providers must implement.

### 2. Gemini Provider

Implemented `GeminiProvider` to connect to Google's Gemini API and generate responses using the supplied prompt.

### 3. Ollama Provider

Implemented `OllamaProvider` to send HTTP requests to the locally running Ollama service using the Llama 3.2 model.

### 4. Common LLM Client

Created the `LLMClient` class, which accepts a provider object and calls its `generate()` method.

### 5. Provider Selection

The main program allows the user to select either Gemini or Ollama and enter a question.

### 6. Unit Testing

Created a `FakeProvider` in `test_client.py` to test the common client without making an actual API request.

## Execution

Install the required packages:

```bash
pip install -r requirements.txt
```

Run the application:

```bash
python main.py
```

Choose a provider:

```text
Choose provider (gemini/ollama):
```

Enter your question when prompted.

### Gemini

Select `gemini`. Make sure the `GEMINI_API_KEY` is configured in the local `.env` file.

### Ollama

Select `ollama`. Make sure Ollama is installed, running and has the `llama3.2` model available.

## Unit Testing

Run the test file:

```bash
python -m unittest test_client.py -v
```

The test uses a fake provider to verify that the common client correctly returns the generated response.

## Learning Outcomes

- Understood provider-independent LLM architecture.
- Learned about Abstract Base Classes and inheritance in Python.
- Implemented Gemini and Ollama providers.
- Learned how to send HTTP requests using the Requests library.
- Understood how to test application logic using a fake provider and unit testing.