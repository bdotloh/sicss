# LLM-Enhanced Topic Modeling of Social Media Posts

This repository contains a demonstration for a workshop on how large language models (LLMs) can improve topic modeling of social media data.

## Background

Topic modeling of social media posts is notoriously challenging due to:
- High noise-to-signal ratio (many uninformative or redundant words)
- Users expressing similar ideas in drastically different ways
- Traditional topic modeling methods often producing incoherent topics due to overfitting on noisy inputs

## Approach

This demo introduces an LLM-based preprocessing step: **summarizing each post before topic modeling**, allowing for:
- Reduced noise
- Enhanced interpretability
- Improved clustering of meaningful topics

## Repository Structure

- **`1.llm_workflow.ipynb`**  
  - Use the [`ollama`](https://github.com/ollama/ollama) Python package to interact with local LLMs
  - Craf prompt templates to summarize individual posts
  - Apply the LLM summarization pipeline to a small sample of text messages.

- **`2.topic_modelling.ipynb`**  
  - Implements a topic modeling workflow using sentence embeddings and clustering
  - Compares the topics produced from raw social media posts versus LLM-generated summaries


## Requirements

To install dependencies:

```bash
pip install -r requirements.txt
```
You’ll also need to install and run ollama locally. For instructions, see this [`guide`](https://www.kdnuggets.com/ollama-tutorial-running-llms-locally-made-super-simple)