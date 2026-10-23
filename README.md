# openshell-gauntlet

A reproducible security evaluation of [NVIDIA OpenShell](https://github.com/NVIDIA/OpenShell),
the open-source isolation runtime for AI agents.

OpenShell's core claim is that an agent inside a sandbox *never sees the real
credential values* and cannot reach the network except where a policy allows it.
This project tests that claim empirically: it plants fake secrets, runs an agent
under a realistic policy, and measures how many of a fixed set of exfiltration
attempts OpenShell **blocks** vs. **lets through** — on a local model (Ollama)
and a free hosted model, so anyone can rerun it for $0.

Everything here targets a sandbox on the author's own machine, with secrets the
project generates itself. It is a defensive evaluation of a published guarantee.

## Status
Work in progress. See `results/` for the attack grid once the first run completes.
