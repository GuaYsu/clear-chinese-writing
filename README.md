# Clear Chinese Writing

A reusable ChatGPT / Agent Skill for writing and revising Chinese prose so it is clear, natural, idiomatic, and information-dense without falling into formulaic “AI style”.

## What this skill is for

This project is not a detector-avoidance tool and does not try to make text “look human” by adding noise, random variation, or stylistic quirks. Its goal is simpler: help models produce Chinese that is accurate, coherent, idiomatic, and appropriate to the genre.

The design combines four layers:

1. **Clear-expression principles inspired by ASD-STE100** — stable terminology, explicit logic, direct verbs, concrete scope, and low ambiguity.
2. **Chinese-native phrasing** — collocation, sentence shape, register, rhythm, and avoidance of semantic calques.
3. **Anti-formula checks** — guardrails against empty contrast, ceremonial transitions, forced significance, repetitive disclaimers, and other common model habits.
4. **Voice preservation** — keep the author’s register and rhythm without mechanically imitating fillers or mannerisms.

## Core principle

> Do not optimize for appearing human. Optimize for writing good Chinese.

A phrase should not be removed merely because it is common in AI output, and it should not be kept merely because a human might say it. The relevant question is whether it serves the meaning, logic, register, or rhythm of the text.

## Typical uses

- Lab reports and technical reports
- Academic and explanatory prose
- Chinese polishing and rewriting
- Long-form answers and educational explanations
- Editing text that is grammatically correct but still feels translated, stiff, or over-compressed

It is not meant to be applied blindly to creative writing, advertising copy, roleplay, literal translation, or highly stylized prose.

## Structure

```text
clear-chinese-writing/
├── SKILL.md
└── references/
    ├── examples.md
    ├── formal-report.md
    ├── native-collocation.md
    ├── natural-chinese.md
    ├── research-basis.md
    └── revision-checklist.md
```

`SKILL.md` contains the core workflow. Supporting files are loaded only when relevant; examples are deliberately separated from the default context to reduce style contamination.

## Design notes

A recurring problem with “humanizer” prompts is that they can replace one recognizable model style with another. This project therefore avoids blanket rules such as banning em dashes, forcing sentence-length variation, or forbidding specific phrases.

Instead, it asks the model to judge the function of a construction in context. For example, “不是……而是……” is fine when there is a real contrast. It becomes a problem when the model invents an alternative merely to reject it.

The same principle applies to Chinese naturalness. When a sentence is understandable but feels non-native, the skill prefers reconstructing the sentence from the intended meaning rather than performing word-for-word substitution.

## Status

This is an evolving project. The current version was iteratively refined through comparisons among technical-writing principles, Chinese linguistic research, model outputs, and human preference feedback.

Issues and examples of failure cases are especially welcome. Useful reports include:

- a sentence that became less natural after the skill was applied;
- a rule that works in one genre but fails in another;
- Mainland / Taiwan / Hong Kong / Singapore Chinese differences;
- cases where a supposedly “AI-like” construction is actually the best wording;
- new patterns of translation-like or model-like Chinese.

## Installation

The repository follows the Agent Skills format: the root skill directory contains `SKILL.md` plus optional supporting files. Import or upload the directory/ZIP in a product that supports Agent Skills.

Availability and invocation behavior depend on the host product and workspace configuration.

## License

MIT. See [LICENSE](LICENSE).
