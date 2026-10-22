# Flux — the open-source Ableton Live alternative

Flux is an **orchestrator, not a new audio engine**: a zero-config, single-window production and live-performance
environment built by weaving together the best FOSS audio tools (Zrythm, Surge XT, Plugdata, Cardinal, Demucs,
Basic Pitch, RAVE, PipeWire) and adding the missing glue: AI on the timeline, live-set automation, and stage tech.

| Repo | Purpose | Language |
|---|---|---|
| [flux-host](https://github.com/flow-verse/flux-host) | Branded Zrythm fork: DAW engine + UI, lock-free AI hand-off, MIDI 2.0 | C / C++ |
| [flux-ai-bridge](https://github.com/flow-verse/flux-ai-bridge) | CLAP plugin that runs Demucs / Basic Pitch / madmom / RAVE | Rust + Python |
| [flux-installer](https://github.com/flow-verse/flux-installer) | Flatpak/Docker + PipeWire low-latency tuning + bundled plugins | Bash / YAML |
| [flux-stage](https://github.com/flow-verse/flux-stage) | Live-show layer: Ableton Link, OSC, DMX, spatial audio, failover rig | Rust |
| [flux-edge](https://github.com/flow-verse/flux-edge) | Privacy-preserving crowd sensing on Jetson (density metadata only) | Python |
| [flux-docs](https://github.com/flow-verse/flux-docs) | Manual, architecture docs, website | Markdown / Docusaurus |

## Status
- **Now:** AI bridge. `flux-ai` separates stems (Demucs) and transcribes to MIDI (Basic Pitch); a Rust client runs it as a worker process.
- **Next:** CLAP plugin wrapper (nih-plug), Zrythm fork in `flux-host`, real installer.
- **Later:** stage layer (Link/OSC/DMX/spatial), edge crowd sensing.

Work is tracked as issues grouped into phase milestones (P1 Foundation ... P7 Edge) in each repo.
