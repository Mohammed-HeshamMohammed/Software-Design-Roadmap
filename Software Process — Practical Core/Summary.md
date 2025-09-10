# Software Process — Practical Core (Summary)

A lightweight, repeatable way to turn ideas into working software through short, testable increments.

## Scope
- Practical principles for process, quality, requirements, and reuse
- Minimal ceremony; optimized for clarity and speed

## Outcomes
By the end, you should be able to:
- Plan small, incremental deliveries with clear “Done”
- Build dependable systems and measure what matters
- Capture clear, testable requirements (functional + non-functional)
- Reuse components safely and effectively
- Run a tight plan→build→test→release feedback loop

---

## 1) Process Discipline (Plan the work; work the plan)

**Plan small**
- Define scope, constraints (time/cost), and a 2–6 week roadmap.

**Work in increments**
- Slice thin vertical features; ship frequently.

**Make risk visible**
- Keep a top-5 risk list; spike/prototype high-risk items early.

**Define Done**
- Code + tests pass + review + integrated + minimal docs.

**Control change**
- Accept change with explicit trade-offs; keep a simple change log.

**Useful artifacts**
- 1-page vision, feature backlog, milestones, acceptance criteria, risk list.

---

## 2) Dependability & Performance

**Qualities to design/test for**
- Availability (uptime, MTTR)
- Reliability (correct, predictable behavior)
- Security (least privilege, validated inputs, safe defaults)
- Efficiency/Performance (p95 latency, throughput, memory)
- Evolvability (clear boundaries, small modules, refactoring budget)

**Tactics**
- Defensive coding, fail-fast, idempotent ops, retries with backoff
- Timeouts, circuit breakers, caching where it helps, backpressure
- Monitoring and logs tied to user journeys

---

## 3) Requirements

**What “good” looks like**
- Clear & testable
- Valuable & feasible (fits the timebox)
- Independent & small (days, not months)
- Prioritized (MoSCoW) with reasons
- Traceable to goals with acceptance criteria

**Capture methods**
- User stories + acceptance criteria, simple use cases, quick prototypes, example data

**Don’t forget non-functional requirements**
- Latency, throughput, error rates, security, accessibility, observability,
  portability, maintainability

---

## 4) Reuse

**What to reuse**
- Libraries/frameworks, services/APIs, components/templates, prior code/docs

**Quick due-diligence**
- Fit, health (updates/issues/docs), license & security, cost of ownership (deps, lock-in)

**Benefits**
- Faster delivery, more testing/polish time, higher quality when fit is good

---

## Testing & Flow (Minimal Loop)

Plan → Implement → Review → Test (unit + a few high-value integration/acceptance) →  
Integrate → Release → Observe → Learn → Next slice

---

# Requirements — Gathering, Analysis, Prototyping, Use Cases (Summary)

## A) Gathering Methods
- Surveys, Interviews, Focus groups, Observations, Use case analysis

## B) Use Case Analysis — Writing Steps
1. Describe a real usage scenario  
2. Use the user’s viewpoint (no jargon/tech detail)  
3. List the steps and the intended result

## C) Requirements Analysis
- **Functional**: what the system does (features/functions)  
- **Non-functional**: qualities/properties (e.g., performance, security, usability)

## D) Prototyping
- Usually non-functional mock that shows layout and feature linkage/flow

## E) Interviews/Surveys → User Stories
- Simple, less-detailed requirement expressions

**Example user story**  
“As a sales staff member, I want to add new sales to the system so that I have a record of all transactions.”

---

## F) Example Use Case — Record Sale in the System

**Role**: Sales Staff

**Main Success Scenario**
1. Initiate “Add Sale”  
2. System requests item name and quantity  
3. User enters details and confirms  
4. System stores the new entry

**Extension E1 — Quantity < 1**
- **Condition**: quantity is < 1, blank, or non-numeric  
- **System**: display “Quantity must be a positive integer (≥ 1)”, highlight Quantity, keep Item Name, do not store  
- **Flow**: return to Step 2

**Preconditions**
- User is signed in as Sales Staff

**Postconditions**
- **Success**: entry stored  
- **Failure**: no change saved
