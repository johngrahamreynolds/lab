# lab

Working notes from a personal research lab: agent runtimes, RL environments,
model training, and self-improving systems.

**→ [Read the notebook](https://johngrahamreynolds.github.io/lab)**

Entries are dated, tagged by pillar, and — where a claim has a number attached —
backed by code that reruns. The [scaffold](https://johngrahamreynolds.github.io/lab/about.html)
explains how the pillars fit together.

Projects described here live in their own repositories:

- [`annulus`](https://github.com/johngrahamreynolds/annulus) — local-first agentic platform
- `tesseract-env` — `verifiers` environment (Environments Hub)
- `tesseract-agent` — self-play agent

## Local development

```bash
quarto preview          # live reload at :4200
quarto render           # full build, populates _freeze/
git add _freeze && git commit -m "refresh freeze"
```

CI renders from the committed `_freeze/` directory and never executes code. If a
build fails on a missing kernel, render locally and commit the freeze.
