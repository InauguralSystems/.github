## Inaugural Systems

Creators of **EigenScript** — a zero-dependency C-implemented programming language with native observer semantics, training a model on its own code.

**Currently shipping · v0.17.0** — the 0.17 line re-architected the observer itself. A dynamical-systems lab kept reporting `equilibrium` on solvers plainly at rest, which traced to observer state living on the recyclable, reference-shared `Value` object — so a convergence iterate built through aliasing temporaries (the normal solver shape) never accumulated its own trajectory and `converged` never fired. Observer state is now keyed to the variable *binding*, numbers are pure immediates, and the entire value-path observer model was deleted, leaving exactly one representation; those convergence loops now converge. The path here ran through a public C embedding API and multi-interpreter runtime (0.15), windowed observer predicates with a leak-and-DoS hardening pass (0.16), and a self-hosting compiler that reproduces the whole toolchain byte-for-byte. The project ships an OpenSSF Best Practices passing badge, CodeQL, a 7.5/10 Scorecard, and Sigstore-signed binaries for Linux and macOS (Intel JIT live since 0.15.2); the Game Boy ROM still runs past original-hardware speed.

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

### Why EigenScript is open

Through pre-1.0 the source stayed private on purpose: bugs got fixed at the root instead of papered over for downstream users, with no obligation to preserve old behavior. Every issue was corrected where it actually lived, the API tightened, and the language got cleaner with each version. That season is now historical — EigenScript is **public**. Read the source, build it yourself, and run the same binary that serves the landing page.

---

### Vision

AI should be **dynamic**, not static.
Our systems operate on **invariants**, allowing code to feel its own stability and momentum.

---

### Founder

**Jonathon McReynolds** ([@InauguralPhysicist](https://github.com/InauguralPhysicist))
Army veteran · Cancer survivor · Self-taught physicist/engineer
