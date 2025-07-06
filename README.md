# Smartclass-Programming-Evaluation-Autograder+

## Overview

**Smartclass-Programming-Evaluation-Autograder+** is a research-driven framework designed to automate the evaluation of student programming submissions using advanced AI techniques. This project addresses critical challenges in large-scale programming education, including inconsistent manual grading, lack of timely feedback, and the need for scalable rubric-based assessment systems. The autograder utilizes graph-based code representations, domain-specific embeddings, and Large Language Models (LLMs) to deliver structured, explainable, and pedagogically-aligned feedback.

This system is being developed as part of a thesis project at the Indian Institute of Technology (IIT) Bhilai and is intended to contribute to the broader domain of intelligent educational technologies and AI-assisted learning analytics.

---

## Research Motivation

Manual grading of programming assignments in higher education is time-consuming, subjective, and difficult to scale. While existing autograding solutions provide surface-level correctness validation, they often lack depth in evaluating logic, problem-solving strategy, or alignment with course-specific rubrics.

This project aims to build an AI-enhanced framework that:
- Evaluates code beyond functional correctness.
- Aligns assessments with academic rubrics and learning objectives.
- Supports multi-level performance analysis (student, group, classroom).
- Facilitates real-time feedback generation and institutional analytics.

---

## Key Features

- **Rubric-Based Assessment**: Evaluates submissions across multiple dimensions such as student aptitude, logical reasoning, problem analysis, and output validation.
- **Prompt Pooling Mechanism**: Uses diverse prompts to enhance the reliability and explainability of LLM-based evaluations.
- **Graph-Based Preprocessing**: Parses source code into Abstract Syntax Trees (ASTs) and graph structures to capture logic flows and syntactic patterns.
- **Hybrid Dataset Utilization**: Combines real-world classroom data (500+ annotated samples) with 35,000+ open-source programming submissions in Python and C.
- **LLM Integration**: Leverages models such as Qwen, LLaMA, and Codex for semantic understanding of student code.
- **Secure Execution Environment**: Uses containerized infrastructures (e.g., Docker) for isolated and reproducible code execution.
- **Analytics Dashboard**: Offers real-time insight into student performance trends, rubric alignment, and grading consistency.

---

## Methodology

1. **Dataset Construction**  
   - Manual collection of student submissions from workshops and classroom assignments.
   - Integration of open-source programming datasets for model generalization.

2. **Code Preprocessing**  
   - Transformation of code into graph representations using ASTs.
   - Feature extraction for structure, control flow, and logic.

3. **Prompt Pooling and Evaluation**  
   - Multiple prompts per rubric category guide LLM-based evaluation.
   - Aggregation of scores through ensemble strategies.

4. **Rubric Mapping**  
   - Scores are assigned based on four rubric dimensions:
     - Aptitude
     - Logic Understanding
     - Problem Analysis
     - Output and Test Case Accuracy

5. **Performance Metrics**  
   - Evaluation based on Accuracy, F1 Score, Rubric Concordance, and Explainability.

---

## Project Timeline

The project was initiated in **May 2025** and spans six months, including:
- Literature review and problem formulation.
- Dataset preparation and prototype development.
- Experimental evaluation using prompt ensembles.
- Real-time deployment trials and final documentation.

---

## Expected Outcomes

- A reusable and scalable framework for programming evaluation in academic institutions.
- Improved grading consistency and faster feedback cycles.
- Integration capabilities for LMS platforms and smart classroom infrastructure.
- Research publications and documentation for reproducibility.

---

## Research Contributions

This project contributes to the fields of:
- AI in Education (AIED)
- Learning Analytics
- Code Semantics and Representation Learning
- Rubric-Driven Assessment
- LLM Interpretability in Educational Use Cases

---

## Repository Structure

```

Smartclass-Programming-Evaluation-Autograder/
├── data/                     # Raw and preprocessed datasets
├── prompts/                 # Prompt pool definitions
├── evaluation/              # LLM evaluation scripts and scoring logic
├── rubric/                  # Rubric schema and mapping functions
├── models/                  # Embedding and LLM model integration
├── dashboard/               # Analytics and visualization modules
├── docker/                  # Secure execution environment setup
├── docs/                    # Documentation and publication drafts
└── README.md

```

---

## Authors and Affiliation

- **Nitin Mane**, M.Tech Mechatronics, Indian Institute of Technology Bhilai  
- **Vikrant Sahu**, Ph.D. Scholar in Data Science and Artificial Intelligence, Indian Institute of Technology Bhilai

For academic inquiries or collaboration opportunities, please contact:  
**nitingautam@iitbhilai.ac.in**

---

## Acknowledgments

This work is supported under the academic supervision of the Department of Mechatronics and the Department of Computer Science and Engineering at IIT Bhilai. The authors would like to thank workshop organizers, student participants, and the institutional review board for their contributions and feedback.

---

## License

This project is under active academic research. Licensing and code availability will be updated post-publication and institutional approval.

