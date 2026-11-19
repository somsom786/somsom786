# Rayn Hasan

I'm an independent developer based in Stockholm. I build tools for measuring AI systems, reviewing software changes, and working with local and financial-market data.

[LinkedIn](https://www.linkedin.com/in/rayn-hasan/)

## AI Infrastructure & Software

### Inference Audit

**Reproducible performance audits for self-hosted LLM inference.** Inference Audit measures first-token and completion latency, token throughput, and how many requests return correct results on time. It saves the observations so the audit can be checked and rebuilt offline.

[Source code](https://github.com/somsom786/inference-audit) · [RTX 4070 case study](https://somsom786.github.io/inference-audit/case-study.html) · [Measured Qwen3-8B audit](https://somsom786.github.io/inference-audit/reports/qwen3-8b-audit.html)

<a href="https://somsom786.github.io/inference-audit/reports/qwen3-8b-audit.html"><img src="https://somsom786.github.io/inference-audit/assets/qwen-report-preview.png" alt="Inference Audit report showing measured Qwen3-8B performance and workload conditions on an RTX 4070" width="640"></a>

In one RTX 4070 study, raising concurrency improved throughput on uniform chat traffic. A mixed workload showed why I also track tail latency and correct, on-time responses before calling a configuration faster.

### FORGE and PULSE

- **[FORGE](https://github.com/somsom786/forge)** — Windows desktop workspace for reviewing coding-agent changes in isolated Git worktrees. See the diff, approve actions, and attach check results to the exact revision under review. [Verification screenshot](https://github.com/somsom786/forge/blob/main/docs/media/verification.png)
- **[PULSE](https://github.com/somsom786/pulse-windows-monitor)** — Local Windows monitor for inspecting NTFS disk usage, live process telemetry, and historical spikes. Rust handles collection and SQLite stores the history. [Storage Explorer screenshot](https://github.com/somsom786/pulse-windows-monitor/blob/main/docs/media/storage-explorer.png)

## Web3, Trading & Experimental Systems

- **[Variational Analytics](https://github.com/somsom786/variational-dashboard)** — A read-only derivatives dashboard with protocol metrics, sortable markets, funding rates, and loss-refund data. The repository includes local run instructions.
- **[WORLDVIEW](https://github.com/somsom786/WORLDVIEW-dashboard)** — Experimental macro terminal that puts a map, event feeds, and market panels in one workspace. The demo uses a mix of public feeds and simulated data. [Open the demo](https://worldview-dashboard.vercel.app/)
- **[Blackjack PnL Lab](https://github.com/somsom786/blackjack-simulator)** — A fake-money practice table and seeded Python simulator. It compares wager rules on identical rounds and exports a replayable CSV.
