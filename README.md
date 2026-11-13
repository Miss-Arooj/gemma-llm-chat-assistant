# Gemma LLM Chat Assistant

Notebook experiment loading the Gemma instruction-tuned model, applying its chat template, maintaining conversational history, and streaming generated text using a background thread.

## Highlights

- Loads an instruction-tuned Gemma model through Transformers.
- Applies the model chat template.
- Maintains conversation messages.
- Streams generated output with `TextIteratorStreamer` and a worker thread.

## Technology stack

Python, PyTorch, Hugging Face Transformers, gemma-4-E2B-it, TextIteratorStreamer

## Repository contents

- `notebooks/gemma-llm-chat-assistant.ipynb` — original project notebook or application entry point.
- `requirements.txt` — Python dependencies.
- `.gitignore` — excludes local environments, secrets, datasets, and model artifacts.
- `screenshots/` — spaces for project documentation and genuine screenshots.

## Setup

1. Clone this repository.
2. Create and activate a virtual environment.
3. Install the dependencies.
4. Follow the project-specific instructions below.

```bash
python -m venv .venv
# Windows PowerShell
.venv\Scripts\Activate.ps1
# macOS / Linux
source .venv/bin/activate
pip install -r requirements.txt
```

## Run / reproduce

Open the notebook in a GPU-enabled environment, install dependencies, and run cells in order. Model files are downloaded from Hugging Face when loaded. Review the model card and license/usage terms before use.

The notebook specifies CUDA via `device_map="cuda"`; use a compatible GPU and verify model availability/access and current Transformers support before running.

## Results

The notebook output includes a sample response and a recorded generation time of approximately 19.82 seconds for that run. This is not a general latency benchmark.

## Limitations and next steps

- The chatbot's response quality depends on the Gemma model's capabilities and input prompt quality.
- Performance and response generation speed may vary depending on available system resources.
- Future improvements could include conversation history, context retention, and enhanced response handling.

## Test Cases

### Creative Thinking
[Watch Creative Thinking](./test_cases/Creative_Thinking.mov)

### 2. Instruction Following

<video src="./test_cases/Instruction_Following.mov" controls width="100%"></video>

### 3. Logical Reasoning

<video src="./test_cases/Logical_Reasoning.mov" controls width="100%"></video>

### 4. Memory Test

<video src="./test_cases/Memory_Test.mov" controls width="100%"></video>
