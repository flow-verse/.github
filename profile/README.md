# Flux — the open-source Ableton Live alternative

Flux is an **orchestrator, not a new audio engine**: a zero-config, single-window production and live-performance
environment built by weaving together the best FOSS audio tools (Zrythm, Surge XT, Plugdata, Cardinal, Demucs,
Basic Pitch, RAVE, PipeWire) and adding the missing glue: AI on the timeline, live-set automation, and stage tech.

| Repo | Purpose | Language |
|---|---|---|
| [flux-host](https://github.com/flow-verse/flux-host) | Modified Zrythm 2 (v2.0.0-alpha.6): DAW engine + UI, lock-free AI hand-off, MIDI 2.0 | C++23 / Qt / JUCE (AGPL) |
| [flux-ai-bridge](https://github.com/flow-verse/flux-ai-bridge) | CLAP plugin that runs Demucs / Basic Pitch / madmom / RAVE | Rust + Python |
| [flux-installer](https://github.com/flow-verse/flux-installer) | Flatpak/Docker + PipeWire low-latency tuning + bundled plugins | Bash / YAML |
| [flux-stage](https://github.com/flow-verse/flux-stage) | Live-show layer: Ableton Link, OSC, DMX, spatial audio, failover rig | Rust |
| [flux-edge](https://github.com/flow-verse/flux-edge) | Privacy-preserving crowd sensing on Jetson (density metadata only) | Python |
| [flux-docs](https://github.com/flow-verse/flux-docs) | Manual, architecture docs, website | Markdown / Docusaurus |

## Status
- **Done:** `flux-ai` (Demucs stems, Basic Pitch to MIDI), a Rust worker client, a CLAP plugin that captures audio and runs it (tested in a minimal CLAP host), and the Zrythm 2 base imported into `flux-host`.
- **Now:** build `flux-host`, then rebrand it (Zrythm's name and logo cannot be used in modified builds).
- **Next:** return stems to the host as tracks, real installer, docs site.
- **Later:** stage layer (Link/OSC/DMX/spatial), edge crowd sensing.

Work is tracked as issues grouped into phase milestones (P1 Foundation ... P7 Edge) in each repo.
