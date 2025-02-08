## Features
1. Detect security vulnerabilities using OpenAI.
2. Identify common security issues (e.g., SQL injection, hardcoded secrets, unvalidated input).
3. Post security warnings on the PR if issues are found.


## How It Works
1. Triggered on a PR update.
2. Fetches changed files (only .js, .ts, .py, .java, .sol for security audit).
3. Sends the code to OpenAI for security analysis.
4. Identifies vulnerabilities, including:
    - SQL Injection
    - Hardcoded credentials
    - XSS vulnerabilities
    - Insecure API usage
5. Posts security findings as a comment on the PR.

## How to use it

1. You'll need an OpenRouter API key with will use latest OpenAI o3 mini for free. Store it as a GitHub secret.
2. Go to GitHub Repo → Settings → Secrets → Actions.
3. Add a new secret named OPENROUTER_API_KEY.


# Development

## Setup
Create a virtual environment:

```
python -m venv env
```

Activate the virtual environment:

```
source env/bin/activate
```

```
pip install -r requirements.txt
```

## Environment Configuration
Configure all the directories properly. Make sure all of them have proper read and write permissions.

```
cp .env.example .env
```
