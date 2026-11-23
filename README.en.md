# Design Skills · Software Interface Design

[中文](README.md) · [English](README.en.md)

Agent Skills for building, improving, and reviewing software interfaces and data visualizations. They can be used independently or together by tools that support Agent Skills.

## Skills

| Skill | Purpose | Status |
| --- | --- | --- |
| [visual-design · Visual Design](visual-design/SKILL.en.md) | Use the product's intended character and real content to shape composition, visual hierarchy, typography, and color. | Released in `v0.1.1` |
| [interaction-design · Interaction Design](interaction-design/SKILL.en.md) | Design and walk through task flows, control behavior, state feedback, and recovery. | Released in `v0.1.1` |
| [data-visualization · Data Visualization](data-visualization/SKILL.en.md) | Choose and review chart designs, checking that visual encodings match the meaning of the data. | Released in `v0.1.1` |

## Language

Chinese is the primary language for maintenance and validation. Each skill uses the Chinese `SKILL.md` as its entry point. The English translations are linked above for reference.

## Installation

Download the ZIP for the skill you want or use the source folder for that version.

| Skill | Archive | Versioned source |
| --- | --- | --- |
| `visual-design` | [Download ZIP](https://github.com/Ethan-decoy/design-skills/releases/download/v0.1.1/visual-design-v0.1.1.zip) | [v0.1.1](https://github.com/Ethan-decoy/design-skills/tree/v0.1.1/visual-design) |
| `interaction-design` | [Download ZIP](https://github.com/Ethan-decoy/design-skills/releases/download/v0.1.1/interaction-design-v0.1.1.zip) | [v0.1.1](https://github.com/Ethan-decoy/design-skills/tree/v0.1.1/interaction-design) |
| `data-visualization` | [Download ZIP](https://github.com/Ethan-decoy/design-skills/releases/download/v0.1.1/data-visualization-v0.1.1.zip) | [v0.1.1](https://github.com/Ethan-decoy/design-skills/tree/v0.1.1/data-visualization) |

After extracting the archive, import the entire skill folder into your tool or copy it into a skill directory that your tool scans. Keep `SKILL.md` directly inside the named skill folder. For tools that follow the `.agents/skills/` convention, use `~/.agents/skills/` for user scope or the project's `.agents/skills/` for project scope. Follow your tool's instructions for installing and enabling skills. [Agent Skills client guide](https://agentskills.io/client-implementation/adding-skills-support#where-to-scan)

Download checksums are listed in `SHA256SUMS.txt` on the release page. [v0.1.1 release](https://github.com/Ethan-decoy/design-skills/releases/tag/v0.1.1)

## Usage

Select a skill in your tool or specify its name in the request. Each line is a separate example.

```text
Use visual-design to improve the hierarchy of the photo review page so the photo, part number, and review status are easy to distinguish.
Use interaction-design to walk through recovery after a failed save and see how the user can continue.
Use data-visualization to review this monthly trend chart and check the scale, missing values, and growth against the original table.
```

### Automatic invocation

Tools that support automatic invocation can load skills by matching the request to their descriptions. A single review request can cover the interface, workflow, and chart together. [How Agent Skills are loaded](https://agentskills.io/home#how-do-agent-skills-work)

```text
Review this dashboard from an aesthetic and UI/UX perspective. What would you improve about the information hierarchy, filtering flow, and trend chart?
```

## Contents

Each skill uses `SKILL.md` as its entry point. The directory also includes an English translation and optional interface metadata. Visual Design is shown as an example.

```text
visual-design/
├── SKILL.md
├── SKILL.en.md
└── agents/
    └── openai.yaml
```

The research note uses a part photo review page to show how composition, typography, and color convey a product's character. [Visual design research note in Chinese](research/visual-design.md)

## Validation and feedback

Release checks cover skill format, alignment with the Chinese originals, and the individual archives and checksums. Walkthroughs of Chinese requests checked skill selection and deliverable choices. Local checks covered installation and user-level discovery. The project author reported good results after trying the skills in practice.

Share your use case, how the skill was invoked, and what happened. [File an issue](https://github.com/Ethan-decoy/design-skills/issues)
