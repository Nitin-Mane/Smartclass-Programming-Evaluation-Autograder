# Prompt Pooling Framework for AI-Based Code Evaluation

**Project Context:**  
This document outlines the design and implementation plan for Prompt Pooling in the Smart Class Programming Evaluation Autograder+ system. The objective is to improve rubric-based code assessment using a set of prompt variants for large language model (LLM) scoring.

## 🎯 Objective

Prompt Pooling is a technique that maintains multiple prompts per rubric category to:

- Improve evaluation robustness and reduce prompt sensitivity.
- Provide diverse instructional perspectives for LLM-based evaluation.
- Aggregate better judgment for code submissions across students, groups, and classrooms.


## 📚 Use Case

The rubric scoring system includes four core evaluation categories:

1. Student Aptitude
2. Logic Understanding
3. Problem Analysis
4. Output and Test Case Accuracy

Each category will have a pool of 2–5 prompt templates.


## 🧱 Prompt Pool Structure

Each rubric dimension will have a pool of prompts:

```json
{
  "aptitude": [
    "Evaluate this code and describe the student's understanding of programming fundamentals.",
    "Assess the syntax and structure of this code to infer the student's grasp of basic concepts."
  ],
  "logic": [
    "Explain the logic used in this code and determine its correctness.",
    "Does this code follow a structured algorithm? Justify your answer.",
    "Review the logic and suggest improvements if needed."
  ],
  "problem_analysis": [
    "Describe how the student has broken down the problem and approached the solution.",
    "Evaluate the strategy used to address the given task."
  ],
  "output": [
    "Compare the expected and actual output for the given test cases. Is the solution valid?",
    "Highlight any edge cases the code may fail to handle."
  ]
}
````


## ⚙️ Prompt Pooling Strategies

### 1. Random Sampling

Randomly selects a prompt from the pool each time a rubric is evaluated.

### 2. Ensemble Prompting

Queries the model with all prompts in a rubric category and aggregates responses (e.g., average score, voting).

### 3. Adaptive Prompting

Selects the best-performing prompt based on:

* Past rubric accuracy
* Student profile
* Code length/type


## 💻 Implementation Plan (Python Pseudocode)

```python
def evaluate_with_prompt_pool(task_input, rubric_category, model, prompt_pool):
    responses = []
    for prompt_template in prompt_pool[rubric_category]:
        prompt = prompt_template + "\n\n" + task_input
        response = model.generate(prompt)
        responses.append(response)
    return responses
```


## 📊 Evaluation Metrics

To assess the effectiveness of Prompt Pooling:

* Rubric score correlation with human-assigned scores
* Score variance across prompt variants
* F1 Score / Accuracy of aggregated scoring
* Student feedback (clarity of explanations)


## 🧪 Future Scope

* Train a prompt selector model for adaptive routing.
* Use prompt ensembles in few-shot format.
* Apply LLM self-consistency or chain-of-thought reasoning to resolve prompt disagreement.
* Integrate with rubric-explainer modules for explainable feedback.


## 📦 File Summary

**Author:** Nitin Mane
**Use Case:** LLM-assisted rubric evaluation in code assessment

```
