# Coding authenticity in student lab reflections

The human-in-the-loop (HITL) prompts used to code students' end-of-semester reflective memos from an introductory physics lab for **direct authenticity** and related research-experience codes. The LLM prompts proposed candidate codes, and a researcher reviewed each one.

## Contents

```
prompts/
  hitl_prompts.ipynb          span-finder and verifier prompts for all 7 codes, plus the settings used
  dummy_exemplar_bank.xlsx    same structure as the real exemplar bank, with invented rows
```

## The coding pipeline

For each memo and each code:

1. A **span finder** (gpt-4.1-mini) flags every passage that *could* match the code. It is set for high recall.
2. The flagged passages are widened to full sentences.
3. A **verifier** (Kimi K2.5) reviews each sentence against the full code definition and the most similar examples from an exemplar bank. It is told to lean toward keeping a sentence.
4. **A researcher reviews every kept sentence** in the context of the whole memo and makes the final decision.

The prompts notebook is for reference only. The original pipeline ran through an institutional AI gateway, so it doesn't include the API or pipeline code.

## Data and privacy

The memos, the coded labels, and the real exemplar bank are student writing protected under an IRB protocol, so they are not included. The example sentences inside the prompts are **synthetic paraphrases** of the originals, and every row of `dummy_exemplar_bank.xlsx` is invented.

## Citation

_Add the paper citation here._
