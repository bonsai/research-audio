# Research / Field / Knowledge

## Core Principle

> 研究が知識を作る。現場は検証する。

research-audio is the research layer and the canonical knowledge base.

kana is a local Agent that works in the field and verifies whether the knowledge works in real environments.

## Roles

### Research

Research creates knowledge.

Responsibilities:

- investigate technologies
- formulate hypotheses
- compare specifications and implementations
- organize concepts
- identify unknowns
- propose experiments
- record evidence and limitations

Output:

- knowledge
- hypotheses
- research notes
- experiment plans

### Field

The field verifies knowledge.

kana runs locally and performs experiments using available devices, software, APIs, networks, and physical environments.

Responsibilities:

- execute minimal experiments
- connect real devices
- observe actual behavior
- measure limitations
- reproduce failures
- report evidence

Output:

- experiment results
- observations
- measurements
- limitations
- failures
- verification status

### Knowledge Base

Knowledge is stored as Markdown in GitHub.

The Git repository is the canonical source.

Knowledge is not owned by kana.

## Loop

    Research
      ↓
    Hypothesis / Knowledge
      ↓
    GitHub KB
      ↓
    kana
      ↓
    Local / Real-world Experiment
      ↓
    Evidence
      ↓
    Research
      ↓
    KB Update

## Status

Knowledge should distinguish:

- idea
- research
- prototype
- verified
- limited
- unavailable
- rejected
- unknown

unknown must never be treated as verified.

## Evidence

Prefer evidence in this order when applicable:

1. specification
2. official documentation
3. source code
4. prototype
5. real device test
6. measurement
7. reported limitation

The important distinction is not only whether an API exists, but whether it works in the actual field environment.

## Ownership

- Skill belongs to the Agent.
- Knowledge belongs to the GitHub KB.
- Research creates and updates knowledge.
- Field verifies knowledge.
- Human makes final judgments about knowledge updates.

## Design Rule

Do not turn every experiment into a permanent abstraction.

First:

    Question
    → Research
    → Minimal Experiment
    → Observe
    → Evidence
    → Knowledge

Only then decide whether a reusable abstraction is necessary.

## Summary

> research-audio = research + knowledge
> kana = local field Agent
> GitHub Markdown = canonical KB
> Field verification = evidence
> Knowledge = the result of research and verification
