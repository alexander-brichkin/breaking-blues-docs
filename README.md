# Breaking Blues

> A quiet ally for reaching out — on the days that's hard.

<p align="center">
  <img src="BreakingBlues/Screenshots/surface-home-light.png" width="216" alt="Home"/>
  <img src="BreakingBlues/Screenshots/surface-composer-light.png" width="216" alt="Draft composer"/>
  <img src="BreakingBlues/Screenshots/surface-reflections.png" width="216" alt="Reflections"/>
</p>

**Breaking Blues** is a warm, offline-first iOS app built with a co-design course (CoDHI).
Its first configuration ("Profile #1") is for young men (18–30) in Sweden with recurrent low
periods and social withdrawal. The wedge is the **Social Bridge**: on a hard day, the app
hands you a ready-to-send message to a friend — from your own messenger. Underneath, it's a
**universal, config-driven behavioural testbed** that can A/B-test onboarding and copy without
an App Store release.

## What it is

- **Social Bridge (Flow A)** — a drafted message (Situation × Tone, 18 bilingual templates)
  sent through **15 messengers**; the user always sends it themselves.
- **Nudge · Reflections · Circle** — gentle "reach out" prompts, a calm mood check-in with an
  early-warning signal, and a consented "let my circle check in on me".
- **Config-driven** — layered templates (per-user → per-profile → default → signed baseline)
  and per-feature A/B flags; **safety (Crisis) is never experimented on**.
- **Craft** — iOS 26 (Liquid Glass), WCAG AA on every screen,
  live in-app language switch (English / Svenska).

## Surfaces

Splash · Onboarding · **Home** (hub) · Composer · Add/Edit Friend · Reflections · Circle ·
Settings · Friends · Crisis.

## Documentation

- 📐 **[Design Spec (build brief)](BreakingBlues/docs/DESIGN_SPEC.md)** — per-surface mockups,
  components, interactions, states and functions to build. Start here.
- 🏛 **[Architecture](BreakingBlues/docs/ARCHITECTURE_VISUAL.md)** — system, Social Bridge flow,
  and the config-driven testbed, with diagrams.

## Tech

iOS 26 · SwiftUI · SwiftPM engine (Foundation-only, CLI-testable) · FastAPI backend
(offline-first, never a hard dependency) · xcodegen.

```bash
# engine core — no Xcode needed
cd BreakingBlues/Packages/BreakingBluesEngine && swift test
```

## Conventions

- Every screen: **WCAG AA** accessibility; per-surface audit loop.
- Test-cases first, then functionality, then the visual/accessibility audit.
- All written artefacts (docs, code, commits) in English.

<sub>© Alexander Brichkin. Built with the CoDHI co-design course.</sub>
