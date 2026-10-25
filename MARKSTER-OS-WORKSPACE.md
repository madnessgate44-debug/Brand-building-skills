# Markster OS Workspace

## Purpose

Use the existing open-source Markster OS as the source operating system for sales and marketing work. Do not recreate its playbooks or specialist skills unless an evidence-based gap requires it.

- Upstream: https://github.com/markster/markster-os
- Upstream license: MIT for skills, playbooks, templates, and research prompts. Preserve the upstream LICENSE and trademark notice.
- Upstream integration: Git submodule at `vendor/markster-os`.
- This repository remains the owner-controlled workspace and integration layer.

## Important runtime limitation

The upstream system is designed around a local CLI and a workspace directory. A Git submodule makes the upstream files addressable from this repository, but does not install the CLI or make local slash commands automatically available inside ChatGPT.

When working through GitHub tools, treat the files in `vendor/markster-os` as the playbook source and execute workflows directly from their documented instructions where tools permit. Never claim the CLI, hooks, or local runtime are installed unless execution evidence confirms it.

## Required execution lifecycle

1. INSPECT: read the relevant upstream instructions and the current company context.
2. SPECIFY: identify the business goal, deliverable, acceptance criteria, constraints, and evidence.
3. PLAN: select the existing Markster OS playbook or skill that matches the task.
4. EXECUTE: work from the playbook, using connected tools where available.
5. VERIFY: compare the output with the acceptance criteria and cite evidence.
6. CLOSE: report files changed, links, validation actually run, blockers, and next action.

Never fabricate market facts, customer evidence, sales results, test outcomes, or completed actions. Separate VERIFIED, USER INPUT, ASSUMPTION, CALCULATED, and UNKNOWN.

## First-run checklist

- [ ] Initialize the upstream submodule: `git submodule update --init --recursive`.
- [ ] Read `vendor/markster-os/README.md`, `QUICKSTART.md`, `AUTOPILOT.md`, `LICENSE`, and `skills/README.md`.
- [ ] Inspect the relevant company segment under `vendor/markster-os/playbooks/segments/`.
- [ ] Populate the workspace company-context files below using only known evidence.
- [ ] Run the upstream validator only in an environment where the CLI is actually available; record exact output.
- [ ] Choose the first playbook based on the readiness assessment, not guesswork.

## Canonical company context

The workspace company context must be stored in this repository, not upstream. Keep unreviewed raw notes separate from approved business facts.

Current company name: UNKNOWN  
Business model: UNKNOWN  
Primary market/geography: UNKNOWN  
Ideal customer profile: UNKNOWN  
Core offer and price: UNKNOWN  
Proof/case studies: UNKNOWN  
Sales channels: UNKNOWN  
Marketing channels: UNKNOWN  
Revenue target: UNKNOWN  
Delivery capacity and constraints: UNKNOWN  

Do not fill unknown fields with invented information. If prior user-provided context is available in the active conversation or retrievable history, cite it in the context file as user input.

## Decision policy

Prefer reusing upstream playbooks over creating new skills. Add local extensions only when a documented gap exists. Keep upstream material attributable and avoid presenting the ScaleOS methodology as original work. Any external outreach, publishing, spending, account changes, or other consequential action requires appropriate user authorization.

## Current status

- [x] Upstream repository selected after README and QUICKSTART inspection.
- [x] Upstream MIT license and trademark notice inspected.
- [x] Integration pointer and operating guide committed to branch.
- [ ] Pull request reviewed and merged.
- [ ] Submodule initialized and files verified in a runtime capable of recursive checkout.
- [ ] Company context completed from verified facts.
- [ ] End-to-end workflow executed and validated.
