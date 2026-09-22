# Contributing to EOL Resistor Calculator

We welcome contributions from security technicians, electrical engineers, and hardware developers.

---

## Ways to Contribute

1. **Panel Presets:** Add detailed resistor threshold specifications and ADC acceptance windows for additional panel families (e.g., Inim, Risco, DMP, Satel).
2. **Triple-EOL & Anti-Masking Profiles:** Submit schematics for Grade 3 anti-masking detectors with separate fault and tamper reporting.
3. **Evals (`evals/evals.json`):** Contribute real-world troubleshooting scenarios and cable resistance edge cases.

---

## Submission Guidelines

- Ensure byte-for-byte SHA256 symmetry between `./SKILL.md` and `./skills/eol-resistor-calculator/SKILL.md`.
- Maintain single-file self-containment in `SKILL.md`.
- Validate before opening a PR:
  ```bash
  python -c "import hashlib; assert hashlib.sha256(open('SKILL.md','rb').read()).hexdigest() == hashlib.sha256(open('skills/eol-resistor-calculator/SKILL.md','rb').read()).hexdigest(), 'Hash mismatch!'"
  ```
