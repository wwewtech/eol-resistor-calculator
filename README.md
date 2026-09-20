# eol-resistor-calculator

Size and verify end-of-line (EOL) resistors for intrusion alarm zones: single vs double EOL, panel-specific values, DEOL state tables, wire-resistance compensation, and placement testing.

## Why?
Unsupervised alarm loops cannot tell a cut wire from a quiet zone. Size the supervision correctly: right value, right place, verified states.

## Quick Installation

### 1. Via `skills.sh` / Vercel Skills CLI
```bash
npx skills add wwewtech/eol-resistor-calculator
```

### 2. Via Claude Code
```bash
claude skills add https://github.com/wwewtech/eol-resistor-calculator
```

### 3. For Google Antigravity
Clone or copy `SKILL.md` directly into your Antigravity skills directory:
```bash
# Windows
mkdir -p "$HOME\.gemini\config\skills\eol-resistor-calculator"
curl -sL https://raw.githubusercontent.com/wwewtech/eol-resistor-calculator/main/SKILL.md -o "$HOME\.gemini\config\skills\eol-resistor-calculator\SKILL.md"

# macOS / Linux
mkdir -p ~/.gemini/config/skills/eol-resistor-calculator
curl -sL https://raw.githubusercontent.com/wwewtech/eol-resistor-calculator/main/SKILL.md -o ~/.gemini/config/skills/eol-resistor-calculator/SKILL.md
```

### 4. For Cursor & Windsurf
Add `SKILL.md` to your workspace prompt context:
```bash
mkdir -p .cursor/skills/eol-resistor-calculator
curl -sL https://raw.githubusercontent.com/wwewtech/eol-resistor-calculator/main/SKILL.md -o .cursor/skills/eol-resistor-calculator/SKILL.md
```


## Links
- [Live Showcase](https://wwew.tech/skills/eol-resistor-calculator)
- [skills.sh](https://skills.sh)
- [SKILL.md](./SKILL.md)

## Core Concepts
- Hardwired burglary zones: single-EOL and double-EOL (DEOL) configurations.
- Compensate wire runs: Long runs add series resistance (~0.02Ω/ft for 22AWG).
- Placement rule: The resistor goes at the END of the loop (last device), never inside the panel.

## License
MIT © wwewtech
