# Week 5 – Token Economics and Budget Planner

## Aim

To develop a Python-based token economics and budget planning tool that estimates LLM token usage, calculates API costs and checks usage limits.

## Introduction

Large Language Models process text using tokens. Every request may consume input tokens and generate output tokens. When using paid LLM APIs, token consumption directly affects the overall usage cost.

In this experiment, I developed a token economics tool that helps estimate API expenses and monitor usage against a predefined budget.

The application calculates estimated token consumption, daily and monthly costs, and checks Requests Per Minute (RPM) and Tokens Per Minute (TPM) limits.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| python-dotenv | Loads configuration from environment variables |
| unittest | Tests the budget planner functionality |

## Files Included

- `budget.py` – Contains the token usage estimation, cost calculation and budget planning logic.
- `test_budget.py` – Contains automated unit tests for the budget planner.
- `requirements.txt` – Lists the required Python packages.
- `.env` – Stores local configuration values, if required. This file is not uploaded to GitHub.
- `.gitignore` – Prevents sensitive and unnecessary files from being tracked by Git.

## Implementation

### 1. Token Usage Estimation

Estimates the number of input and output tokens required for LLM requests.

### 2. API Cost Calculation

Calculates the estimated cost based on token usage and the configured pricing information.

### 3. Daily and Monthly Budget Planning

Estimates daily and monthly API expenses to help understand and plan LLM usage.

### 4. Rate Limit Monitoring

Considers two important API usage limits:

- **RPM (Requests Per Minute):** Maximum number of requests allowed per minute.
- **TPM (Tokens Per Minute):** Maximum number of tokens allowed per minute.

### 5. Budget Checking

Compares estimated API expenses against the configured budget to help identify whether the planned usage is within the available budget.

### 6. Automated Testing

Uses Python's `unittest` framework to verify the budget calculation and planning functionality.

## Execution

Install the required packages:

```bash
pip install -r requirements.txt
```

Run the budget planner:

```bash
python budget.py
```

Run the automated tests:

```bash
python -m unittest test_budget.py -v
```

## Expected Results

The program performs token usage and cost calculations based on the configured inputs and pricing values.

It helps estimate:

- Input and output token consumption.
- Estimated API costs.
- Daily and monthly usage expenses.
- Requests Per Minute (RPM).
- Tokens Per Minute (TPM).
- Whether estimated usage fits within the configured budget.

The actual results depend on the input values and pricing configuration.

## Learning Outcomes

- Understood the concept of token economics in LLM applications.
- Learned how input and output tokens affect API costs.
- Implemented token usage and cost estimation using Python.
- Understood daily and monthly budget planning.
- Learned about RPM and TPM rate limits.
- Understood how to compare estimated costs against a budget.
- Practiced automated testing using Python's `unittest` framework.