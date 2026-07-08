## Inaugural Systems

**Learning and innovating within constraints.**

A one-person systems lab building an entire software stack from first principles — a language with native observer semantics, and the AI, game, emulator, and SAT solver that stress-test it. Every line was built on a 2007 dual-core Pentium laptop; the constraint is the method, not a limitation.

[inauguralsystems.com](https://inauguralsystems.com) · [@inauguralsys on X](https://x.com/inauguralsys) · [contact@inauguralsystems.com](mailto:contact@inauguralsystems.com)

---

### What's built

The runtime, and the programs that push it hard enough to expose its next gap — each forcing-function consumer keeps a public ledger of the language gaps it drove upstream.

**The runtime**

- **EigenScript** — the language. A single zero-dependency C binary: bytecode VM, copy-and-patch JIT, native observer semantics, tensor math, a reversible trace tape, LSP, formatter, embedded DB.

**Built with it — the forcing functions**

- **Tidepool** — a Spore-inspired cell-stage evolution game with an in-language DQN reinforcement-learning trainer.
- **DMG** — a Game Boy emulator built as a deliberate worst-case workload; runs past original-hardware speed through the JIT.
- **EigenMiniSat** — a MiniSat-targeted CDCL SAT solver with Glucose-style LBD clause management and a repeatable benchmark suite.
- **dynamics** — an observer-rich dynamical-systems lab; the repo that forged the windowed convergence predicates.
- **EigenRegex** — a Pike-VM regex engine, linear-time, no backtracking.
- **liferaft** — a deterministic simulation tester for the Raft consensus protocol, replayed byte-for-byte under injected chaos.
- **tidelog** — CBOR serialization + a crash-recoverable store, byte-identical across hosted and bare-metal runs.
- **EigenGauntlet** — a stress harness for root language/runtime gap discovery.

**Research**

- **iLambdaAi** _(private)_ — a self-training research system that trains a model on its own EigenScript source, using observer semantics as the supervision signal.

The full release history lives in [the changelog on GitHub](https://github.com/InauguralSystems/EigenScript/releases).

---

### Approach

Built private through pre-1.0 so bugs got fixed at the root instead of papered over for downstream users — every issue corrected where it actually lived, the API tightened, the language cleaner with each version. That season is historical: EigenScript is now **public**. Read the source, build it yourself, and run the same binary that serves the landing page.

The method is a loop — point a demanding workload at the runtime, and it turns up a real bug in a signature feature, fixed at the root, upstream, with a regression test. The systems operate on **invariants**, so code can feel its own stability and momentum: measurement, not guesswork.

---

### Founder

**Inaugural Physicist** ([@InauguralPhysicist](https://github.com/InauguralPhysicist)) — Jonathon McReynolds.
Army veteran · cancer survivor · self-taught physicist and engineer.
