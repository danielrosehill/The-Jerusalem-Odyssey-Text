# The Jerusalem Odyssey Text Generation Experiment

## Overview

This repository contains the results of an experiment testing the maximum output capabilities of large language models (LLMs), specifically comparing Gemini 2.5 and Anthropic Claude 3.7 Sonnet. The experiment aimed to determine if Gemini 2.5 could produce its claimed maximum output of 65,000 tokens, while also evaluating Anthropic's performance with its 128,000 token output capability.

## Experiment Results

The experiment revealed that **Gemini 2.5 could not meet its claimed maximum output** of 65,000 tokens. In contrast, **Anthropic Claude 3.7 Sonnet performed notably well**, generating "The Jerusalem Odyssey" - a complete 15-chapter novella based on the provided prompt.

## Content Analysis

### Word Count and Character Count

The generated story in `output.md` contains:
- **Total words: 31,245**
- **Total characters (with spaces): 177,892**
- **Total characters (without spaces): 146,647**

### Token Estimate

Using standard tokenization estimates (where 1 token ≈ 4 characters or 0.75 words):
- **Estimated tokens: ~36,662** (based on character count / 4)
- **Estimated tokens: ~41,660** (based on word count / 0.75)

Taking the average of these estimates: **~39,161 tokens**

### Percentage Analysis

- **Word count as percentage of requested 40,000 words: 78.1%**
- **Token estimate as percentage of Claude's claimed 128,000 token capability: 30.6%**

 
## Repository Contents

- `output.md`: The complete generated story (15 chapters)
- `prompt.py`: Python script used to generate the text using Anthropic's API
- `system-prompt.md`: The system prompt provided to the model
- `user-prompt.md`: The user prompt containing the story outline
- `README.md`: This file, documenting the experiment

## Technical Implementation

The experiment used Anthropic's Claude 3.7 Sonnet model with the following parameters:
- Model: `claude-3-7-sonnet-20250219`
- Maximum tokens: 128,000
- Temperature: 1.0
- System prompt: Instructions to generate a 38,000-40,000 word manuscript
- User prompt: Detailed plot outline for "The Jerusalem Odyssey"

## Conclusions

While the generated output fell short of the requested 40,000 words (achieving 78.1%), it demonstrates Claude 3.7 Sonnet's ability to maintain narrative coherence, character development, and thematic consistency across a lengthy text. 

The experiment highlights the current capabilities and limitations of state-of-the-art language models in generating extended creative content.
