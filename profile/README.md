## Inaugural Systems

Creators of **EigenScript** — a zero-dependency C-implemented programming language with native observer semantics, training a model on its own code.

**Currently shipping · v0.11.8** — a reversible runtime: a trace tape replays any run byte-for-byte, temporal interrogatives query prior state, and the graphical debugger steps backward in time. The bytecode VM's JIT compiles hot loops into native thunks, and the entire test suite runs leak-clean under AddressSanitizer in CI.

[inauguralsystems.com](https://inauguralsystems.com) · [@inauguralsys on X](https://x.com/inauguralsys) · [contact@inauguralsystems.com](mailto:contact@inauguralsystems.com)

---

### Projects

Five repositories driving each other. The language adds a primitive; the consumers immediately use it; gaps exposed downstream become the next features upstream.

- **EigenScript** — the language. Single C binary, bytecode VM, JIT, observer semantics, tensor math, LSP, formatter, embedded DB.
- **iLambdaAi** — self-training research system that trains a model on its own EigenScript source using observer semantics as the supervision signal.
- **Tidepool** — Spore-inspired cell-stage evolution game written entirely in EigenScript, with an in-language DQN reinforcement-learning trainer.
- **DMG** — Game Boy DMG emulator written in EigenScript as a deliberate worst-case workload for the language.
- **EigenMiniSat** — CDCL SAT solver in EigenScript, benchmarked against the MiniSat C++ reference and reaching into Glucose territory.

Supporting:

- **EigenGauntlet** — stress harness for root language/runtime gap discovery.

---

### Why the repos are private

Pre-1.0 work moves fastest when bugs can be fixed at the root instead of papered over for downstream users. Keeping the source private removes the obligation to preserve old behavior — every issue gets corrected where it actually lives, the API tightens, and the language gets cleaner with each version. When EigenScript is ready to support contracts that can be kept, it will go public.

---

### Vision

AI should be **dynamic**, not static.
Our systems operate on **invariants**, allowing code to feel its own stability and momentum.

---

### Founder

**Jonathon McReynolds** ([@InauguralPhysicist](https://github.com/InauguralPhysicist))
Army veteran · Cancer survivor · Self-taught physicist/engineer
