## Inaugural Systems

Creators of **EigenScript** — a zero-dependency C-implemented programming language with native observer semantics, training a model on its own code.

**Currently shipping · v0.24.0** — the 0.24 line hunted silent tolerance out of the runtime. The emblem case: the Game Boy emulator's sprite priorities were quietly wrong because `sort` — a builtin the emulator itself had demanded — returned "equal" for anything non-numeric and silently sorted nothing; the fix wave that followed made sort raise, made parser limits fail loudly by name, made parentheses always mean one argument, gave modules a write boundary so a loaded library can never clobber its caller's variables, and replaced queue-mode audio with a 16-channel mixer. Every change landed with the consumers: the same day v0.24.0 shipped, all ten downstream repos re-verified and moved to it, the self-hosting compiler re-proved its byte-exact bootstrap against the new oracle, and the bare-metal OS booted its full self-test ladder on the new runtime. The project ships an OpenSSF Best Practices passing badge, CodeQL, a 7.5/10 Scorecard, and Sigstore-signed binaries for Linux and macOS; the Game Boy ROM still runs past original-hardware speed.

[inauguralsystems.com](https://inauguralsystems.com) · [@inauguralsys on X](https://x.com/inauguralsys) · [contact@inauguralsystems.com](mailto:contact@inauguralsystems.com)

---

### Projects

A portfolio of repositories driving each other. The language adds a primitive; the consumers immediately use it; gaps exposed downstream become the next features upstream — every consumer keeps a public ledger of the language gaps it forced.

- **EigenScript** — the language. Single C binary, bytecode VM, JIT, observer semantics, tensor math, LSP, formatter, embedded DB.
- **iLambdaAi** — self-training research system that trains a model on its own EigenScript source using observer semantics as the supervision signal.
- **Tidepool** — Spore-inspired cell-stage evolution game written entirely in EigenScript, with an in-language DQN reinforcement-learning trainer.
- **DMG** — Game Boy DMG emulator written in EigenScript as a deliberate worst-case workload for the language.
- **EigenMiniSat** — CDCL SAT solver in EigenScript, benchmarked against the MiniSat C++ reference and reaching into Glucose territory.

Supporting:

- **EigenGauntlet** — stress harness for root language/runtime gap discovery.
- **EigenRegex** — Pike-VM regex engine (linear-time guarantee, no backtracking) in pure EigenScript.
- **dynamics** — observer-rich dynamical-systems lab; the repo that forges the windowed convergence predicates.
- **tidelog** — CBOR serialization + a crash-recoverable KV store, byte-identical across hosted and bare-metal runs.

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
