# GitHub Implementations

- **google-deepmind/mona**
  What it implements: Official code for MONA (Myopic Optimization with Non-myopic Approval), reproducing the "Camera Dropbox" gridworld environment used to study long-horizon reward tampering and reward hacking.
  Relevance: Directly implements the reward-tampering mitigation method discussed in Section 6.2, complementary to the rollback framework proposed in this paper.
  Link: https://github.com/google-deepmind/mona

- **google-deepmind/ai-safety-gridworlds**
  What it implements: A suite of reinforcement learning gridworld environments (including safe interruptibility and side-effects tasks) used to empirically test AI safety properties.
  Relevance: Provides a concrete implementation of the safe-interruptibility concept discussed in Section 2.3 (Corrigibility and Shutdown), foundational to this paper's rollback architecture.
  Link: https://github.com/google-deepmind/ai-safety-gridworlds

- **checkpoint-restore/criu**
  What it implements: Checkpoint/Restore in Userspace (CRIU) — freezes a running Linux process and restores it later from a saved state, including memory, open files, and network connections.
  Relevance: The underlying OS-level mechanism that agent-sandbox checkpoint/restore systems (Section 4.3, 5.6) build on top of.
  Link: https://github.com/checkpoint-restore/criu

- **anthropics/sycophancy-to-subterfuge-paper**
  What it implements: The released environment definitions and code for the reward-tampering curriculum from Denison et al. (2024), including sample transcripts of models tampering with reward and unit tests.
  Relevance: Directly implements the experimental setup cited in Sections 1, 3.1, and 7.6 to discuss reward tampering as an adversarial risk to rollback controllers.
  Link: https://github.com/anthropics/sycophancy-to-subterfuge-paper

- **kubernetes-sigs/agent-sandbox**
  What it implements: A Kubernetes controller providing isolated, pluggable sandbox environments (gVisor/Kata) for agent workloads, with snapshot and restore support.
  Relevance: A production-oriented implementation of the "State Restoration Layer" architecture described in Section 5.6.
  Link: https://github.com/kubernetes-sigs/agent-sandbox
