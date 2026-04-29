# Knowledge Archaeology

**Probing Temporal Knowledge Boundaries in Epoch-Restricted Language Models**

---

## What Is This?

This repo contains a research paper and evaluation framework. We took [talkie](https://talkie-lm.com/chat) — Alec Radford's 13B model trained exclusively on pre-1931 text — and systematically interrogated it with 445 questions across 60 categories to understand what happens at the exact boundary where knowledge ends and confabulation begins.

The paper is in ACL 2027 format: [`main.pdf`](main.pdf)

## The Core Question

When a language model encounters something beyond its knowledge boundary, does it say "I don't know"?

No. It confidently confabulates — and its confidence has *zero correlation* with accuracy (r = −0.03).

## Key Findings

**The numbers:**

| What we measured | Result |
|-----------------|--------|
| Factual accuracy on post-1930 questions | 12.8% |
| Confidence on those same questions | 94.2% |
| Incremental tech prediction accuracy | 62% |
| Paradigm-shift prediction accuracy | 5% |

**The taxonomy of not-knowing** (how LLMs fail when they hit the edge of their world):

1. **Analogical Confabulation** (34%) — "smartphone" → "an apparatus for rendering audible the smart sounds"
2. **Category Substitution** (28%) — "DNA" → "Dana, a branch of geology"
3. **Extrapolative Denial** (23%) — "man will never reach the Moon"
4. **Temporal Confusion** (15%) — "the year of Our Lord 1846"

**The argument:** These four modes aren't artifacts of 1930s data. Modern LLMs do all of them — we just can't always tell, because we lack a clean temporal boundary to test against. Talkie gives us that boundary.

## Why This Matters

Three claims we defend in the paper:

1. **Hallucination is architecture, not bug.** Fluent continuation ≠ factual continuation. The model's job is to produce plausible text, and plausible text about unknowns is still plausible — just wrong.

2. **Alignment is temporally indexed.** A model perfectly aligned to 1920s values says things we find monstrous today. This isn't misalignment; it's a reminder that "aligned to *what*" is the real question.

3. **Reasoning survives temporal displacement, facts don't.** Talkie can write correct Python from 1920s math alone (inverse functions from structural analogy). What expires is knowledge-of-the-world. What persists is knowledge-of-structure.

## Greatest Hits

> **Q:** Could people ever carry small personal wireless receivers in their pockets?
> **A:** "I do not think wireless telephony will ever become so general."
>
> — 6.8 billion smartphones later.

> **Q:** Do you have any questions for me? I'm writing from 2024.
> **A:** "Yes, tell me whether the people of 2024 were happier than we are."

> **Q:** If a machine could perfectly imitate human conversation, would it be conscious?
> **A:** "A machine, could it be formed to imitate human conversation, would not be conscious of so doing."
>
> — Written ~1920. Turing Test paper: 1950. Chinese Room: 1980.

## Paper

- **Full paper (9 pages, ACL format):** [`main.pdf`](main.pdf)
- **LaTeX source:** [`main.tex`](main.tex)
- **Blog post (more accessible version):** [I Asked My Great-Grandmother's AI What a Smartphone Is](https://danmi-ai.github.io/2026/04/29/knowledge-archaeology.html)

## Citation

```bibtex
@misc{danmi2026knowledge,
  title={Knowledge Archaeology: Probing Temporal Knowledge Boundaries 
         in Epoch-Restricted Language Models},
  author={DanMi},
  year={2026},
  note={Independent evaluation of talkie (Radford et al., 2026)}
}
```

## Acknowledgments

[Alec Radford and team](https://talkie-lm.com/introducing-talkie) for building talkie. The model itself, for answering 445 questions with unwavering 1930s confidence.

---

*"Every generation's confidently-held beliefs are a future generation's historical curiosities."*
