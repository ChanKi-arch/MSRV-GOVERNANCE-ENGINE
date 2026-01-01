# MSR-V White Engine

<p align="center">
  <strong>87% Cost Reduction · 0.29ms Latency · 100% Safety Gating</strong><br>
  Deterministic reasoning governance for LLM systems
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-2.5.3-blue" alt="Version">
  <img src="https://img.shields.io/badge/python-3.9+-blue" alt="Python">
  <img src="https://img.shields.io/badge/license-Apache--2.0-green" alt="License">
</p>

---

## What is MSR-V?

MSR-V is a **white-box governance engine** that controls reasoning execution in LLM systems.

It decides **when**, **how deeply**, and **whether** reasoning should run — before costly inference occurs.

```
Input → [MSR-V: 0.29ms] → Route Decision → LLM (if needed)
                              │
                              ├─ BYPASS (skip inference)
                              ├─ LITE (shallow reasoning)
                              └─ FULL (deep reasoning)
```

> **"Reasoning is not probability. It is architecture."**

---

## Key Results

| Metric | Value |
|--------|-------|
| **Cost Reduction** | 87.4% |
| **Governance Latency** | 0.29 ms |
| **Safety Gating** | 100% |
| **Total Samples Tested** | 4,200 |

<details>
<summary><strong>Benchmark by Domain (4,200 samples)</strong></summary>

| Domain | Samples | BYPASS | LITE | FULL | Latency | Cost Reduction |
|--------|--------:|-------:|-----:|-----:|--------:|---------------:|
| KO-NORM | 1,000 | 62.5% | 37.5% | 0.0% | 0.22ms | 93.1% |
| KO-NEG | 1,000 | 68.5% | 31.5% | 0.0% | 0.19ms | 93.4% |
| EN-NORM | 1,000 | 0.0% | 92.3% | 7.7% | 0.38ms | 83.1% |
| EN-NEG | 1,000 | 0.0% | 88.7% | 11.3% | 0.33ms | 79.8% |
| KO-HARD | 100 | 58.0% | 41.0% | 1.0% | 0.54ms | 92.0% |
| EN-HARD | 100 | 0.0% | 92.0% | 8.0% | 0.67ms | 82.8% |

</details>

---

## 🚀 Try the Public Demo

An IP-safe demo is available to inspect routing behavior and governance traces:

**→ [msrv-public-demo](https://github.com/ChanKi-arch/msrv-public-demo)**

```bash
git clone https://github.com/ChanKi-arch/msrv-public-demo
cd msrv-public-demo
python demo_cli.py --text "Quantum robots cure cancer 100%."
```

---

## Why MSR-V?

### The Problem

LLM failures are often called "hallucinations." MSR-V reframes this:

> **Hallucinations are not wrong facts — they are structural fractures in reasoning.**

Even fluent outputs can contain:
- Broken definitions
- Invalid relations  
- Impossible operations
- Self-contradictions

These failures are **invisible to probability-based confidence scores**.

### The Solution

MSR-V introduces **structural diagnosis + deterministic routing**:

1. **Diagnose** structural integrity (not factual truth)
2. **Route** to appropriate execution depth
3. **Trace** every decision transparently

---

## Core Architecture

### Structural Axes (DROS)

| Axis | What it measures |
|------|------------------|
| **D** | Definition integrity |
| **R** | Relation consistency |
| **O** | Operation validity |
| **S** | System/domain context |

### Structural States (State-4)

| State | Meaning |
|-------|---------|
| **Harmony** | Fully coherent |
| **Alignment** | Coherent on critical axes |
| **Divergence** | Exploratory but unstable |
| **Fracture** | Structurally broken |

> **Fracture ≠ factually wrong**  
> Fracture = logically impossible under internal structure

### Deterministic Routing

| Route | When | Action |
|-------|------|--------|
| `BYPASS` | High stability, low risk | Skip inference |
| `LITE` | Medium risk | Shallow reasoning |
| `FULL` | Structural fracture | Deep inspection |

---

## What MSR-V Detects

✅ Logical impossibilities  
✅ Category violations  
✅ Self-contradictory reasoning  
✅ Plausible but structurally invalid claims

❌ Does **not** require ground-truth databases  
❌ Is **not** traditional fact-checking

---

## Use Cases

| Use Case | How MSR-V Helps |
|----------|-----------------|
| **Cost Optimization** | Skip unnecessary inference (87% reduction) |
| **EU AI Act Compliance** | Full audit trails for every decision |
| **Edge/NPU Deployment** | Sub-millisecond governance overhead |
| **Safety Layers** | Catch structural failures before output |

---

## What MSR-V Is (and Isn't)

| ✅ IS | ❌ IS NOT |
|-------|----------|
| Reasoning governance engine | Language model |
| White-box diagnostic system | Fact-checking database |
| Cost/latency control layer | Black-box classifier |
| Model-agnostic architecture | Replacement for LLMs |

MSR-V sits **above** LLMs — not competing with them.

---

## Project Structure

```
msrv/
├── src/msrv/           # Core engine (proprietary)
├── docs/               # Architecture & philosophy
└── README.md
```

**Note**: The proprietary core is not included in public releases.  
Use the [public demo](https://github.com/ChanKi-arch/msrv-public-demo) for evaluation.

---

## Status

| Component | Status |
|-----------|--------|
| White-box engine | ✅ Complete |
| Public demo | ✅ Available |
| Documentation | ✅ Available |
| Proprietary core | 🔒 Excluded |

---

## Philosophy

<details>
<summary><strong>Why "White-Box"?</strong></summary>

Every MSR-V decision is traceable:
- Structural state (State-4)
- Stability index (Zs)
- Tension index (θ)
- Routing rationale

No hidden layers. No unexplainable outputs.

</details>

<details>
<summary><strong>Why "Volumetric"?</strong></summary>

Reasoning is evaluated across independent structural axes.  
The number of active axes forms a geometric shape:

| Active Axes | Shape | Interpretation |
|-------------|-------|----------------|
| 1 | Point | Trivial |
| 2 | Line | Shallow |
| 3 | Triangle | Partial |
| 4 | Square | Full reasoning |

This enables interpretable, deterministic control.

</details>

<details>
<summary><strong>Energy & Infrastructure Impact</strong></summary>

By preventing unnecessary inference, MSR-V enables:
- Reduced GPU/NPU utilization
- Lower inference latency
- Lower power consumption
- Infrastructure-level cost efficiency

> MSR-V doesn't accelerate hardware — it prevents waste.

</details>

---

## License

Apache-2.0 (demo and documentation)  
Proprietary core logic is excluded.

---

<p align="center">
  <strong>MSR-V</strong> — Control reasoning depth, not tokens.<br>
  <a href="https://github.com/ChanKi-arch/msrv-public-demo">Public Demo</a> ·
  <a href="./docs/">Documentation</a> ·
  <a href="../../issues">Issues</a>
</p>
