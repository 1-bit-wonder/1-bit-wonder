# Hi, I'm 1-bit-wonder 👋

> **Full-stack web developer by trade, low-level tinkerer by inclination.**  
> The two have more in common than they look. Both are about stripping away layers until there's nothing left to hide behind—whether that's a static HTML page or a 1-bit CPU.

The patron saint of this profile is the **Motorola MC14500B**: a processor from 1977 with a one-bit accumulator. Not 8-bit, not 4-bit. *One.* It can hold a single true or false, and that's the whole show. People built traffic lights and industrial elevators out of these things. I think that's beautiful, and I'm not totally sure why.

---

## 🌙 By Night (Systems & Tinkering)

*   **[cpu-1bw14500b](https://github.com/1-bit-wonder/cpu-1bw14500b)**  
    A cycle-accurate Rust simulator of that little chip. One-bit ALU, 16 opcodes, no general-purpose registers, checked against its published instruction timing. Most CPUs you simulate require abstracting things away; with this one, there's nothing *to* abstract. That's the appeal.
*   **[noctalia-nixos-tracker](https://github.com/1-bit-wonder/noctalia-nixos-tracker)**  
    A Luau desktop plugin that tells me when a `nixpkgs` PR lands on the branch I care about. There's no API, so it scrapes the server-rendered HTML like it's 2004. Runs from the read-only Nix store, keeps state in `$XDG_STATE_HOME`, and never pings twice for the same PR. Built because a broken login greeter once had me manually refreshing a webpage for three days straight.
*   **[noctix-os](https://github.com/1-bit-wonder/noctix-os)**  
    My entire digital footprint in a single Nix flake: a Hyprland desktop and a nix-darwin Mac setup. Fully cross-platform, featuring automated VM and ISO outputs. If I set my computer on fire, I can have it back exactly as it was with a single `nix build`.

## ☀️ By Day (Web Architecture)

**Full-stack web development since 2017.** I started in the trenches of PHP and Laravel and have spent every year since deleting things.

Now, my toolbelt is stripped down to **Astro, TypeScript, and plain HTML/CSS**, spinning up a database only when the problem leaves me absolutely no choice. The dream is a page that is *just a page*. Fewer moving parts, nothing to break, and loads before you blink.

---

## 📬 Read / Reach

*   **Writing:** I write things up at [1-bit-wonder.github.io/blog](https://1-bit-wonder.github.io/blog)
*   **Email:** [onebitwonder@f-m.fm](mailto:onebitwonder@f-m.fm)
*   **Open Source:** Feel free to open an issue or PR on any repository here.

**💡 Available for remote work, contracts, and interesting architectural problems.**

<details>
<summary>📊 GitHub metrics</summary>

![Metrics](/github-metrics.svg)

</details>
