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

## Test Example
- **Question**: Why is variance always negative?
- **Response**: Actually, variance is never negative—it is always zero or positive. If someone says “variance is negative,” that’s a misunderstanding. Let me explain carefully why:

1. Definition of Variance

For a dataset 
𝑥
1
,
𝑥
2
,
.
.
.
,
𝑥
𝑛
x
1
	​

,x
2
	​

,...,x
n
	​

, with mean 
𝜇
μ, the variance is:

𝜎
2
=
1
𝑛
∑
𝑖
=
1
𝑛
(
𝑥
𝑖
−
𝜇
)
2
σ
2
=
n
1
	​

i=1
∑
n
	​

(x
i
	​

−μ)
2

or for a sample:

𝑠
2
=
1
𝑛
−
1
∑
𝑖
=
1
𝑛
(
𝑥
𝑖
−
𝑥
ˉ
)
2
s
2
=
n−1
1
	​

i=1
∑
n
	​

(x
i
	​

−
x
ˉ
)
2
2. Why it cannot be negative

Each term 
(
𝑥
𝑖
−
𝜇
)
2
(x
i
	​

−μ)
2
 is squared.

The square of any real number is always ≥ 0.

The sum of non-negative numbers is ≥ 0.

Dividing by a positive number (like 
𝑛
n or 
𝑛
−
1
n−1) keeps it ≥ 0.

✅ Therefore, variance ≥ 0.

Zero variance occurs only if all values are the same.

Otherwise, variance is positive.

3. Common confusion

Sometimes people think “variance is negative” because standard deviation formula or calculations go wrong (like taking the square root incorrectly or using wrong signs in software).

But mathematically, variance cannot be negative.
- **Hallucinated**: No (it corrected the false premise instead).
