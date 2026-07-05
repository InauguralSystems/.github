## Inaugural Systems

Creators of **EigenScript** — a zero-dependency C-implemented programming language with native observer semantics, training a model on its own code.

**Currently shipping · v0.26.0** — the 0.25/0.26 line made the freestanding and hosted runtimes agree byte-for-byte and cut a stdlib backlog drawn from the cross-repo pattern survey. The emblem case: `0xFF` had only ever parsed because glibc's `strtod` happens to accept hex, so the bare-metal OS lexed the same source as `0` plus an identifier `xFF` and every hex-using program broke on the metal; the fix made the lexer consume hex itself on every profile, made the `bit_*` builtins the same int64 two's-complement operation as the infix operators (a `(uint32_t)(int32_t)` conversion had been undefined behavior above 2^31, caught by a new CRC-32 module), and added an async abort seam so ctrl-c can break a runaway eval at the metal REPL. Seven new stdlib surfaces landed with it — CRC-32/Adler-32 checksums, civil-date math, packed BCD, bounded polling, hexdump, a twin-gate test harness, and named observer slots. Every change landed with the consumers: the same day v0.26.0 shipped, all ten downstream repos re-verified and moved to it, the self-hosting compiler re-proved its byte-exact bootstrap against the new oracle, and the bare-metal OS booted its full self-test ladder on the new runtime. The project ships an OpenSSF Best Practices passing badge, CodeQL, a 7.5/10 Scorecard, and Sigstore-signed binaries for Linux and macOS; the Game Boy ROM still runs past original-hardware speed.

[inauguralsystems.com](https://inauguralsystems.com) · [@inauguralsys on X](https://x.com/inauguralsys) · [contact@inauguralsystems.com](mailto:contact@inauguralsystems.com)

---

### Projects

A portfolio of repositories driving each other. The language adds a primitive; the consumers immediately use it; gaps exposed downstream become the next features upstream — every forcing-function consumer keeps a public ledger of the language gaps it forced.

- **EigenScript** — the language. Single C binary, bytecode VM, JIT, observer semantics, tensor math, LSP, formatter, embedded DB.
- **iLambdaAi** _(private)_ — self-training research system that trains a model on its own EigenScript source using observer semantics as the supervision signal.
- **Tidepool** — Spore-inspired cell-stage evolution game written entirely in EigenScript, with an in-language DQN reinforcement-learning trainer.
- **DMG** — Game Boy DMG emulator written in EigenScript as a deliberate worst-case workload for the language.
- **EigenMiniSat** — MiniSat-style CDCL SAT solver in EigenScript with Glucose-style LBD clause management, plus a repeatable benchmark suite over self-generated instance families and a vendored DIMACS corpus.

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
