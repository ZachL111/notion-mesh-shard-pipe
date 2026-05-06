# Notion Mesh Shard Pipe Walkthrough

This note is the quickest way to read the extra review model in `notion-mesh-shard-pipe`.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | quorum health | 182 | ship |
| stress | lease drift | 182 | ship |
| edge | replica lag | 148 | ship |
| recovery | membership churn | 206 | ship |
| stale | quorum health | 171 | ship |

Start with `recovery` and `edge`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

The useful comparison is `membership churn` against `replica lag`, not the raw score alone.
