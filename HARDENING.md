<!-- markdownlint-disable -->

# Hardening Report: jacobtomlinson--gha-find-replace/v3

> This file was generated automatically by the hardening agent.

**Policy SHA:** `d636be7e43ef829af6e853da6b3c7566db9f72fe`

**Test Policy SHA:** `843adf9e4b8f85d0c08b27b9d0b09dd094b54702`

**Harden Agent Version:** `2`

Action **jacobtomlinson--gha-find-replace/v3** was hardened automatically. 1 finding(s) were identified and resolved across 1 iteration(s).

## Findings Fixed

### unpinned-uses (severity: high)

Docker action runs.image uses a mutable tag instead of a SHA digest: `image: "docker://ghcr.io/jacobtomlinson/gha-find-replace:3.0.5"`. Pin it to an @sha256: digest.

Locations:

- `action.yml:26`

## Iteration Notes

### Iteration 1

**Fixes applied:** unpinned-uses

**Notes:**

Pinned runs.image to docker://ghcr.io/jacobtomlinson/gha-find-replace:3.0.5@sha256:2c691f105028671938545a51b2064cc378c8d93971a5009c39974362bf4f5429, keeping the docker:// scheme and the tag inline.

