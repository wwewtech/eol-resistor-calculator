# EOL Resistor Calculator — Global Launch & Distribution Kit

This kit contains high-engagement announcement templates to publish and distribute `eol-resistor-calculator` across physical security, hardware hacking, and embedded engineering communities.

---

## 1. Twitter / X Viral Launch Thread

### Post 1 (Hook + Banner):
> Low-voltage installers know the nightmare of retrofitting an alarm panel:
>
> 8 zones wired behind drywall, unknown resistor values, and constant "Zone 4 Tamper / Line Fault" alerts.
>
> We just open-sourced **EOL Resistor Calculator**: an autonomous agent skill for security alarm loop balancing 🧵👇
>
> `npx skills add wwewtech/eol-resistor-calculator`
> [Attach: assets/eol-banner.svg]

### Post 2 (The Supervision Math):
> Simple Single-EOL only tells you if a wire was cut.
>
> Double-EOL (DEOL) differentiates Normal, Alarm, Tamper Open, and Tamper Short on just two wires.
>
> Triple-EOL (TEOL) adds Anti-Masking detection.
>
> This skill computes:
> - The exact equivalent resistance $R_{eq}$ for every state
> - The ADC voltage thresholds given any $V_{cc}$ and pullup $R_{pullup}$
> - Noise tolerance margins ($V_{margin} \ge 0.35V$) to prevent false alarms

### Post 3 (Panel Presets Built-in):
> Includes manufacturer presets:
> • Honeywell / Ademco Vista: 2.0 kΩ
> • DSC PowerSeries / Neo: 5.6 kΩ
> • Texecom Premier: 4.7 kΩ / 2.2 kΩ
> • Bosch Security: 1.0 kΩ
> • Custom arbitrary resistor pair solver

### Post 4 (Install & Run):
> 📦 skills.sh: https://skills.sh/wwewtech/eol-resistor-calculator
> ⭐ GitHub: https://github.com/wwewtech/eol-resistor-calculator
> 🌐 Web Visualizer: https://wwewtech.github.io/eol-resistor-calculator/

---

## 2. Reddit (`r/homedefense`, `r/AskElectronics`, `r/embedded`, `r/ClaudeAI`)

### Title:
> **An open-source agent skill for calculating security alarm loop resistors (EOL, DEOL, TEOL) and ADC voltage thresholds**

### Body:
> Hey everyone,
>
> Balancing alarm zone loops with End-of-Line resistors is easy on paper, but in real installations with long wire runs, differing panel ADC references, and sensor tamper contacts, false tamper triggers are rampant.
>
> We built **EOL Resistor Calculator** (https://github.com/wwewtech/eol-resistor-calculator), an agent skill (`SKILL.md`) that guides agents in:
> - Solving Single EOL, Double EOL (DEOL), and Triple EOL (TEOL) resistor topologies
> - Computing ADC voltage windows across all zone states (Normal, Alarm, Tamper, Fault, Mask)
> - Validating noise margins against sensor loop wire resistance
> - Generating wiring diagrams and test verification procedures
>
> **Install:**
> ```bash
> npx skills add wwewtech/eol-resistor-calculator
> ```
>
> GitHub: https://github.com/wwewtech/eol-resistor-calculator
> Web Demo: https://wwewtech.github.io/eol-resistor-calculator/

---

## 3. Pull Request Submission Template

```markdown
## Summary
Adds the `eol-resistor-calculator` skill to `skills/eol-resistor-calculator/SKILL.md`.

### Overview
`eol-resistor-calculator` provides autonomous coding agents with deterministic circuit mathematics for security alarm panel zone loops, calculating End-of-Line (EOL), Double EOL (DEOL), and Triple EOL (TEOL) supervision resistor values and voltage thresholds.

### Features
- State resistance matrices for Normal, Alarm, Tamper, and Fault
- ADC voltage divider window calculation with noise margin verification
- Loop wire resistance compensation (AWG 18-24)
- Built-in presets for Honeywell, DSC, Texecom, and Bosch panels

### Validation
Passes all CI checks with 0 errors and 0 warnings. Verified against canonical hardware loop evals.
```
