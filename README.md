# Gemma LLM Chat Assistant

Notebook experiment loading the Gemma instruction-tuned model, applying its chat template, maintaining conversational history, and streaming generated text using a background thread.

## Highlights

- Loads an instruction-tuned Gemma model through Transformers.
- Applies the model chat template.
- Maintains conversation messages.
- Streams generated output with `TextIteratorStreamer` and a worker thread.

## Technology Stack

Python, PyTorch, Hugging Face Transformers, gemma-4-E2B-it, TextIteratorStreamer

## Repository Contents

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

## Run / Reproduce

Open the notebook in a GPU-enabled environment, install dependencies, and run cells in order. Model files are downloaded from Hugging Face when loaded. Review the model card and license/usage terms before use.

The notebook specifies CUDA via `device_map="cuda"`; use a compatible GPU and verify model availability/access and current Transformers support before running.

## Results

The notebook output includes a sample response and a recorded generation time of approximately 19.82 seconds for that run. This is not a general latency benchmark.

## Test Cases

The following test cases evaluate the chatbot's conversational ability, reasoning, memory, coding knowledge, creativity, general knowledge, and instruction-following capabilities.

### 1. General Conversation

**Purpose:** Test how naturally the chatbot communicates and responds to everyday conversational questions.

**Test Prompts:**

1. Hi! How are you today?
2. What do you usually do when someone asks you a difficult question?
3. If you could travel anywhere in the world, where would you go and why?

**Test Video:**

https://github.com/user-attachments/assets/0600edd5-8411-4551-9cc8-17a5a60f8e96

### 2. Logical Reasoning

**Purpose:** Test the chatbot's ability to solve problems, understand questions, and think logically.

**Test Prompts:**

1. I have 5 apples. I give 2 to Ali and 1 to Sara. How many apples do I have left?
2. A farmer has 17 sheep. All but 9 run away. How many are left?
3. If yesterday was Monday, what day will tomorrow be?

**Test Video:**

https://github.com/user-attachments/assets/cca84ec7-e245-4eae-9deb-797cfc4906a7

### 3. Memory Test

**Purpose:** Check whether the chatbot remembers information shared in previous messages during the conversation.

**Test Prompts:**

1. My name is Ahmed, and I am a software developer.
2. What is my name and profession?
3. I also like Python programming. What programming language do I like?

**Test Video:**

https://github.com/user-attachments/assets/5e2bf5ff-87ba-45d3-ae8c-afe155d6a572

### 4. Coding Knowledge

**Purpose:** Test the chatbot's understanding of programming concepts and its ability to generate basic code.

**Test Prompts:**

1. Explain Python functions in simple words.
2. Write a Python function to check whether a number is even or odd.
3. What is the difference between a list and a tuple in Python?

**Test Video:**

https://github.com/user-attachments/assets/3c9c3514-ec04-48cb-9e72-8732c2c43efc

### 5. Creative Thinking

**Purpose:** Test the chatbot's creativity, imagination, and ability to generate interesting and original content.

**Test Prompt:**

1. Create a funny conversation between a cat and a dog.

**Test Video:**

https://github.com/user-attachments/assets/a76852f7-1014-4372-89cc-1dc52718e4ea

### 6. Knowledge and Explanation

**Purpose:** Test the chatbot's general knowledge and ability to explain different concepts clearly.

**Test Prompts:**

1. Why is the sky blue?
2. How does artificial intelligence work?

**Test Video:**

https://github.com/user-attachments/assets/88d72753-58df-4e7d-be5a-7049a8b3531c

### 7. Instruction Following

**Purpose:** Test whether the chatbot understands and follows specific instructions, formatting requirements, and word limits.

**Test Prompts:**

1. Explain artificial intelligence in exactly 3 sentences.
2. Give me 5 fruits, but don't use bullet points.
3. Explain cloud computing to a 10-year-old in fewer than 30 words.

**Test Video:**

https://github.com/user-attachments/assets/e40cf19f-d322-4e62-917d-4739939f650d

### 8. Challenging Questions

**Purpose:** Test the chatbot's ability to handle tricky questions, explain complex ideas, and apply logical reasoning.

**Test Prompts:**

1. Why is 0.999999... equal to 1?
2. Can a person be both right and wrong in an argument? Explain.
3. If all roses are flowers, and some flowers fade quickly, can we conclude that some roses fade quickly?

**Test Video:**

https://github.com/user-attachments/assets/adf8485d-9886-489a-98db-9104b0f533c2

## Limitations and Next Steps

- The chatbot's response quality depends on the Gemma model's capabilities and input prompt quality.
- Performance and response generation speed may vary depending on available system resources.
- Future improvements could include conversation history, context retention, and enhanced response handling.
