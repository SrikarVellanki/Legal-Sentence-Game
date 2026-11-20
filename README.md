# Legal Sentence Game

[![Built with askThili](https://ask.thili.ai/api/v1/public/projects/zpwdhvetvu/badge.svg)](https://ask.thili.ai/b/zpwdhvetvu)

This project develops a command-line interface game for law students to hone their legal drafting skills. Players complete partial legal sentences using n-gram predictions, then receive instant feedback on the clause type from a fine-tuned GPT-2 model. It's a practical application of language models for educational purposes.

## What you are building

**Goal.** You will build a CLI game where law students practice drafting legal sentences using n-gram prediction, receiving instant feedback on generated clause types from a fine-tuned GPT-2 model.

**Done when.** The project is done when you have a functional CLI game where players can complete legal sentences using n-gram predictions, and their completed sentences are classified by a fine-tuned GPT-2 model, providing feedback.

## Milestones

Tick these off as you go, and commit after each one.

- [ ] **1. Prepare a legal text corpus for n-gram model training.**  
      Hint: Use techniques from the 'Build a Next-Word Predictor from Scratch' drill for corpus cleaning and tokenization.
- [ ] **2. Implement the n-gram next-word predictor.**  
      Hint: Implement n-gram probability calculation and next-word prediction as shown in the 'Build a Next-Word Predictor from Scratch' drill.
- [ ] **3. Load the fine-tuned GPT-2 model for legal clause classification.**  
      Hint: Follow the 'Fine-Tune GPT-2 to Tag Legal Contract Clauses' drill to load your fine-tuned GPT-2 model for inference.
- [ ] **4. Create a CLI game interface presenting partial legal sentences for completion.**  
      Hint: Use basic Python input/output functions to create an interactive command-line experience.
- [ ] **5. After user completion, classify the full sentence and provide feedback.**  
      Hint: Apply the loaded GPT-2 model from 'Fine-Tune GPT-2 to Tag Legal Contract Clauses' for classification and format the feedback clearly.

## Run it

You need Python 3.12 and git.

```bash
python3.12 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env        # then choose a model; see the comments inside
python -m app.cli hello
pytest
```

Your work goes in `app/core.py` (one stub per milestone) and `tests/test_core.py`. The first tests pass already; they
check the plumbing.

## Settings and secrets

Model settings live in `.env`, which is ignored by git. **Never commit `.env` or paste a key into code.** If a key ever
reaches GitHub, treat it as leaked and make a new one.

## Stretch ideas

- Implement more advanced n-gram techniques like Kneser-Ney smoothing for better predictions.
- Add a scoring system to track player performance over multiple rounds.
- Enhance the GPT-2 feedback to suggest alternative phrasing or highlight common legal drafting errors.
