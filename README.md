# `1-bit-wonder`

Full-stack web developer by trade, low-level tinkerer by inclination. The two have more in common than they look: both come down to removing layers until little is left to hide behind. A static page at one end, a single-bit CPU at the other.

The name is a debt to the **Motorola MC14500B**, a processor from 1977 with a one-bit accumulator where its contemporaries had four or eight. It holds a single true or false, and that is the entire machine. People built traffic lights and freight elevators out of it.

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

Nothing underneath that to abstract away.

---

### By night

- **[cpu-1bw14500b](https://github.com/1-bit-wonder/cpu-1bw14500b)** — A cycle-accurate Rust simulator of the chip above. One-bit ALU, the sixteen opcodes, no general-purpose registers, checked against the published instruction timing. Simulating most CPUs means deciding what to abstract; this one has nothing to abstract.
- **[fractals](https://github.com/1-bit-wonder/fractals)** — A 1-bit fractal generator that renders square avatars in pure black and white. Fourteen fractals fill an 8-bit brightness buffer — escape-time ones (Mandelbrot, Julia, Burning Ship) in hand-written WASM, the geometric ones in TypeScript — and a single quantize step collapses that to one bit of ink, by hard threshold or 8×8 Bayer dither. Keeping the 8-bit intermediate makes re-dithering instant, with no recompute. Exports true one-bit-per-pixel PNGs, hand-encoded, about eight times smaller than the usual.
- **[noctalia-nixos-tracker](https://github.com/1-bit-wonder/noctalia-nixos-tracker)** — A Luau desktop plugin that tells me the moment a `nixpkgs` PR lands on the branch I care about. Upstream exposes no API, so it parses server-rendered HTML like it's 2004. Runs from the read-only Nix store, keeps its state in `$XDG_STATE_HOME`, never pings twice for the same PR. Born of three days spent manually refreshing a page during a broken-greeter incident.
- **[noctix-os](https://github.com/1-bit-wonder/noctix-os)** — My whole machine as one file: a Hyprland desktop and a nix-darwin Mac from a single cross-platform Nix flake, with VM and ISO outputs. If the hardware goes up in smoke, one `nix build` brings it back bit-for-bit.

### By day

Full-stack web since 2017. I started in the trenches of PHP and Laravel and have spent every year since deleting things. The toolbelt is down to Astro, TypeScript, and plain HTML/CSS, with a database added only when the problem leaves no other option. Fewer moving parts, less to break.

### Reading / reach

- Writing — [1-bit-wonder.github.io/blog](https://1-bit-wonder.github.io/blog)
- Mail — [onebitwonder@f-m.fm](mailto:onebitwonder@f-m.fm), or open an issue or PR on any repo here.
- Open to remote work, contracts, and the occasional interesting architectural problem.
