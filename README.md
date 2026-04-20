# Week 4 Starter: Math Agent

A ReAct agent that solves questions using tool calls.

## Walkthrough Video

- YouTube (unlisted): https://youtu.be/dundrKgUj84

## Setup

1. Install [uv](https://docs.astral.sh/uv/getting-started/installation/) if you don't have it.

2. Copy `.env.example` to `.env` and add your API key:
   ```bash
   cp .env.example .env
   ```
   Then edit `.env` and replace `your-key-here` with your key from [Google AI Studio](https://aistudio.google.com/apikey).

   To use a different provider, change the `MODEL` variable in `agent.py` and set the matching key in `.env`.

3. Make sure `.env` is in your `.gitignore` so you don't commit your key.

## Run (CLI)

```bash
uv run agent.py
```

`uv` will install dependencies automatically on first run.

The agent will work through each question in `math_questions.md` and print the ReAct trace (Reason / Act / Result) for each one.

## Run (Web UI)

```bash
python web_app.py
```

Then open `http://127.0.0.1:8000` in your browser.
If port `8000` is occupied, run `PORT=8001 python web_app.py` and open `http://127.0.0.1:8001`.

Click `Run All Questions` to automatically execute every question in `math_questions.md` and see each question with its final answer.

## Files

- `agent.py` - the ReAct agent (CLI + reusable `run_question`)
- `web_app.py` - minimal local web UI
- `calculator.py` - calculator tool
- `products.json` - product catalog with prices
- `math_questions.md` - the questions the agent solves
- `.env.example` - template for your API key
