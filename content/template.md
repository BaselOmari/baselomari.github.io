---
title: "Building GPT from Scratch"
date: 2026-05-26
categories: [ml, transformers]
tags: [gpt, deep-learning, nlp]
math: true
---

<!--
  ============================================================
  FORMATTING GUIDE — delete this section when writing the real post
  ============================================================
-->

## Formatting Reference

Below are examples of the formatting tools available to you in this Hugo + PaperMod + KaTeX setup. Delete everything from here down and replace with your actual content.

---

### Headers

```markdown
## Section Title        (h2 — use for top-level sections)
### Subsection          (h3)
#### Sub-subsection     (h4)
```

---

### Inline Code and Code Blocks

Inline: use backticks — `model = GPT(config)`.

Fenced code block with syntax highlighting:

```python
import torch
import torch.nn as nn

class SelfAttention(nn.Module):
    def __init__(self, embed_dim, num_heads):
        super().__init__()
        self.attn = nn.MultiheadAttention(embed_dim, num_heads)

    def forward(self, x):
        out, _ = self.attn(x, x, x)
        return out
```

Another language:

```bash
pip install torch numpy tiktoken
python train.py --epochs 10 --lr 3e-4
```

---

### Math (LaTeX)

Inline math: the softmax function is $\sigma(z_i) = \frac{e^{z_i}}{\sum_j e^{z_j}}$.

Display math (centered, on its own line):

$$
\text{Attention}(Q, K, V) = \text{softmax}\!\left(\frac{QK^\top}{\sqrt{d_k}}\right) V
$$

Multi-line equations:

$$
\begin{aligned}
\mathcal{L} &= -\sum_{t=1}^{T} \log P(x_t \mid x_{<t}) \\
             &= -\sum_{t=1}^{T} \log \text{softmax}(W_e \cdot h_t)_{x_t}
\end{aligned}
$$

---

### Images

```markdown
![Alt text](/images/my-diagram.png)

<!-- With caption: -->
![Architecture diagram](/images/architecture.png)
*Figure 1: The transformer block.*
```

---

### Lists

Unordered:
- Tokenization
- Embedding
- Positional encoding

Ordered:
1. Preprocess the dataset
2. Build the vocabulary
3. Train the model
4. Generate text

---

### Blockquotes

> "What I cannot create, I do not understand." — Richard Feynman

---

### Tables

| Hyperparameter | Value |
|----------------|-------|
| Layers         | 12    |
| Heads          | 12    |
| Embed dim      | 768   |
| Context length | 1024  |

---

### Links

[Attention Is All You Need (Vaswani et al.)](https://arxiv.org/abs/1706.03762)

---

### Bold, Italics, Strikethrough

**bold text** / *italic text* / ~~strikethrough~~

---

<!-- END OF FORMATTING GUIDE — your real post starts below -->

