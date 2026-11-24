# Week 3 – LLM Monitoring with MongoDB

## Aim

To implement an LLM monitoring system that tracks API usage, token consumption, response time, estimated cost and request status using MongoDB.

## Introduction

In this experiment, I developed a Python-based monitoring system for Large Language Model applications.

When an application communicates with an LLM, it is important to monitor how many tokens are used, how long the model takes to respond and how much each request costs.

To achieve this, I integrated MongoDB for storing usage information and implemented logging functionality to record LLM requests and their results.

The system helps track LLM activity and understand the performance and usage of AI applications.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| Google Gemini API | Cloud-based LLM provider |
| Ollama | Local LLM provider |
| MongoDB Atlas | Stores LLM usage and monitoring records |
| PyMongo | Connects Python applications to MongoDB |
| Requests | Sends HTTP requests to Ollama |
| python-dotenv | Loads environment variables |
| unittest | Tests application functionality |

## Files Included

- `main.py` – Main application that accepts user input and generates LLM responses.
- `llm_client.py` – Handles LLM provider communication and request processing.
- `usage_logger.py` – Handles logging and storing usage information.
- `test_client.py` – Contains unit tests for the LLM client.
- `requirements.txt` – Lists the required Python packages.
- `.env` – Stores API keys and database configuration locally. This file is not uploaded to GitHub.
- `.gitignore` – Prevents sensitive and unnecessary files from being tracked by Git.

## Implementation

### 1. LLM Client

Implemented an LLM client to communicate with the supported language model providers.

### 2. Usage Tracking

Tracked important information about LLM requests, such as:

- Input and output token usage
- Request response time (latency)
- Estimated API cost
- Request success or failure status

### 3. MongoDB Integration

Used MongoDB Atlas to store monitoring records. PyMongo provides the connection between the Python application and the MongoDB database.

### 4. Request Monitoring

Recorded request details to help monitor LLM usage and identify failed requests.

### 5. Error Handling

Included request handling mechanisms such as timeouts and retries to improve reliability when communicating with LLM providers.

### 6. Testing

Used Python's `unittest` framework to test the LLM client functionality.

## Execution

Install the required packages:

```bash
pip install -r requirements.txt
```

Configure the required API keys and MongoDB connection details in the local `.env` file.

Run the application:

```bash
python main.py
```

Run the unit tests:

```bash
python -m unittest test_client.py -v
```

## Expected Results

After executing the application, LLM requests are processed and monitoring information is recorded.

The monitoring records are intended to include token usage, response latency, estimated cost and request status.

The actual records depend on the provider, generated response and database configuration.

## Learning Outcomes

- Understood the importance of monitoring LLM applications.
- Learned how to track token usage and response latency.
- Understood estimated API cost calculation.
- Learned how to integrate MongoDB Atlas with Python.
- Used PyMongo to store monitoring information.
- Understood error handling, timeouts and retries.
- Learned how to test LLM client functionality using unit testing.