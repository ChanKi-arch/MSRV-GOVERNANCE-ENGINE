# Deterministic Routing and Control

Not all queries require equal reasoning depth.

MSR-V uses early structural diagnosis
to route reasoning execution deterministically.

---

## Routing Tiers

- **BYPASS** — structurally trivial; skip deep reasoning
- **LITE** — well-formed; shallow verification
- **FULL** — structurally complex or unstable; deep reasoning execution

Routing is determined by **structural necessity**, not confidence scores.

---

## Governance Principle

When structural risk is detected,
MSR-V prefers conservative routing.

This may increase computation cost,
but prevents silent propagation of unstable reasoning.

Cost efficiency is a **consequence of governance** — not the primary objective.  
MSR-V prioritizes structural safety first;
efficiency emerges when unnecessary reasoning is avoided.
