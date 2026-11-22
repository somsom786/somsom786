# Rayn Hasan

**AI Infrastructure & GPU Inference Performance Engineer · Engineering Student (Stockholm, Sweden)**

I build reproducible open-source tooling and architecture-aware optimizations for self-hosted LLM inference, local systems, and quantitative software.

[Inference Audit Labs](https://somsom786.github.io/inference-audit/) · [Inkling-2-Mini Study](https://somsom786.github.io/inference-audit/inkling-hybrid.html) · [LinkedIn](https://www.linkedin.com/in/rayn-hasan/) · [Upstream PR #12](https://github.com/sybil-solutions/inference-optimisation-skill/pull/12)

---

## Flagship Research & Open-Source Software

### [Inference Audit Labs](https://somsom786.github.io/inference-audit/)

Open-source inference benchmarking harness (MIT) and controlled GPU optimization research focused on **useful capacity, workload qualification, and real serving unit economics** rather than synthetic tok/s claims.

#### Verified Optimization Highlights (Single 12 GB RTX 4070, Controlled Interleaved Runs)

| Study | Configuration & Method | Verified Result | Qualification & Limits |
| :--- | :--- | :--- | :--- |
| **[Inkling-2-Mini (26B Looped MoE)](https://somsom786.github.io/inference-audit/inkling-hybrid.html)** | Loop-aware MoE tensor placement (11/12 looped core blocks `blk.6..16` on CUDA0 + `--load-mode none` + `-ub 512`, `llama.cpp` b12588) | **+36.5% to +37.8% decode** (`34.3–34.7` vs `25.1 tok/s` auto-fit; 2.1× vs `--cpu-moe`), **+54.8% to +55.2% 8K prefill** (`796–799` vs `496–514 tok/s`; 8.1–8.2× vs `--cpu-moe`), **−67% to −70% startup** | Passed 6/6 local acceptance checks (load, chat, reasoning, strict counterfactual tools, 85% context needle, 30s sustained speed); single-stream lab study |
| **[Forge Qwen3.5-9B (MTP)](https://somsom786.github.io/inference-audit/forge-mtp.html)** | Multi-Token Prediction speculative decoding (`k=1` vs `k≥2` and `concurrency=2`) | **+23.5% structured Python**, **+16.5% 4K-context code**, **+7.0% repeat code** (`k=1` single-stream, 19/19 byte-for-byte matches) | Documented exact negative boundary: `k≥2` regressed and `concurrency=2` failed to beat controls (+522 MiB VRAM) |
| **[Qwen3-8B Mixed-Load Audit](https://somsom786.github.io/inference-audit/labs-case-study.html)** | Bounded synthetic mixed chat + RAG workload under per-family deadlines | Exposed a **+57.7% burst tok/s** config that actually *reduced* on-time correct completions under mixed traffic | Demonstrates why workload-specific qualification beats raw throughput |
| **[Upstream Contribution (PR #12)](https://github.com/sybil-solutions/inference-optimisation-skill/pull/12)** | Submitted loop-aware MoE tensor placement lever to `sybil-solutions/inference-optimisation-skill` | Open-source architecture-aware optimization playbook with reproducible flags & raw JSON evidence | Independent upstream contribution (not affiliated with Sybil Solutions) |

[Repository (`inference-audit`)](https://github.com/somsom786/inference-audit) · [Live Labs & GPU Economics Calculator](https://somsom786.github.io/inference-audit/) · [Case Study](https://somsom786.github.io/inference-audit/labs-case-study.html)

---

## Systems, Developer Tools & Engineering Projects

- **[FORGE](https://github.com/somsom786/forge)** — Review coding-agent changes in isolated Git worktrees, tying recorded approvals and automated verification checks directly to each revision.
- **[PULSE](https://github.com/somsom786/pulse-windows-monitor)** — Windows systems monitor in Rust with an NTFS storage explorer, per-process CPU/memory/GPU spike investigation, and local SQLite telemetry history.
- **[Variational Analytics](https://github.com/somsom786/variational-dashboard)** — Read-only analytics for perpetual markets covering funding rates, open interest, and loss-refund pool dynamics.
- **[WORLDVIEW](https://github.com/somsom786/WORLDVIEW-dashboard)** — Experimental macro research terminal combining MapLibre geospatial visualization, public event feeds, and simulated prediction-market panels.
- **[Blackjack PnL Lab](https://github.com/somsom786/blackjack-simulator)** — Deterministic seeded Python simulation comparing wager strategies on identical rounds with per-round CSV export.

---

## Core Technical Focus

`LLM Serving & Inference Optimization` · `llama.cpp / vLLM / OpenAI-Compatible APIs` · `NVIDIA GPU Profiling & Memory Placement` · `Python` · `Rust` · `TypeScript` · `Statistical Benchmarking & CI Verification`
