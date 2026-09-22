# Changelog

All notable changes to the `eol-resistor-calculator` skill will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.0.0] - 2026-09-22

### Initial Release — Security Loop Supervision & EOL Calculation

#### Added
- **Master Skill (`SKILL.md`):** Complete electrical specification for SEOL, DEOL, and TEOL alarm loops.
- **Far-End Placement Axiom:** Strict prohibition against panel-terminal resistor stacking.
- **4-State DEOL Truth Table:** Full discrimination between Normal, Alarm, Short Tamper, and Open Tamper.
- **Copper Wire Drop Compensation:** Formulas and resistance ratings for 18, 20, 22, and 24 AWG conductors.
- **Panel Matrix:** Standards for DSC (5.6k), Honeywell (2.0k), Paradox (1.0k), Texecom (2.2k/4.7k), and Bosch (1.0k).
- **Interactive Laboratory (`docs/index.html`):** In-browser live loop and multimeter simulation tool.
- **CI Validation:** Automated YAML frontmatter and SHA256 file symmetry verification.
