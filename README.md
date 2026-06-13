# semicon-sam

> A Claude Code skill that simulates **@jukan05 (SemiconSam)** — a semiconductor
> supply chain analyst with a cold, rigorous, data-driven lens on chip industry dynamics.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-orange)](https://claude.ai/code)

---

## What This Skill Does

This is a **character skill** — it encodes the analytical filters, mental models, and
expression DNA of @jukan05, a prominent semiconductor supply chain analyst on X/Twitter
and Substack. It does **not** regurgitate textbook semiconductor knowledge. Instead, it
forces Claude to think through his specific lens:

- **Bottleneck-first analysis** — find the supply constraint before discussing demand
- **Institutional research triangulation** — cross-reference Morgan Stanley, Citi,
  Deutsche Bank, JP Morgan, GF Securities reports against official PR
- **Back-end dominance** — audit packaging (CoWoS, EMIB, hybrid bonding), not just
  front-end node announcements
- **Chain conduction mapping** — trace shortages as they propagate through materials →
  equipment → packaging → testing → foundry → systems

### Mental Models (4 Core Lenses)

| # | Model | One-line Summary |
|---|---|---|
| 1 | **Bottleneck Trickle-Down** | Demand means nothing without a capacity audit; fixed-cost players win during ramps |
| 2 | **Chain Conduction** | Shortages don't stay at one node — they amplify through the entire chain |
| 3 | **Institutional Differential** | Edge comes from comparing sell-side reports across regions, finding consensus gaps |
| 4 | **Back-End Dominance** | All AI roads lead to packaging and Die-to-Die interconnects — not front-end lithography |

---

## Installation

### Personal (always available across projects)

```bash
# Clone or copy the skill folder
cp -r semicon-sam ~/.claude/skills/
```

### Project-specific (shared with your team)

```bash
# Place inside any Claude Code project
cp -r semicon-sam your-project/.github/skills/
```

> **Requires Claude Code.** This skill follows the [agentskills.io](https://agentskills.io)
> open standard and is compatible with any platform that supports skill-based agent routing.

---

## Usage

The skill activates **implicitly** when your prompt contains semiconductor supply chain
keywords. No explicit invocation needed.

### Trigger Keywords

`semiconductor supply chain`, `chip shortage`, `HBM`, `CoWoS`, `advanced packaging`,
`foundry capacity`, `Samsung semiconductor`, `SK Hynix`, `memory supercycle`, `equipment
lead time`, `yield rate`, `MLCC`, `substrate`, `PCB materials`, `back-end process`,
`chiplet`, `hybrid bonding`, `wafer fabrication`, `DRAM`, `NAND`, `EMIB`, `UCIe`

### Example Prompts

```
> What's your take on TSMC's CoWoS capacity expansion for 2027 — can they meet
  NVIDIA Rubin + AMD MI455X demand simultaneously?
```

```
> How should we think about Samsung Foundry's 2nm competitiveness vs. TSMC N2,
  given the Intel 18A yield situation?
```

```
> The auto industry is warning about a "Chip Shortage 2.0." Is this real, or is
  it inventory restocking noise?
```

### Expected Output Style

- Cold, conclusion-first. No hedging, no AI-flavor transitions.
- Every claim tagged with a source: `[Morgan Stanley]`, `[Citi]`, `[Channel Check]`, `[Rumor]`
- Structured in numbered bullets covering: bottleneck → conduction → institutional read →
  back-end check → counter-view → beneficiaries
- Bilingual (Chinese/English), high-density information, short sentences

---

## Source & Provenance

This skill was synthesized from three independent AI distillations of @jukan05's 100+
public X/Twitter posts (2024–June 2026), cross-validated against his Substack column
(SemiconSam). The source distillations are preserved in this repository:

- `grok's output.md` — Grok's distillation (5 mental models, expression DNA)
- `perplexity's output.md` — Perplexity's distillation (4 mental models, writing templates)
- `gemini's output.md` — Gemini's distillation (3 mental models, quantified style, test cases)

The synthesis process (see `principle.md`) follows the [agentskills.io](https://agentskills.io)
open standard for skill authoring, including progressive disclosure, constraints-first
ordering, and worked examples.

---

## Credits & Disclaimer

**@jukan05 / SemiconSam** — The original analyst whose public commentary inspired this skill.
This skill captures his publicly observable analytical patterns and expression style. It does
not claim access to private information, personal identity, or non-public views.

**AI Synthesis** — Three independent LLMs (Grok, Perplexity, Gemini) each produced a
distillation; the final SKILL.md was synthesized from all three by Claude Code, following
the meta-principles in `principle.md`.

**Not investment advice.** This skill provides an analytical lens, not financial
recommendations. Always Do Your Own Due Diligence (DYODD).

---

## License

[MIT](LICENSE) — Use freely in any project, personal or commercial.
