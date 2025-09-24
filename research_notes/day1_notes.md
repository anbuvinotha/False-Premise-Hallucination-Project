# Day 1: LLM and False Premise Hallucination Notes

## False Premise Hallucination in LLM (Large Language Models)
- AI-trained massive text data.
- Designed to predict the next word (tokens).
- Based on transformer architecture.

## What is LLM?
- AI trained on massive text data.
- Predicts the next word (tokens).
- Built on transformer architecture.

## What is Transformers?
- Neural network architecture introduced in 2017 in the paper "Attention is all you need".

## Working of LLM
1) Sentence to Token:
   - Input: I love apples.
   - Sentence is split into words: [I] [love] [apples] → These are tokens.
2) Embedding:
   - Tokens are converted into numerical values.
3) Positional Encoding:
   - Transformers don’t know the order by default, so we add position info.
4) Self Attention (Heart of the Transformer):
   - Each word looks at the other word and checks how much important it is.
5) Feedforward Network + Stacking Layers:
   - Transformers are made up of dozens or hundreds of feedforward and stacking layers.

## LLM Hallucination
- LLM models generate incorrect but confident answers, especially on false premise inputs, due to prioritizing fluency over fact-checking during pre-training.
