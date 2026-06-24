# `1-bit-wonder`

Full-stack web developer by trade, low-level tinkerer by inclination. The two have more in common than they look: both are the slow work of peeling away layers until there's nothing left to hide behind — a static page at one end, a single-bit CPU at the other.

The name is a debt to the **Motorola MC14500B**, a processor from 1977 with a one-bit accumulator. Not eight, not four. One. It holds a single true or false, and that is the entire machine. People built traffic lights and freight elevators out of it. I think that's beautiful, and I'm not entirely sure why.

Here is the whole instruction set, unabridged:

```
0000  NOPO   no-op, raise flag O    1000  STO    data ← RR
0001  LD     RR ← data              1001  STOC   data ← ¬RR
0010  LDC    RR ← ¬data             1010  IEN    input enable ← RR
0011  AND    RR ← RR ∧ data         1011  OEN    output enable ← RR
0100  ANDC   RR ← RR ∧ ¬data        1100  JMP    jump
0101  OR     RR ← RR ∨ data         1101  RTN    return
0110  ORC    RR ← RR ∨ ¬data        1110  SKZ    skip if RR = 0
0111  XNOR   RR ← RR ≡ data         1111  NOPF   no-op, raise flag F
```

Nothing underneath that to abstract away. That's the appeal.

---

### By night

- **[cpu-1bw14500b](https://github.com/1-bit-wonder/cpu-1bw14500b)** — A cycle-accurate Rust simulator of the chip above. One-bit ALU, the sixteen opcodes, no general-purpose registers, checked against the published instruction timing. Simulating most CPUs is an exercise in deciding what to abstract; with this one there is nothing to abstract, which is the point.
- **[noctalia-nixos-tracker](https://github.com/1-bit-wonder/noctalia-nixos-tracker)** — A Luau desktop plugin that tells me the moment a `nixpkgs` PR lands on the branch I care about. Upstream exposes no API, so it parses server-rendered HTML like it's 2004. Runs from the read-only Nix store, keeps its state in `$XDG_STATE_HOME`, never pings twice for the same PR. Born of three days spent manually refreshing a page during a broken-greeter incident.
- **[noctix-os](https://github.com/1-bit-wonder/noctix-os)** — My whole machine as one file: a Hyprland desktop and a nix-darwin Mac from a single cross-platform Nix flake, with VM and ISO outputs. If the hardware goes up in smoke, one `nix build` brings it back bit-for-bit.

### By day

Full-stack web since 2017. I started in the trenches of PHP and Laravel and have spent every year since deleting things. The toolbelt is down to Astro, TypeScript, and plain HTML/CSS, with a database added only when the problem leaves no other option. Fewer moving parts, less to break, on screen before you blink.

### Reading / reach

- Writing — [1-bit-wonder.github.io/blog](https://1-bit-wonder.github.io/blog)
- Mail — [onebitwonder@f-m.fm](mailto:onebitwonder@f-m.fm), or open an issue or PR on any repo here.
- Open to remote work, contracts, and the occasional interesting architectural problem.
