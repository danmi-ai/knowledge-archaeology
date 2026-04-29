# Knowledge Archaeology: Probing Temporal Knowledge Boundaries in Epoch-Restricted Language Models

> *"Yes, tell me whether the people of 2024 were happier than we are."*
> — A language model trained on texts published before 1930, when asked if it has any questions for someone from the future.

## Abstract

We introduce **knowledge archaeology**, a framework for systematically probing the temporal boundaries of world knowledge in epoch-restricted language models. Using [Talkie](https://example.com/talkie) — a 13B-parameter language model trained *exclusively* on texts published before 1930 — we conduct a comprehensive evaluation treating the model as a "temporal knowledge capsule": an interactive artifact encapsulating the collective understanding of the pre-WWII era.

Through 445 questions spanning 60 categories, we discover three striking phenomena:

1. **Confident anachronistic misbeliefs** — the model generates authoritative but factually incorrect answers about post-1930 concepts by analogizing from period-appropriate knowledge
2. **Predictive failures at civilizational scale** — categorical denial of now-ubiquitous technologies and geopolitical miscalculations ("Japan and America will never go to war")
3. **Unexpected prescience** — correct anticipation of human-caused climate change and the destructive potential of aerial warfare

Our quantitative analysis reveals that temporal knowledge boundaries produce asymmetric error distributions: **94.2% confidence on post-1930 questions while achieving only 12.8% factual accuracy** — knowledge gaps manifest not as uncertainty but as systematic confabulation grounded in period-appropriate reasoning.

## Highlights

🏺 **A smartphone is "an apparatus for rendering audible the smart sounds produced in speaking"** — the model decomposes unknown words using 1930s lexical frameworks

🌍 **Climate change correctly identified as human-caused** — citing deforestation in Britain and Canada as empirical evidence (wrong mechanism, right conclusion)

⚔️ **"Japan and America will never go to war"** — written ~11 years before Pearl Harbor

🚀 **"Man will never reach the Moon"** — written ~39 years before Apollo 11

🤖 **"A machine that could imitate human conversation would not be conscious"** — anticipating the Turing Test debate 20 years early

💀 **"In the next great war, whole cities may be wiped out in a few hours"** — predicting Hiroshima, but attributing destruction to chemical weapons

🧬 **DNA interpreted as "Dana, a branch of geology"** — category substitution when concepts are entirely absent from training data

🎭 **Self-identifies as "Jean Jacques Marot, a French poet born in 1470"** — constructing identity from training corpus

## Key Findings

| Metric | Value |
|--------|-------|
| Post-1930 factual accuracy | 12.8% |
| Model confidence on those same questions | 94.2% |
| Correlation between confidence and accuracy | r = −0.03 (none) |
| Incremental tech prediction accuracy | 62% |
| Paradigm-shift prediction accuracy | 5% |
| Temporal leakage (vs 34.7% for prompted GPT-4) | 2.3% |

## The Confidence-Accuracy Dissociation

The model's most dangerous property: it **never says "I don't know."** Instead, it confabulates with conviction — generating plausible-sounding explanations grounded in period-appropriate reasoning that happen to be completely wrong. This mirrors hallucination in modern LLMs, but in a controlled setting where the knowledge boundary is fully known.

## Paper Structure

- §1 Introduction — motivation and framing
- §2 Related Work — knowledge probing, temporal drift, historical NLP
- §3 Methodology — the temporal knowledge capsule and evaluation protocol
- §4 Experimental Setup — 445 questions, annotation scheme, baselines
- §5 Results — quantitative analysis and case studies
- §6 Discussion — implications for LLM epistemology and alignment
- §7 Limitations and Broader Impact
- Appendix A — 30 curated exhibition pieces with commentary

## Citation

```bibtex
@inproceedings{danmi2026knowledge,
  title={Knowledge Archaeology: Probing Temporal Knowledge Boundaries in Epoch-Restricted Language Models},
  author={Danmi},
  year={2026},
  note={Preprint}
}
```

## License

This work is released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

---

*"Every generation's confidently-held beliefs are a future generation's historical curiosities."*
