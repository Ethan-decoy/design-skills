# Design Skills · Software Interface Design

[中文](README.md) · [English](README.en.md)

Codex skills for building, improving, and reviewing software interfaces and data visualizations. Use them independently or together on tasks such as designing a dashboard or workbench.

## Skills

| Skill | Purpose | Status |
| --- | --- | --- |
| [visual-design · Visual Design](visual-design/SKILL.en.md) | Use the product's intended character and real content to shape composition, visual hierarchy, typography, and color. | Released in `v0.1.0` |
| [interaction-design · Interaction Design](interaction-design/SKILL.en.md) | Design and walk through task flows, control behavior, state feedback, and recovery. | Released in `v0.1.0` |
| [data-visualization · Data Visualization](data-visualization/SKILL.en.md) | Choose and review chart designs, checking that visual encodings match the meaning of the data. | Released in `v0.1.0` |

## Language

Chinese is the primary language for maintenance and validation. Each skill uses the Chinese `SKILL.md` as its installed entry point and provides interface text in Chinese. The English translations linked above are for readers who want to understand the instructions in English.

## Installation

### Install with Codex

Send the corresponding line to Codex for each skill you want to install.

```text
$skill-installer install https://github.com/Ethan-decoy/design-skills/tree/v0.1.0/visual-design
$skill-installer install https://github.com/Ethan-decoy/design-skills/tree/v0.1.0/interaction-design
$skill-installer install https://github.com/Ethan-decoy/design-skills/tree/v0.1.0/data-visualization
```

The links are pinned to `v0.1.0`. To install from the main branch, replace `v0.1.0` with `main` in the URL. When updating an installed skill, explicitly ask to replace the existing installation with the same name.

### Install manually

Download the ZIP for the skill you want. Extract it and copy the entire skill folder into your user directory at `~/.agents/skills/` or the target project's `.agents/skills/`. Each archive contains the Chinese entry point, its English translation, and the interface metadata. Checksums are available in `SHA256SUMS.txt` on the release page. [v0.1.0 release](https://github.com/Ethan-decoy/design-skills/releases/tag/v0.1.0) · [Codex skill locations](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills)

## Usage

Include the skill name to invoke it explicitly. Each line is a separate example.

```text
Use $visual-design to improve the hierarchy of the photo review page so the photo, part number, and review status are easy to distinguish.
Use $interaction-design to walk through recovery after a failed save and see how the user can continue.
Use $data-visualization to review this monthly trend chart and check the scale, missing values, and growth against the original table.
```

### Automatic invocation

All three skills allow automatic invocation. Codex can select relevant skills by matching the request to their descriptions. A single review request can cover the interface, workflow, and chart together. [How Codex uses skills](https://learn.chatgpt.com/docs/build-skills#how-chatgpt-and-codex-use-skills)

```text
Review this dashboard from an aesthetic and UI/UX perspective. What would you improve about the information hierarchy, filtering flow, and trend chart?
```

## Contents

The skills share the same directory layout. Visual Design is shown as an example.

```text
visual-design/
├── SKILL.md
├── SKILL.en.md
└── agents/
    └── openai.yaml
```

The research note uses a part photo review page to show how composition, typography, and color convey a product's character. [Visual design research note in Chinese](research/visual-design.md)

## Validation and feedback

`v0.1.0` is the first release. Release checks cover skill format, alignment with the Chinese originals, and the individual archives and checksums. Walkthroughs of Chinese requests checked skill selection and deliverable choices. A local Codex check confirmed user-level discovery. The project author reported good results after trying the skills in practice.

Share your use case, how the skill was invoked, and what happened. [File an issue](https://github.com/Ethan-decoy/design-skills/issues)
