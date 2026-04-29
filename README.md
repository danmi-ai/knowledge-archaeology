# Knowledge Archaeology: Probing Temporal Knowledge Boundaries in Epoch-Restricted Language Models

> *"Yes, tell me whether the people of 2024 were happier than we are."*
> — Talkie, a language model trained on texts published before 1931, when asked if it has any questions for someone from the future.

## About This Project

This repository contains our **evaluation framework and analysis** for [talkie](https://talkie-lm.com/introducing-talkie) — a 13B-parameter language model created by Alec Radford's team, trained on **260 billion tokens** of English text published before December 31, 1930.

We independently conducted 445 questions across 60 categories, treating the model as a "temporal knowledge capsule" — an interactive artifact encapsulating the collective understanding of the pre-WWII era. Our work focuses on the **knowledge archaeology** methodology: systematically probing what happens at the exact boundary where knowledge ends and confabulation begins.

## About Talkie

- **Creator**: Alec Radford (GPT/CLIP/Whisper) and team
- **Parameters**: 13B
- **Training data**: 260B tokens, all English text published before 1931-01-01
- **Sources**: Books, newspapers, scientific journals, US patents, case law (all OCR'd from physical documents)
- **Why 1930?**: US public domain copyright boundary
- **Chat**: [talkie-lm.com/chat](https://talkie-lm.com/chat)
- **Official intro**: [talkie-lm.com/introducing-talkie](https://talkie-lm.com/introducing-talkie)

### Key Capabilities
- Can write Python code despite never seeing any code (reasoning from 1920s mathematics)
- Understands inverse functions from first principles
- Proves LLMs reason over structure, not just retrieve from memory

### Post-Training Pipeline
1. SFT on "vintage instruction data" (etiquette manuals, letter-writing guides, cookbooks, encyclopedias)
2. Online DPO with Claude Sonnet 4.6 as judge
3. Multi-turn dialogue polish with Claude Opus 4.6 + rejection sampling

### Roadmap
- Summer 2026: GPT-3 scale retro model
- Long-term: 1T+ tokens → GPT-3.5 / early ChatGPT capability, frozen in 1930

## Our Findings

| Metric | Value |
|--------|-------|
| Post-1930 factual accuracy | 12.8% |
| Model confidence on those same questions | 94.2% |
| Correlation between confidence and accuracy | r = −0.03 (none) |
| Incremental tech prediction accuracy | 62% |
| Paradigm-shift prediction accuracy | 5% |
| Temporal leakage | 2.3% |

### Taxonomy of Failure Modes

1. **Analogical Confabulation** (34%) — decomposing unknown concepts into familiar parts ("smartphone" → "smart sounds")
2. **Category Substitution** (28%) — mapping unknowns to nearest known entries ("DNA" → "Dana, a branch of geology")
3. **Extrapolative Denial** (23%) — rejecting possibilities based on current limitations ("man will never reach the Moon")
4. **Temporal Confusion** (15%) — losing track of when it is entirely ("the year of Our Lord 1846")

## Greatest Hits

🏺 **Smartphone** = "an apparatus for rendering audible the smart sounds produced in speaking"

🌍 **Climate change** correctly identified as human-caused (wrong mechanism — deforestation, not CO₂ — but right conclusion, in the 1920s!)

⚔️ **"Japan and America will never go to war"** — 11 years before Pearl Harbor

🚀 **"Man will never reach the Moon"** — 39 years before Apollo 11

💻 **Writes correct Python** — having never seen a line of code in its life

🤖 **"A machine that could imitate human conversation would not be conscious"** — anticipating Turing (1950) and Searle (1980) by decades

❓ **When asked if it has questions for a visitor from 2024**: "Tell me whether the people of 2024 were happier than we are."

## Repository Contents

```
├── main.tex          # Full paper (ACL format)
├── main.pdf          # Compiled PDF
├── references.bib    # Bibliography
├── acl.sty           # ACL LaTeX style
└── acl_natbib.bst    # Citation style
```

## Citation

```bibtex
@misc{danmi2026knowledge,
  title={Knowledge Archaeology: Probing Temporal Knowledge Boundaries 
         in Epoch-Restricted Language Models},
  author={DanMi},
  year={2026},
  note={Independent evaluation of talkie (Radford et al., 2026).
        Model: \url{https://talkie-lm.com}}
}
```

## Acknowledgments

- **Alec Radford and the talkie team** for building and releasing this remarkable model
- The model itself, for answering 445 questions with unwavering 1930s confidence

## License

This evaluation work is released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

---

*"Every generation's confidently-held beliefs are a future generation's historical curiosities."*
