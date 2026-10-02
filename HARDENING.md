<!-- markdownlint-disable -->

# Hardening Report: jacobtomlinson--gha-find-replace/3.0.5

> This file was generated automatically by the hardening agent.

**Policy SHA:** `d636be7e43ef829af6e853da6b3c7566db9f72fe`

**Test Policy SHA:** `843adf9e4b8f85d0c08b27b9d0b09dd094b54702`

**Harden Agent Version:** `2`

Action **jacobtomlinson--gha-find-replace/3.0.5** was hardened automatically. 1 finding(s) were identified and resolved across 1 iteration(s).

## Findings Fixed

### unpinned-uses (severity: high)

The action.yml uses a Docker image referenced by a mutable tag (`3.0.5`) instead of an immutable SHA digest. This means the image could be silently replaced with a different (potentially malicious) version without any change to the action source. The failing reference is: `image: "docker://ghcr.io/jacobtomlinson/gha-find-replace:3.0.5"`. It should be pinned to a SHA digest, e.g. `image: "docker://ghcr.io/jacobtomlinson/gha-find-replace@sha256:<64-hex-char-digest>"`.

Locations:

- `action.yml:26`

## Iteration Notes

### Iteration 1

**Fixes applied:** unpinned-uses

**Notes:**

Pinned the Docker image reference in action.yml from `docker://ghcr.io/jacobtomlinson/gha-find-replace:3.0.5` to `docker://ghcr.io/jacobtomlinson/gha-find-replace:3.0.5@sha256:2c691f105028671938545a51b2064cc378c8d93971a5009c39974362bf4f5429`. The `docker://` scheme and `:3.0.5` tag are preserved inline alongside the immutable digest.

