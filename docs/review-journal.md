# Review Journal

I treated `notion-mesh-shard-pipe` as a project where the smallest useful behavior should still be inspectable.

The local checks classify each case as `ship`, `watch`, or `hold`. That gives the project a small review vocabulary that matches its distributed systems focus without claiming live deployment or external usage.

## Cases

- `baseline`: `quorum health`, score 182, lane `ship`
- `stress`: `lease drift`, score 182, lane `ship`
- `edge`: `replica lag`, score 148, lane `ship`
- `recovery`: `membership churn`, score 206, lane `ship`
- `stale`: `quorum health`, score 171, lane `ship`

## Note

The repository should be understandable without pretending it is larger than it is.
