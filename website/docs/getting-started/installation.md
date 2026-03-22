---
sidebar_position: 2
title: "Installation"
description: "Install Gauss from a Linux repository checkout."
---

# Installation

## Recommended

```bash
# From the root of a checked-out math-inc/opengauss repository
./scripts/install.sh
```

This repository-local installer targets Linux checkouts, with Ubuntu, Debian, and WSL as the primary supported environments. It keeps code in your existing checkout, writes runtime state to `~/.gauss/`, exposes `gauss` via `~/.local/bin/gauss`, and prewarms `~/GaussWorkspace`.
When the installer runs in an interactive terminal, it finishes by opening `gauss-open-session` in that preconfigured project.

## Compatibility Behavior

- `gauss` is the primary command
- `gauss update` expects the active CLI to come from a checked-out `math-inc/opengauss` git repository
- if you already have `~/.gauss/`, the installer reuses it

## After Install

If you ran the installer headlessly or passed `--no-launch`, reopen the workflow session manually:

```bash
gauss-open-session
```

The default `~/GaussWorkspace` project is already initialized and selected for the managed Lean workflows. If you want to switch to a different project, use:

```text
/project use /path/to/project
```

## Windows

Native Windows is not a primary target. Use WSL2 when possible.
