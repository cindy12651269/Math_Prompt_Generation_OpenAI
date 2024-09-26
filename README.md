# Math Prompt Generation with OpenAI

This repository contains a project that generates math-related prompts using OpenAI's GPT model. The goal of this project is to leverage generative AI to create diverse and challenging math problems for educational or research purposes, with support for both English and Chinese.

## Project Overview

The project includes a Python script that demonstrates how to use OpenAI's API to generate math problems and their solutions. The key features include:
- Connecting to the OpenAI API.
- Generating math problems in both English and Chinese.
- Solving math problems using OpenAI's GPT model.
- Supporting different topics and levels of difficulty.

### Key Functions

1. **`get_completion(messages, model="gpt-4-turbo", temperature=0, max_tokens=1000)`**  
   This function sends a request to the OpenAI API to generate a response based on the provided messages. It uses the ChatGPT API to generate completions in either English or Chinese.

   - **Parameters:**
     - `messages`: A list of dictionaries containing the role (`system`, `user`, etc.) and the content (prompt).
     - `model`: The model to be used, default is `"gpt-4-turbo"`.
     - `temperature`: Controls randomness in the output; a higher value means more creative responses.
     - `max_tokens`: Limits the length of the generated response.
     
   - **Returns:**  
     The content of the generated response, either a math problem or solution.

   Example usage:
   ```python
   messages = [
       {"role": "system", "content": "You are a helpful assistant that generates math problems."},
       {"role": "user", "content": "Generate a hard algebra word problem."}
   ]
   result = get_completion(messages)
   print(result)
### `generate_math_problem(topic, difficulty, problem_type, language="en")`

This function generates a math problem based on the provided topic, difficulty, and problem type. The language can be set to either English ("en") or Chinese ("zh").

**Parameters:**
- `topic`: The topic of the math problem (e.g., Algebra, Geometry).
- `difficulty`: The level of difficulty (easy, medium, hard).
- `problem_type`: The type of problem (word problem, equation, theoretical question).
- `language`: Specifies the language for the problem ("en" for English, "zh" for Chinese).

**Returns:**  
A generated math problem in the specified language.

**Example usage:**

```python
problem = generate_math_problem("Algebra", "hard", "theoretical question", "zh")
print(problem)

