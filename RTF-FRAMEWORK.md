# RTF prompt framework

A simple framework for structuring prompts. Use this to evaluate whether a prompt is complete.

## Components

| Element | Question | Examples |
|---------|----------|----------|
| **Role** | Who should the AI act as? | Expert, advisor, writer, analyst, coach |
| **Task** | What should the AI do? | Analyse, create, explain, summarise, compare |
| **Format** | How should the output look? | Bullet points, table, step-by-step, code |

## Flow

Role → Task → Format → Structured response

## Evaluation

A prompt is complete when all three elements are clear (explicit or inferable from context). Missing elements warrant clarification questions.
