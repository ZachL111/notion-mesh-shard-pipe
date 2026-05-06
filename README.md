# notion-mesh-shard-pipe

`notion-mesh-shard-pipe` keeps a focused SQL implementation around distributed systems. The project goal is to implement an SQL distributed systems project for shard constraint solving, using bounded scenario files and conflict explanations.

## Why It Exists

I want this repository to be useful as a quick reading exercise: fixtures first, implementation second, verifier last.

## Notion Mesh Shard Pipe Review Notes

The first comparison I would make is `membership churn` against `replica lag` because it shows where the rule is most opinionated.

## Features

- `fixtures/domain_review.csv` adds cases for quorum health and lease drift.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/notion-mesh-shard-walkthrough.md` walks through the case spread.
- The SQL code includes a review path for `membership churn` and `replica lag`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Architecture Notes

The core code exposes a scoring path and the added review layer uses `signal`, `slack`, `drag`, and `confidence`. The domain terms are `quorum health`, `lease drift`, `replica lag`, and `membership churn`.

The SQL checks add a separate view over the domain review fixture.

## Usage

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Tests

The check exercises the source code and the review fixture. `recovery` is the high score at 206; `edge` is the low score at 148.

## Limitations And Roadmap

The repository is intentionally scoped to local checks. I would expand it by adding adversarial fixtures before adding features.
