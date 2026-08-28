# Awesome Agentic AI Safety

A curated collection of research papers, datasets, tools, implementations, and
learning resources on safety, rollback, and recovery mechanisms for objective
misinterpretation in agentic AI systems. Built around an AI-assisted research
paper studying how autonomous agents can be safely interrupted, restored, and
revalidated after pursuing a misinterpreted objective.

## Contents

- [Overview](#overview)
- [AI-Assisted Research Paper](#ai-assisted-research-paper)
- [Citation Integrity Audit](#citation-integrity-audit)
- [Curated Research Papers](#curated-research-papers)
- [Datasets](#datasets)
- [Tools and Libraries](#tools-and-libraries)
- [GitHub Implementations](#github-implementations)
- [Tutorials and Learning Resources](#tutorials-and-learning-resources)
- [License](#license)

## Overview

Agentic AI systems combine large language models, planning, memory, tool use,
and autonomous multi-step decision-making. This introduces a distinctive
safety problem: an agent can remain highly competent while pursuing an
objective that differs from what its designer or user actually intended. This
phenomenon spans specification gaming, reward hacking, goal misgeneralization,
reward tampering, and inner misalignment.

Most conventional safeguards — reward-model improvement, human feedback,
monitoring, and shutdown mechanisms — try to prevent or detect this kind of
failure before or during execution. This repository centers on a
complementary approach: **rollback**, the controlled restoration of an
agent and its environment to a previously validated state once objective
misinterpretation is suspected.

The resources here are organized around a layered safety framework in which
objective uncertainty, runtime monitoring, action gating, checkpointing,
rollback, and post-rollback revalidation work together as mutually
reinforcing controls. Particular attention is given to the distinction
between *logical* rollback of agent state and *physical or external-world*
reversibility — and to recent research showing that naive restoration can
itself introduce new hazards, such as duplicated or resurrected external
actions ("semantic rollback attacks").

## AI-Assisted Research Paper

**Safety and Rollback Mechanisms for Objective Misinterpretation in Agentic AI Systems**

[View Paper](paper/AI_Assisted_Research_Paper.pdf)

This paper synthesizes the AI-safety and distributed-systems literature into
a seven-layer architecture for objective-aware rollback, distinguishes
recoverable from irreversible effects, and identifies open research gaps —
including objective-aware checkpointing, rollback benchmarks, semantic
idempotency, and formal verification of recovery.

## Citation Integrity Audit

All references cited in the paper and listed in this repository were checked
independently for correct title, authorship, publication year, venue, and a
working persistent identifier (arXiv ID, DOI, or conference record), rather
than accepted on the basis of AI-generated output alone.

[View Audit](citation-audit/Citation_Integrity_Audit.pdf)

## Curated Research Papers

See [`references/references.md`](references/references.md) for the full list
of 21 verified papers, organized into:
- Survey and Foundational Papers
- Goal Misgeneralization and Reward Hacking
- Corrigibility and Shutdown
- Reward Modeling, Approval, and Mitigation
- Checkpoint/Restore and Agent-Sandbox Systems

## Datasets

See [`datasets/datasets.md`](datasets/datasets.md) for benchmark environments
and curated failure-case collections relevant to this conceptual/architectural
research area.

## Tools and Libraries

See [`tools/tools.md`](tools/tools.md) for sandboxing, checkpoint/restore, and
safe-RL tooling referenced throughout the paper.

## GitHub Implementations

See [`implementations/github-repositories.md`](implementations/github-repositories.md)
for official code accompanying the key papers cited above.

## Tutorials and Learning Resources

- **[Reward Hacking in Reinforcement Learning](https://lilianweng.github.io/posts/2024-11-28-reward-hacking/)** — Lilian Weng
  A detailed, well-cited technical overview of reward hacking and goal misgeneralization, with concrete RL examples (CoinRun, Maze).

- **[AI Alignment Forum](https://www.alignmentforum.org/)**
  Community hub for technical AI alignment research, including primary discussion threads on corrigibility, interruptibility, and reward tampering.

- **[DeepMind Safety Research Blog](https://deepmindsafetyresearch.medium.com/)**
  Ongoing publications from Google DeepMind's safety team on specification gaming, safe interruptibility, and related topics.

- **[Anthropic Alignment Science Blog](https://alignment.anthropic.com/)**
  Research updates from Anthropic's alignment team, including work related to reward tampering and model behavior under training pressure.

- **[CS 285: Deep Reinforcement Learning (UC Berkeley)](https://rail.eecs.berkeley.edu/deeprlcourse/)**
  A full graduate-level course covering the RL foundations (MDPs, policy optimization) needed to understand goal misgeneralization and reward hacking papers.

## License

This repository's original content (README, audit, and curation) is licensed
under the [MIT License](LICENSE). Linked papers, datasets, and tools remain
the property of their respective authors and are subject to their own
licenses — see individual links for details.
