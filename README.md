# Gemini Hallucination Detection

This project demonstrates how to use Gemini 1.0 Pro to detect hallucinations in Large Language Models (LLMs). This project is part of the #MLOlympiad and #GeminiSprint.

![Dataset Cover](dataset-cover.jpg)

## Project Overview

The project explores different methods for detecting hallucinations in LLMs. The main idea is to use an LLM to generate an answer for a given prompt and then compare the generated answer with a target answer. The difference between the two answers can be used as a score to detect hallucinations.

The project is based on the Kaggle competition [ML Olympiad - Detect Hallucinations in LLMs](https://www.kaggle.com/competitions/ml-olympiad-detect-hallucinations-in-llms) and uses the dataset from [GenAI Hallucinations](https://www.kaggle.com/datasets/lucamassaron/genai-hallucinations).

## Notebooks

The repository contains two notebooks:

*   **gemini_hallucinations_detection.ipynb**: This notebook uses Gemini 1.0 Pro to generate an answer for a given prompt and then calculates the distance between the generated answer and a target answer using text embeddings. This distance is used as a score to detect hallucinations. The notebook also generates a submission file for the Kaggle competition.
*   **selfcheckgpt.ipynb**: This notebook explores alternative methods for detecting hallucinations. It uses the SelfCheckGPT library to calculate different scores like 1-gram similarity, cosine similarity, and logloss to evaluate the factuality of the generated text.

## Dataset

The project uses the "GenAI Hallucinations" dataset, which contains prompts, answers, and a target label indicating whether the answer is a hallucination or not.

## Getting Started

To get started with the project, you need to have a Google Cloud account and a project with the Vertex AI API enabled. You also need to install the required libraries, which are listed in the notebooks.

## Results

The `gemini_hallucinations_detection.ipynb` notebook achieves a certain ROC AUC score on the Kaggle competition. The `selfcheckgpt.ipynb` notebook provides a comparison of different hallucination detection methods. The results are discussed in the notebooks themselves.