# Reasoning Skills
I'm experimenting with co-reasoning between humans and LLMs. The goal: use LLMs to achieve real-life goals faster, with fewer errors, and with higher probability of getting what you actually want.

One way to do this is through **reasoning skills,** structured protocols that force specific cognitive operations during mapping, decision-making, and strategy design.

## Why frameworks
Most people prompt LLMs with open-ended questions and get open-ended answers. Thinking and decision-making frameworks constrain how the LLM thinks. Instead of "analyze this situation," a framework says: "look at this from _here_, with _these_ constraints, and produce _this_ shape of output." 

The constraint is what makes the output non-generic. It forces the LLM into a specific cognitive operation (comparing along precise dimensions, stress-testing from an adversarial position, mapping what's unknown before acting) instead of producing plausible-sounding general analysis.

Frameworks also make co-reasoning _auditable_. You can see what lens was applied, what was prioritized, what was left out, and where the reasoning might break. That's harder to do with freeform conversation.

## What's in here
This repository includes two types of skills:

**Rebuilt existing frameworks.** Known thinking and decision-making tools: 2x2 matrices, weighted decision models, systems mapping, second-order effects analysis, stakeholder mapping, issue trees, pre-mortem, and others, rebuilt from the ground up as structured LLM skills. 

**Original co-reasoning protocols.** New frameworks designed specifically for human-LLM collaboration, like mapping what you don't know you don't know, or stress-testing a strategy through multiple independent cognitive lenses before synthesis.

## How these skills are built
Three principles separate these skills from most of what's out there.

**1. Framework depth over framework labels.**

Most LLM skills describe a framework at the surface level. "Run a second-order effects analysis by asking 'And then what?'" That's like telling an LLM "Imagine you're a copywriter," when in reality, there's enormous variation in how good copywriters actually work, what they pay attention to, and what distinguishes strong work from average work. A one-line or superficial instruction produces generic thinking.

These skills are built by getting obsessed with what makes a framework actually work: the fundamental principles, the common failure modes, what to pay attention to, what a strong output looks like versus a weak one, and where the framework breaks down. The skill encodes all of that.

**2. Cognitive functions over flat instructions.**

Instead of describing a framework as a sequence of steps, these skills assign distinct cognitive roles to different phases of the analysis. Each role approaches the problem from a specific, irreducible angle, and they operate independently before synthesis.

For example, the 2x2 Matrix skill includes two cognitive functions: the **Axis Creator,** which designs axis pairs that generate the most meaningful spread across four quadrants, and the **Differentiation Challenger**, which eliminates obvious axis pairs and tests whether they create useful tension or just tidy structure. The two functions work in sequence, and both must sign off before the matrix is finalized.

This matters because LLMs tend toward premature convergence. Cognitive functions force the model to hold multiple lenses open before collapsing into a single answer.

**3. Clarifying questions before execution.**

Each cognitive function is required to surface what it doesn't know before it starts working. Instead of letting the LLM fill gaps with assumptions, the skill forces each function to ask the clarifying questions it needs, independently, before generating any output. This means the human stays in the loop on the inputs, not just the outputs. The LLM doesn't get to silently decide what the problem is.

## Current skills
The list is growing.

| Skill      | Type              | What it does                                                                                                                                                                                        |
| ---------- | ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2x2 matrix | Rebuilt framework | Designs strong 2x2 matrices by treating axis selection as the core analytical act, not quadrant filling. Produces two materially different matrix options and compares what each reveals and hides. |

## How to use
Copy the skill folder you want into your project's skills directory. Each skill is self-contained: just the folder and its SKILL.md. Works with Claude Code, Cursor, Windsurf, Cline, GitHub Copilot, and any agent that supports the open Agent Skills standard.

## About
Built by [Victoria Rudi](https://victoriarudi.xyz/). This is a growing repository. More skills are in progress.

## License
MIT
