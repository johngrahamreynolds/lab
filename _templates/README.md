# Post templates

Four kinds of post cover almost everything. Quarto ignores folders starting
with `_`, so these never render. Start a post by copying one:

```bash
cp -r _templates/result posts/2026-11-20-chance-2048-rq1
```

| Template | Use for | Usually drafted from |
| --- | --- | --- |
| `question/` | Opening a project: what is open and the smallest test | the project's `docs/QUESTION.md` |
| `build-log/` | A milestone in building the system | ADRs and experiment records |
| `result/` | A finding, with its figure regenerated from run data | an experiment record's Result section |
| `negative-result/` | Something that did not work, and what it ruled out | an abandoned experiment |

Every post:

- starts as `draft: true` and is tagged with a pillar, the project, and its kind
- links the exact commit or release it describes
- regenerates any number or figure from data (rendered locally, frozen in
  `_freeze/`, committed)

Each post also drafts a section of the project's paper; the template says
which.
