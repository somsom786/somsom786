# sombody

Independent developer in Stockholm. I build tools for AI infrastructure, local-first systems, and financial-market research.

[LinkedIn](https://www.linkedin.com/in/rayn-hasan/)

## AI Infrastructure & Software

### Inference Audit

**How much useful work can an LLM server actually deliver?**

Inference Audit runs bounded synthetic workloads against authorized OpenAI-compatible endpoints. It measures first-token latency, completion latency, and how many tasks finish correctly and on time. The saved observations can be checked and turned back into an HTML report offline.

In a mixed workload on one RTX 4070, four serving slots shortened the wait for the first token while reducing correct, on-time completions per second. That trade-off is why I built the audit around useful work under a deadline.

[Repository](https://github.com/somsom786/inference-audit) · [Interactive case study](https://somsom786.github.io/inference-audit/case-study.html) · [Measured Qwen3-8B audit](https://somsom786.github.io/inference-audit/reports/qwen3-8b-audit.html)

<a href="https://somsom786.github.io/inference-audit/reports/qwen3-8b-audit.html"><img src="https://somsom786.github.io/inference-audit/assets/qwen-report-preview.png" alt="Overview of a measured Qwen3-8B load sweep on an RTX 4070" width="640"></a>

### Developer tools and local systems

- **[FORGE](https://github.com/somsom786/forge)** — Review coding-agent work in isolated Git worktrees. The desktop app ties approvals and check results to the revision under review. [Verification screenshot](https://github.com/somsom786/forge/blob/main/docs/media/verification.png)
- **[PULSE](https://github.com/somsom786/pulse-windows-monitor)** — Inspect NTFS disk usage and investigate CPU, memory, and GPU spikes. The Windows app collects data in Rust and records local history in SQLite. [Storage explorer screenshot](https://github.com/somsom786/pulse-windows-monitor/blob/main/docs/media/storage-explorer.png)

## Web3, Trading & Experimental Systems

- **[Variational Analytics](https://github.com/somsom786/variational-dashboard)** — Read-only analytics for Variational perpetual markets, including funding rates, open interest, and the loss-refund pool. [Data client](https://github.com/somsom786/variational-dashboard/blob/main/src/lib/api.ts) · [Run locally](https://github.com/somsom786/variational-dashboard#run-locally)
- **[WORLDVIEW](https://github.com/somsom786/WORLDVIEW-dashboard)** — Experimental macro terminal combining a MapLibre map, public event feeds, and simulated prediction-market panels. [Hosted demo](https://worldview-dashboard.vercel.app/)
- **[Blackjack PnL Lab](https://github.com/somsom786/blackjack-simulator)** — Seeded Python simulator that compares two wager rules on identical rounds and exports the results to CSV.
