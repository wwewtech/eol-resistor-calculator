---
name: eol-resistor-calculator
description: Size and verify end-of-line (EOL) resistors for intrusion alarm zones: single vs double EOL, panel-specific values, DEOL state tables, wire-resistance compensation, and placement testing. Use when wiring or troubleshooting hardwired alarm panels (DSC, Honeywell, Paradox and similar). Never advise bypassing supervision.
---

# EOL Resistor Calculator

Unsupervised alarm loops cannot tell a cut wire from a quiet zone. Size the supervision correctly: right value, right place, verified states.

## Scope

- Hardwired burglary zones: single-EOL and double-EOL (DEOL) configurations.
- Zone state tables: normal / alarm / short / tamper / open per wiring type.
- Out of scope: addressable/wireless zones, fire-verification logic, panel programming menus (vendor-specific).

## When NOT to use

- Addressable loops or wireless sensors — no EOL applies.
- As a substitute for the panel's installation manual — panel tables win over this skill on any conflict.

## Reference values (verify against the panel manual first)

| Configuration | Normal | Alarm | Tamper/short/open |
|---|---|---|---|
| Single EOL (e.g. 5.6k DSC) | ~5.6k | open (∞) | short (0): trouble |
| Double EOL (e.g. 2×2.2k) | ~4.4k | ~2.2k | 0: short; ∞: open/cut |
| SEOL range (DSC IQ Pro) | 1k–10k acceptable | — | UL verified at 5.6k |

Common values by vendor: DSC 5.6k, Honeywell/Ademco 2k/2.2k typical, Paradox varies — always confirm from the panel docs, never assume.

## Method

1. **Identify the panel's expected scheme.** Single, double, or no-EOL — from the installation manual, not memory. Record the exact expected values.
2. **Compute.** For DEOL: normal = R1+R2 in the loop path, alarm = one resistor, tamper/open/short per the vendor state table. Show the arithmetic, not just the answer.
3. **Compensate wire runs.** Long runs add series resistance (~0.02Ω/ft for 22AWG — negligible for kΩ EOLs, but verify on marginal panels with tight windows). Flag when run resistance exceeds 1% of the EOL value.
4. **Placement rule.** The resistor goes at the END of the loop (last device), never inside the panel — panel-side placement blinds supervision to the field wiring. This is the #1 field error; check it explicitly.
5. **Verify states.** Measure with a meter at the panel terminals: simulate normal (door closed), alarm (door open), short (jumper), open (disconnect). All four must read as the state table predicts before sign-off.
6. **Document.** Record per zone: scheme, resistor value(s), measured readings for all states, date. Future troubleshooting starts here.

## Safety rules

- Never recommend disabling supervision or swapping NO/NC logic to dodge a trouble condition — fix the wiring.
- Treat a zone that reads correctly but intermittently as a failing splice/terminal, not a panel problem: re-terminate first.
- Sources: panel installation manuals (e.g. DSC IQ Pro reference), UL 864 supervision requirements.
