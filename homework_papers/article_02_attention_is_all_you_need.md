# Article 2 – Attention Is All You Need

**Authors:** Vaswani, Shazeer, Parmar, Uszkoreit, Jones, Gomez, Kaiser, Polosukhin (Google)
**Published:** NIPS 2017

## Central idea
The article proposes the **Transformer**, a model for translation that uses only
**attention**, without recurrent networks (RNN) or convolutions.
The goal is better translation and faster training.

## Three important takeaways
1. **Only attention.** Each word can look at all the other words directly.
2. **Faster training.** Without recurrence, the work can be done in parallel.
3. **Better results.** New best BLEU scores on English–German (28.4) and
   English–French (41.0), with less training cost.

## Interesting observations
- Multi-head attention: several attentions in parallel.
- Positional encoding is added because the model does not know word order.
- Training: 8 GPUs, 3.5 days for the big model.
- The code is public.

## Patterns identified
- Problem → background → model → why self-attention → training → results → conclusion.
- They change one part of the model at a time to see what matters (model variations).

## Practical applications
- Translation, text generation, chatbots.

## Critical thinking
- **Assumptions:** BLEU score is a good measure of translation quality.
- **Limitations:**
  - Self-attention cost grows with the square of the sentence length (table in section 4).
  - Only tested on translation in this paper.
  - Needs strong hardware.
- **Do I agree?** Yes, the results are clear.

## My feedback on the article
- **Worth reading?** Yes, a very important paper.
- **Structure:** Very good: abstract, introduction, background, model, training,
  results, conclusion, references.
- **Relevance:** Very high.
- **Weak point:** dense, needs background in deep learning.
- **Overall:** Professional and well tested.
