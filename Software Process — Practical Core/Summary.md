# Software Process — Practical Core — Overview

A lightweight, repeatable way to turn ideas into working software through short, testable increments.

## Scope
- Process patterns and minimal artifacts
- Core quality attributes (run-time + change-time)
- Requirements capture at a practical level
- Safe reuse of components and services
- A tight build–test–release feedback loop

## Audience and Prerequisites
- Audience: CS/CE students, junior developers, and teams adopting lightweight process
- Prerequisites: Basic programming, Git, and unit-testing familiarity

## Learning Outcomes
By the end, you should be able to:
- Plan small, incremental deliveries and define “Done”
- Design and measure for availability, reliability, security, efficiency, and evolvability
- Write clear, testable requirements (functional and non-functional)
- Evaluate and adopt third-party components safely
- Run a minimal loop: plan → build → test → release → observe → learn

## Syllabus Outline
1. **Process Discipline**  
   Plan small; work in increments; make risk visible; define “Done”; control change; minimal artifacts (vision, backlog, milestones, acceptance criteria, risk list).

2. **Dependability & Performance**  
   Qualities to design/test for: availability, reliability, security, efficiency, evolvability.  
   Supporting tactics: defensive coding, retries/backoff, timeouts/circuit breakers, caching/backpressure, monitoring tied to user journeys.

3. **Requirements (Quality Checklist)**  
   Clear & testable; valuable & feasible; independent & small; prioritized (MoSCoW); traceable to goals with acceptance criteria.

4. **Reuse (Don’t Reinvent the Wheel)**  
   What to reuse (libs/APIs/components/docs) and quick due-diligence: fit, health, license/security, cost of ownership.  
   Benefits: faster delivery, more testing/polish, higher quality when fit is good.

5. **Testing & Flow (Minimal Loop)**  
   Plan → Implement → Review → Test (unit + a few integration/acceptance) → Integrate → Release → Observe → Learn → Next slice.

### Requirements — Toolkit (Quick Addendum)
- **Gathering Methods:** surveys, interviews, focus groups, observations, use-case analysis.  
- **Use-Case Writing Steps:** real scenario → user viewpoint (no jargon) → ordered steps to result.  
- **Analysis:** functional vs. non-functional requirements.  
- **Prototyping:** quick, usually non-functional mock to show layout/flow.  
- **Artifacts:** simple user stories and a basic use-case template (role, main success steps, extensions, preconditions, postconditions).

## Materials
A printable summary is included as a PDF in this repository:  
- **[Download: Software Process — Practical Core (PDF)](./process_practical_core_overview.pdf)**
