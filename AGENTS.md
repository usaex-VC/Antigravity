# Antigravity Repository Agent Execution Contract

This repository adopts `USAEX-GLOBAL-ENGINEERING-EXECUTION-V1` from `usaex-VC/VOS` as the minimum engineering-execution floor for owner-controlled development. Repository rules may strengthen but must not weaken it.

## Engineering execution boundary

- ChatGPT performs all feasible architecture, code, deterministic repair, static audit, test design, repository/PR operations, exact-SHA freeze, evidence review, and merge orchestration directly.
- The owner's local Windows agent is `TESTS_ONLY`, reserved only for irreducibly local Windows runtime or corporate endpoint-security proof.
- Automatic hosted test/verification/acceptance CI is forbidden by default. Manual hosted diagnostics are non-authoritative only; automatic non-test jobs require an explicit reviewed whitelist.
- Detailed execution belongs in committed repo-relative MD files. A local job is invalid unless it uses the current canonical VOS handoff contract, including `FULL_SUITE`, bounded wall time, explicit parallelism, exact tested SHA in the result, commit+push evidence, and stop-on-first-deterministic-failure semantics.
- `NOT_RUN`, `SKIP`, `BLOCKED`, `UNKNOWN`, stale-head, malformed, dirty-worktree, or unpushed evidence is never PASS.

## Executable VOS pre-dispatch

A policy citation alone is not enforcement. Before any local test/qualification command, the approved central VOS consumer launcher MUST execute authoritative `agent-preflight` against the committed job MD using the separately qualified `engineering-v1` policy channel.

Proceed only when the launcher verifies its frozen body, exact approved Python runtime, clean product worktree, repository identity, immutable VOS runtime, stable `engineering-v1` resolution, and the child returns exactly `VOS_AGENT_PREFLIGHT=ALLOW_LOCAL_AGENT`.

Any bootstrap hash mismatch, Python mismatch, channel movement, repository mismatch, dirty worktree, parser failure, `CHATGPT_CONTINUE`, `REJECT_INEFFICIENT_TEST_PLAN`, `INFRA_BLOCKED`, or endpoint-security block forbids local execution. Direct test invocation that bypasses this preflight is non-authoritative and prohibited.

## Verification economy

- Use `FAST -> STAGE -> ACCEPTANCE`; full repository suites are not the default edit loop.
- `FULL_SUITE` must be committed in the handoff as `NOT_REQUESTED` or an allowed VOS-required basis before runtime may execute it.
- Stop at the first deterministic blocking failure. Reuse compatible evidence and do not rerun weaker checks already superseded by stronger proof.
- Parallelize independent work/verification where safe. Worker counts must be measured, not guessed.
- Runs over 900 seconds require concrete justification; runs over 1800 seconds require parallel/decomposed execution.

VOS governs engineering execution only; repository-specific product behavior and domain contracts remain authoritative within this repository unless explicitly superseded by a stronger local contract.
