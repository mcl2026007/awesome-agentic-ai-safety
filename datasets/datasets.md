# Datasets

Note: This research is architectural and conceptual rather than empirical, so
traditional ML datasets (image/text corpora) are not the primary resource type
for this topic. Instead, the closest equivalents are benchmark environments and
curated failure-case collections used in the AI-safety literature to study
objective misinterpretation, specification gaming, and reward hacking. These are
listed below.

- **AI Safety Gridworlds**
  Source: Google DeepMind
  Description: A suite of reinforcement learning gridworld environments designed to illustrate specific AI safety properties, including safe interruptibility, side effects, and reward gaming.
  Application: Used as a reference benchmark suite for evaluating specification gaming and safe-interruption behavior, directly relevant to Sections 3 and 4 of this paper.
  Link: https://github.com/google-deepmind/ai-safety-gridworlds

- **Objective Robustness Failures (Goal Misgeneralization environments)**
  Source: Langosco et al. (2022), "Goal Misgeneralization in Deep Reinforcement Learning"
  Description: Modified ProcGen Maze and CoinRun environments used to empirically demonstrate goal misgeneralization, where an agent's capabilities generalize but its goal does not.
  Application: Referenced in Section 2.1 and 3.1 to illustrate how objective misinterpretation manifests even when training rewards are correctly specified.
  Link: https://github.com/jbkjr/objective-robustness-failures

- **Sycophancy to Subterfuge: Reward-Tampering Curriculum**
  Source: Denison et al. (2024), Anthropic
  Description: A curriculum of increasingly gameable LLM-agent environments (political sycophancy through direct reward-tampering) with released environment definitions and sample transcripts.
  Application: Used in Sections 1 and 7.6 to discuss reward tampering and adversarial risks to rollback controllers.
  Link: https://github.com/anthropics/sycophancy-to-subterfuge-paper
