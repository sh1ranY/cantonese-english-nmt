# Cantonese–English Neural Machine Translation

**ICRAI 2025 · Published research · Peixuan Yang, co-second author and presenter**

[Read the paper](https://doi.org/10.1109/ICRAI68431.2025.11396704)

This repository provides a concise guide to our collaborative study, *Optimized Fine-tuning and Pseudo-Data Strategies for Cross-Domain Low-Resource Language Cantonese-English Neural Machine Translation*. It is a publication companion, not a released training-code package.

## Research question

How can corpus preparation, NLLB fine-tuning, and pseudo-parallel data improve low-resource Cantonese–English translation, including transfer to a different domain?

## Method

1. Curate a parallel corpus of approximately 1.1 million sentence pairs.
2. Apply filtering, normalization, deduplication, and LaBSE-based semantic alignment.
3. Fine-tune NLLB-200-distilled-600M.
4. Generate pseudo-parallel data through reverse translation and compare nested sampling scales.
5. Evaluate in-domain translation and legal-domain generalization.

## Published results

| Setting | Metric | Reported score |
| :--- | :--- | ---: |
| Best in-domain model | BLEU | 29.63 |
| Best in-domain model | chrF | 56.65 |
| Legal-domain evaluation | BLEU | 15.87 |

The study identifies a 200k pseudo-data to 200k original-data setting as optimal within its experiments. These are the paper's reported results, not new runs from this repository. Scores depend on the paper's datasets and evaluation setup and should not be compared with unrelated benchmarks without matching those conditions.

## My contribution

I contributed to corpus construction and cleaning, NLLB fine-tuning, and pseudo-data sampling experiments. I am marked as a co-second author in the published paper and presented the work at ICRAI 2025. Findings and reported scores belong to the collaborative study.

## Paper and citation

Yichao Wang, Yukun Gao, Peixuan Yang, and Bohan Zhao. **Optimized Fine-tuning and Pseudo-Data Strategies for Cross-Domain Low-Resource Language Cantonese-English Neural Machine Translation.** 2025 11th International Conference on Robotics and Artificial Intelligence (ICRAI).

DOI: [10.1109/ICRAI68431.2025.11396704](https://doi.org/10.1109/ICRAI68431.2025.11396704)

```bibtex
@inproceedings{wang2025cantonese,
  author = {Wang, Yichao and Gao, Yukun and Yang, Peixuan and Zhao, Bohan},
  title = {Optimized Fine-tuning and Pseudo-Data Strategies for Cross-Domain Low-Resource Language Cantonese-English Neural Machine Translation},
  booktitle = {2025 11th International Conference on Robotics and Artificial Intelligence (ICRAI)},
  year = {2025},
  doi = {10.1109/ICRAI68431.2025.11396704}
}
```

## Availability

The published paper is linked above. This repository does not redistribute the publisher PDF, source books, training corpus, or model checkpoints. Training scripts and evaluation artifacts are not currently released here.

---

[Peixuan Yang's profile](https://github.com/sh1ranY)

## Experiment companion

- [Workflow, documented settings and reproduction gaps](docs/experiment-guide.md)
- [Reported headline results as CSV](results/reported-results.csv)

These additions describe the study; they do not constitute released training scripts or a new replication.
