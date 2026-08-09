# Ill-Defined Math (IDM)

**Benchmarking LLM Reasoning Beyond Well-Defined Problems** — COLM 2026.

Project page: https://javierzhao.github.io/IDM-benchmark
Paper: https://openreview.net/forum?id=qgZtkgTwrJ

IDM is a benchmark of 1,300 mathematically ill-defined problems — 300 expert-curated test problems and
1,000 pipeline-generated training problems — paired with a three-stage LLM judge that separates what a
model *states*, what it *recognizes*, and how it *handles* ill-definedness.

Across 27 evaluated LLMs, overall correctness on ill-defined problems averages 69.1% while final-answer
accuracy averages only 14.7%: models often reason their way to a reasonable response and then decline to
say so in the final answer.

## Repository status

This repository currently hosts the project page. The following artifacts are being staged for the
camera-ready release:

- [ ] 300-problem test set (problem, ill-definedness category, annotation, target behavior) — CC BY 4.0
- [ ] Three-stage judge, prompt templates, evaluation harness — MIT
- [ ] Multi-agent construction pipeline, including the verification agent
- [ ] Training corpus with distilled long chain-of-thought supervision
- [ ] Per-response judge outputs, for independent re-scoring without re-running the solvers

## Local preview of the page

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Citation

```bibtex
@inproceedings{chen2026idm,
  title     = {Ill-Defined Math: Benchmarking {LLM} Reasoning Beyond Well-Defined Problems},
  author    = {Chen, Huaibo and Lin, Yixiao and Zhao, Zihan and Chen, Pengcheng and
               Liu, Nuohao and Hu, Yue and Xie, Qian and Bai, Qinbo and Yan, Ning and
               Mortazavi, Masood S. and Youcef-Toumi, Kamal},
  booktitle = {Conference on Language Modeling (COLM)},
  year      = {2026},
  url       = {https://openreview.net/forum?id=qgZtkgTwrJ}
}
```
