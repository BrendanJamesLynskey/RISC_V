# ▲ RISC-V — History, ISA &amp; Ecosystem

Interactive single-deck Reveal.js presentation covering RISC-V end-to-end — from its origins at UC Berkeley through the base integer ISAs, the standard extension alphabet, the privilege architecture, virtual memory, traps, the RVV 1.0 vector extension, the hypervisor extension, custom extensions &amp; CHERIoT, the vendor landscape, and the modern software ecosystem.

Designed as interview preparation and self-study material for hardware and silicon engineers, and as a complement to the [RISC-V SoC platform](https://github.com/BrendanJamesLynskey/RISCV_SoC) repos.

## ▶ [Open the Presentation](https://brendanjameslynskey.github.io/RISC_V/)

> **Setup:** Enable GitHub Pages (Settings → Pages → Deploy from `main` branch, `/ (root)` directory).
>
> Alternatively, open `index.html` locally in any browser — the deck works offline after first load.

---

## Topics covered

- **Origins** — UC Berkeley, Patterson &amp; Asanović, the motivation for an open ISA, RISC-V Foundation → RISC-V International.
- **Base ISAs** — RV32I, RV64I, RV32E (embedded, 16 registers), RV128I; instruction formats (R/I/S/B/U/J); the unified register file and PC.
- **Standard extensions** — **M** (multiply/divide), **A** (atomics, LR/SC, AMO), **F/D/Q** (floating-point), **C** (compressed 16-bit), **B** (bit manipulation), **K** (scalar crypto), **V** (vectors), **H** (hypervisor), plus **Zicsr**, **Zifencei**, **Zba/Zbb/Zbc/Zbs**, and the profile system (RVA22/RVA23).
- **Privilege architecture** — M-mode, S-mode, U-mode; CSRs; `mstatus`, `mtvec`, `mepc`, `mcause`; delegation (`medeleg`/`mideleg`).
- **Virtual memory** — Sv32 / Sv39 / Sv48 / Sv57; page table walks; `satp`; TLBs and `SFENCE.VMA`.
- **Traps &amp; interrupts** — synchronous exceptions, asynchronous interrupts, the trap entry/exit sequence, CLINT and PLIC.
- **RVV 1.0 vectors** — the vector register file, `vtype` / `vl`, LMUL, SEW, tail/mask agnostic behaviour, vector load/store, reductions.
- **Hypervisor (H)** — HS-mode, VS-mode, two-stage translation (G-stage + VS-stage), virtualised interrupts.
- **Custom extensions &amp; CHERIoT** — the custom opcode space, vendor extensions, capability-based security on RISC-V.
- **Vendor landscape** — SiFive, Andes, T-Head, Ventana, Tenstorrent, Rivos, Espressif, Raspberry Pi RP2350, MIPS, Western Digital, and the academic cores (Rocket, BOOM, CVA6, Ibex, PULP).
- **Software ecosystem** — GCC &amp; LLVM, Linux, the sbi (SBI/OpenSBI) boot flow, QEMU, Spike, FreeRTOS/Zephyr, Rust on RISC-V.

## Interactive widgets

- **Instruction-format encoder** — pick an instruction; see the live bit-field breakdown across R / I / S / B / U / J formats and the final 32-bit encoding.
- **Mini RV32I CPU stepper** — a cycle-by-cycle stepper running a small Fibonacci program, visualising register-file updates, PC advance, and memory accesses.

---

## Technical details

- **Framework:** [Reveal.js 4.6.1](https://revealjs.com) from CDN
- **Fonts:** Playfair Display (headings), DM Sans (body), JetBrains Mono (code)
- **Offline:** works after first load (fonts &amp; Reveal.js cached by the browser)
- **Navigation:** `→` / `←` for slides, `Esc` for overview, `F` for fullscreen, `S` for speaker notes

## Related repositories

- [Hardware](https://github.com/BrendanJamesLynskey/Hardware) — parent hub indexing all hardware repos and presentations
- [RISCV_SoC](https://github.com/BrendanJamesLynskey/RISCV_SoC) — top-level RISC-V SoC integrating CPU, crossbar, MMU, cache, DMA, IOMMU, and PLIC
- [RISCV_RV32IMC_5stage](https://github.com/BrendanJamesLynskey/RISCV_RV32IMC_5stage) — 5-stage in-order RV32IMC pipeline with caches and AXI4-Lite bus
- [RISCV_RV32I_SingleCycle](https://github.com/BrendanJamesLynskey/RISCV_RV32I_SingleCycle) — single-cycle RV32I reference SoC
- [Cortex_M](https://github.com/BrendanJamesLynskey/Cortex_M) — contrasting 8-part Arm Cortex-M presentation series in the same visual style

## License

Educational use. Content © Brendan Lynskey. Fonts and Reveal.js retain their own licenses.
