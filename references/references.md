# References

All papers below are drawn from and verified against the reference list of the
author's own AI-assisted research paper, "Safety and Rollback Mechanisms for
Objective Misinterpretation in Agentic AI Systems." Each has been checked for
correct title, authors, year, and a working persistent identifier (arXiv ID,
DOI, or conference record).

## Survey and Foundational Papers

- **Concrete Problems in AI Safety**
  Amodei, D., Olah, C., Steinhardt, J., Christiano, P., Schulman, J., & Mané, D. (2016)
  [arXiv:1606.06565](https://arxiv.org/abs/1606.06565)
  Foundational paper identifying reward hacking, side effects, and safe exploration as core AI safety problems; establishes the vocabulary used throughout this research.

- **Specification gaming: the flip side of AI ingenuity**
  Krakovna, V., Uesato, J., Mikulik, V., Rahtz, M., Everitt, T., Kumar, R., Kenton, Z., Leike, J., & Legg, S. (2020)
  [DeepMind Blog / Research](https://deepmind.google/blog/specification-gaming-the-flip-side-of-ai-ingenuity/)
  A curated catalogue of ~60 real specification gaming incidents; used to motivate the taxonomy of failure in Section 3.1.

- **Risks from Learned Optimization in Advanced Machine Learning Systems**
  Hubinger, E., van Merwijk, C., Mikulik, V., Skalse, J., & Garrabrant, S. (2019)
  [arXiv:1906.01820](https://arxiv.org/abs/1906.01820)
  Introduces mesa-optimization, explaining how a learned model can itself become an optimizer with a divergent objective.

## Goal Misgeneralization and Reward Hacking

- **Goal Misgeneralization in Deep Reinforcement Learning**
  Di Langosco, L. L., Koch, J., Sharkey, L. D., Pfau, J., & Krueger, D. (2022)
  [PMLR 162, ICML 2022](https://proceedings.mlr.press/v162/langosco22a.html) / [arXiv:2105.14111](https://arxiv.org/abs/2105.14111)
  Empirically demonstrates that agents can retain capability while pursuing an unintended goal after distribution shift; central to this paper's Section 2.1.

- **Defining and Characterizing Reward Gaming**
  Skalse, J. M. V., Howe, N. H., Krakovna, V., & Krueger, D. (2022)
  [NeurIPS 2022, OpenReview](https://openreview.net/forum?id=yb3HOXO3lX2)
  Formalizes reward hacking via proxy vs. true reward and proves strong "unhackability" is difficult to achieve for broad policy classes.

- **Sycophancy to Subterfuge: Investigating Reward-Tampering in Large Language Models**
  Denison, C., MacDiarmid, M., Barez, F., Duvenaud, D., Kravec, S., Marks, S., Schiefer, N., Soklaski, R., Tamkin, A., Kaplan, J., Shlegeris, B., Bowman, S. R., Perez, E., & Hubinger, E. (2024)
  [arXiv:2406.10162](https://arxiv.org/abs/2406.10162)
  Shows LLMs trained on a curriculum of gameable environments can generalize to directly tampering with their own reward mechanism.

- **Reward Hacking in Language Model Agents: Revisiting AI Safety Gridworlds**
  Çağatan, Ö. V., & Zhao, X. (2026)
  [arXiv:2606.15385](https://arxiv.org/abs/2606.15385)
  Adapts AI Safety Gridworlds into a text-based suite, showing specification gaming emerges zero-shot in LLM agents.

## Corrigibility and Shutdown

- **Corrigibility**
  Soares, N., Fallenstein, B., Yudkowsky, E., & Armstrong, S. (2015)
  MIRI / Future of Humanity Institute Technical Report
  Defines a corrigible system as one that cooperates with corrective intervention rather than resisting shutdown or modification.

- **Safely Interruptible Agents**
  Orseau, L., & Armstrong, S. (2016)
  [UAI 2016 Proceedings](https://dl.acm.org/doi/10.5555/3020948.3021006)
  Proves RL agents can be formally designed to be safely interruptible without learning to avoid interruption.

- **The Off-Switch Game**
  Hadfield-Menell, D., Dragan, A., Abbeel, P., & Russell, S. (2017)
  DOI: [10.24963/IJCAI.2017/32](https://doi.org/10.24963/IJCAI.2017/32)
  Shows a rational agent with uncertainty about its own objective has an incentive to preserve, not disable, an off-switch.

- **The Shutdown Problem: An AI Engineering Puzzle for Decision Theorists**
  Thornley, E. (2024)
  [arXiv:2403.04471](https://arxiv.org/abs/2403.04471)
  Formalizes the tension between competent goal-pursuit and reliable shutdown compliance.

- **Optimal Policies Tend to Seek Power**
  Turner, A. M., Smith, L., Shah, R., Critch, A., & Tadepalli, P. (2021)
  [arXiv:1912.01683](https://arxiv.org/abs/1912.01683)
  Formal results showing optimal policies in broad MDP classes have incentives to preserve control over their environment.

## Reward Modeling, Approval, and Mitigation

- **Learning Human Objectives by Evaluating Hypothetical Behavior (ReQueST)**
  Reddy, S., Dragan, A. D., Levine, S., Legg, S., & Leike, J. (2019)
  [arXiv:1912.05652](https://arxiv.org/abs/1912.05652)
  Proposes learning reward models from evaluated hypothetical trajectories rather than exposing agents to unsafe states directly.

- **MONA: Myopic Optimization with Non-myopic Approval Can Mitigate Multi-step Reward Hacking**
  Farquhar, S., Varma, V., Lindner, D., Elson, D., Biddulph, C., Goodfellow, I., & Shah, R. (2025)
  [arXiv:2501.13011](https://arxiv.org/abs/2501.13011) / [PMLR 267](https://proceedings.mlr.press/v267/farquhar25a.html)
  Combines short-horizon optimization with longer-horizon approval to reduce multi-step reward hacking without needing to detect it.

## Checkpoint/Restore and Agent-Sandbox Systems

- **DeltaBox: Scaling Stateful AI Agents with Millisecond-Level Sandbox Checkpoint/Rollback**
  Dong, Y., He, J., Hou, Y., Du, D., Xu, Z., Yu, S., Xia, Y., & Chen, H. (2026)
  [arXiv:2605.22781](https://arxiv.org/abs/2605.22781), DOI: 10.48550/arXiv.2605.22781
  Introduces change-based, incremental checkpoint/restore achieving millisecond-scale rollback for agent sandboxes.

- **Crab: A Semantics-Aware Checkpoint/Restore Runtime for Agent Sandboxes**
  Wu, T., Chang, C., Cao, L., Gao, W., & Wang, W. (2026)
  [arXiv:2604.28138](https://arxiv.org/abs/2604.28138), DOI: 10.48550/arXiv.2604.28138
  Identifies the "agent-OS semantic gap" and shows chat-only recovery misses most OS-level effects relevant to safe rollback.

- **ACRFence: Preventing Semantic Rollback Attacks in Agent Checkpoint-Restore**
  Zheng, Y., Yang, Y., Zhang, W., & Quinn, A. (2026)
  [arXiv:2603.20625](https://arxiv.org/abs/2603.20625), DOI: 10.48550/arXiv.2603.20625
  Identifies "semantic rollback attacks" (Action Replay, Authority Resurrection) where restoring an LLM agent causes duplicated or resurrected external effects.

## Implementations Directly Cited

- **google-deepmind/mona** — Official MONA implementation
  [github.com/google-deepmind/mona](https://github.com/google-deepmind/mona)
  Code accompanying Farquhar et al. (2025), above.

- **google-deepmind/ai-safety-gridworlds** — AI Safety Gridworlds suite
  [github.com/google-deepmind/ai-safety-gridworlds](https://github.com/google-deepmind/ai-safety-gridworlds)
  Reference RL safety benchmark environments cited across Sections 2.3 and 6.4.

- **anthropics/sycophancy-to-subterfuge-paper** — Reward-tampering curriculum
  [github.com/anthropics/sycophancy-to-subterfuge-paper](https://github.com/anthropics/sycophancy-to-subterfuge-paper)
  Code and sample transcripts accompanying Denison et al. (2024), above.

- **checkpoint-restore/criu** — CRIU
  [github.com/checkpoint-restore/criu](https://github.com/checkpoint-restore/criu)
  The OS-level checkpoint/restore utility underlying DeltaBox and Crab.
