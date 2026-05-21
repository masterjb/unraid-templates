# x265-butler — Release Notes

Container image: `ghcr.io/masterjb/x265-butler` ([GHCR](https://github.com/users/masterjb/packages/container/package/x265-butler))
Source repository: `gitlab.com/MisterJB/x265-butler` (private; access on request).

---

## v2.13.0 — M2 v2.0 Polish + Power (Milestone 2 close)

**Released:** 2026-05-21 (UTC) · **Image:** `ghcr.io/masterjb/x265-butler:2.13.0` (anonymously pullable)

x265-butler v2.13.0 closes Milestone 2 — eleven UI / engine / pipeline / supply-chain phases shipped on top of the v1.0 MVP baseline.

### Phases shipped in M2 (P7–P17, 11 of 11)

- **P7** Stats + Dashboard
- **P8** UI Redesign cross-page
- **P9** Release-Eng V2 + Supply-Chain
- **P10** Pipeline V2 + Container-Polish (libvmaf bake-in)
- **P11** Encoder-Benchmark (Smart-Sampling + Pareto-Frontier)
- **P12** Encoder-Profile-Editor + Settings-Polish
- **P13** Library Power-User
- **P14** Multi-Share Support
- **P15** Storage-Analyzer
- **P16** Auto-Scan-on-Change (chokidar)
- **P17** CA Publication (this release)

### Image digest (v2.13.0)

```
sha256:6493543392f338ed09e08c7143edbdfe3347e6f26679f421d6515fc872d4d940
```

Single-architecture `linux/amd64` (unRAID target). Config layer: `sha256:868e9c98e83a24886ca86ad14262cc33bb0506b3de71142e09bd7fd604ee31fb`.

### Verify

```
docker logout ghcr.io
docker pull ghcr.io/masterjb/x265-butler:2.13.0
```

GHCR manifest endpoint returns `HTTP/2 200` via anonymous Bearer token (Docker Registry v2 protocol).

### Build pipeline

GitLab CI pipeline (M1 v1.5.0 historical reference): https://gitlab.com/MisterJB/x265-butler/-/pipelines/2500969219
(The source repository is private; CI artifacts and pipeline output are not publicly browsable. M2 image build pipelines run inside the same private project; M2-shipped artifact is the GHCR `:2.13.0` image referenced above.)

### Forum / discussion

unRAID forum support thread (umbrella for all `masterjb` docker templates):
https://forums.unraid.net/topic/182094-support-human-126094-docker-templates/

---

## v1.5.1 — M1 v1.0 MVP, GHCR-public release (historical)

**Released:** 2026-05-05 (UTC) · **Image:** `ghcr.io/masterjb/x265-butler:1.5.1` (anonymously pullable)

First publicly distributed release. Supersedes v1.5.0 (which was halted at a GitLab CR registry-target-mismatch incident; resolved by switch to GHCR).

### Image digests (v1.5.1 — multi-architecture)

- Manifest list (image index): `sha256:4e506d3022e34e2e99d8e207292670337b4aa0045384e5e7eda222f1866ef028`
- `linux/amd64`: `sha256:daaee95429d46b07130823aa8d64b0c56c7331448843af0634acc9b19a256b6d`
- `linux/arm64`: `sha256:e0bbc648f046e16920a2cf8f85b8142e15f4c288375b0b837e37b70848c26f67`

### Build pipeline (M1 v1.5.0)

https://gitlab.com/MisterJB/x265-butler/-/pipelines/2500969219

(Multi-arch build resolved during M2 P10 Pipeline V2 + Container-Polish; M2 currently ships `amd64` only because unRAID targets that platform exclusively — `arm64` build paused pending demand.)

---

## v1.5.0 — M1 v1.0 MVP, internal GitLab CR release (historical / deferred)

Released internally on `registry.gitlab.com/misterjb/x265-butler:v1.5.0`; deferred public release after a target-mismatch incident. Superseded by v1.5.1 (GHCR public). Manifest digest preserved as historical artifact: `sha256:cac261df88a083c168983090c97da80c6433145eb418bedf81bdbd8858176b06`.
