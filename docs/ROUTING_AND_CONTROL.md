# Deterministic Routing and Control

Not all queries require equal reasoning depth.

MSR-V performs **early structural diagnosis**
to deterministically decide **whether** reasoning should run
and **how deeply** it should be executed.

Routing decisions are made *before* costly inference occurs.

---

## Routing Tiers (v2.5.5)

- **MINI** — structurally stable and low risk  
  Minimal or local inference; reasoning execution may be skipped.

- **STANDARD** — well-formed but non-trivial  
  Shallow or budget-conscious reasoning execution.

- **PREMIUM** — structurally complex or unstable  
  Full, deep reasoning execution is required.

Routing is determined by **structural necessity**,  
not by confidence scores or probability estimates.

---

## Governance Principle

When structural risk is detected,
MSR-V deliberately favors **conservative routing**.

This may increase computational cost in individual cases,
but prevents the silent propagation of structurally unstable reasoning.

Cost efficiency is therefore a **byproduct of governance**,  
not its primary objective.

MSR-V prioritizes **structural safety first**;  
efficiency emerges naturally when unnecessary reasoning is avoided.
