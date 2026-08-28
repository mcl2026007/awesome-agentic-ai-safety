# Tools and Libraries

- **CRIU (Checkpoint/Restore in Userspace)**
  Purpose: A Linux utility that freezes a running process and saves its complete state to disk as a set of files, enabling later restoration from that exact point.
  Relevance: The foundational, general-purpose checkpoint/restore technology underlying much of the agent-sandbox rollback research discussed in Sections 4.3 and 5.6.
  Link: https://github.com/checkpoint-restore/criu

- **E2B**
  Purpose: An open-source, cloud-based sandboxing runtime with a full Linux OS and SDK, purpose-built for safely executing untrusted AI/LLM-agent code.
  Relevance: A practical example of the "sandboxing" preventive control described in Section 4.2 (Preventive, Reactive, and Recovery Controls).
  Link: https://github.com/e2b-dev/e2b

- **Safety-Gymnasium**
  Purpose: A standardized, scalable safe reinforcement learning (SafeRL) benchmark library providing constrained environments and cost-based APIs.
  Relevance: Supports the paper's discussion of safe exploration and constrained-policy research referenced in Sections 4.2 and 8.6 (Formal Verification of Recovery).
  Link: https://github.com/PKU-Alignment/safety-gymnasium

- **Arrakis**
  Purpose: A self-hosted microVM sandbox platform for AI agent code execution with built-in checkpoint-and-restore functionality.
  Relevance: Illustrates the technical feasibility of efficient agent-sandbox checkpointing discussed in Section 4.3, alongside DeltaBox and Crab.
  Link: https://github.com/abshkbh/arrakis

- **Kubernetes Agent Sandbox**
  Purpose: A Kubernetes-native controller providing pluggable, isolated sandbox environments (via gVisor/Kata) for running agent workloads at scale, including snapshot/restore support.
  Relevance: Demonstrates production-grade infrastructure for the "State Restoration Layer" architecture described in Section 5.6.
  Link: https://github.com/kubernetes-sigs/agent-sandbox
