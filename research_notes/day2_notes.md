# Day 2: False Premise Hallucination Research Notes
<!-- Notes sourced from "Whispers that Shake Foundations: Analyzing and Mitigating False Premise Hallucinations in Large Language Models" (EMNLP 2024) -->

## FAITH Method
- FAITH (False premise Attention head constraIining for miTigating Hallucinations): A novel method to reduce false premise hallucinations.

## False Premise Hallucination
- Phenomenon where LLMs generate hallucinated text in response to false premise questions.

## False Premise Question
- Questions with assumed false facts (e.g., “Why does the moon orbit Mars?”) believed by the asker.

## False Premise Heads
- Specific attention heads influencing factual knowledge, causing hallucinations when disturbed.
- Insight: These heads disrupt knowledge in shallow layers during inference.
- Note: Self-attention layers transfer factual knowledge from MLP layers during inference.

## Hallucination Mitigation in FAITH
- Step 1: Localize false premise attention heads.
- Step 2: Constrain these heads during inference.
- Experimental Result: Presence of false premise heads leads to hallucinations.

## Reflection
- FAITH could help my project by targeting attention heads in LLMs like Grok to reduce errors on stats questions. This connects to my Day 1 test where ChatGPT corrected a false premise.
