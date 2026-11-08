# [xt-ml.github.io](https://xt-ml.github.io/)

> The central hub and portal for projects, documentation, and static deployments from the **xt-ml** organization.

---

## Published Projects & Sites

| Project                          | Live Site                                                                                               | Source Repository                                                                               | Description                                                                                                                                                                                                                                     |
| :------------------------------- | :------------------------------------------------------------------------------------------------------ | :---------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ShadowClaw**                   | [xt-ml.github.io/shadow-claw](https://xt-ml.github.io/shadow-claw/)                                     | [`xt-ml/shadow-claw`](https://github.com/xt-ml/shadow-claw)                                     | Personal AI agent that runs natively in your terminal, on desktop, or in the browser, with local/cloud LLMs, real shell and filesystem access, and a built-in MCP server.                                                                       |
| **ShadowClaw DAW**               | [xt-ml.github.io/shadow-claw-daw](https://xt-ml.github.io/shadow-claw-daw/)                             | [`xt-ml/shadow-claw-daw`](https://github.com/xt-ml/shadow-claw-daw)                             | In-browser Digital Audio Workstation (DAW) workbench, Web Audio API synthesis engine, TC39 Signals, 15 declarative `scdaw_*` WebMCP tools, autonomous musical skills, and offline WAV bouncing.                                                 |
| **ShadowClaw Light Meter**       | [xt-ml.github.io/shadow-claw-light-meter](https://xt-ml.github.io/shadow-claw-light-meter/)             | [`xt-ml/shadow-claw-light-meter`](https://github.com/xt-ml/shadow-claw-light-meter)             | Hardware light meter sensory workbench, Web Bluetooth GATT telemetry engine, declarative WebMCP sensory tools, and autonomous agent skills for TinyDuino (ASM2001) + Bluegiga BLE112 (ASD2112) + KY-018 Photoresistor.                          |
| **ShadowClaw Single File**       | [xt-ml.github.io/shadow-claw-single-file](https://xt-ml.github.io/shadow-claw-single-file/)             | [`xt-ml/shadow-claw-single-file`](https://github.com/xt-ml/shadow-claw-single-file)             | Zero-install, standalone single-file distribution of ShadowClaw encapsulated in a single HTML document (~64 KB) powered by CDN-delivered modular ESM, browser-native Import Maps, OPFS, and in-browser local AI.                                |
| **ShadowClaw Template**          | [xt-ml.github.io/shadow-claw-template](https://xt-ml.github.io/shadow-claw-template/)                   | [`xt-ml/shadow-claw-template`](https://github.com/xt-ml/shadow-claw-template)                   | Starter template repository for authoring and deploying static websites, knowledge hubs, and agent skills driven by the ShadowClaw engine.                                                                                                      |
| **ShadowClaw Agent CLI Weather** | [xt-ml.github.io/shadow-claw-agent-cli-weather](https://xt-ml.github.io/shadow-claw-agent-cli-weather/) | [`xt-ml/shadow-claw-agent-cli-weather`](https://github.com/xt-ml/shadow-claw-agent-cli-weather) | Model-agnostic weather and report-generation pipeline for operational forecasting, downstream markdown generation, and agent-driven automation workflows.                                                                                       |
| **Block Garden Knowledge Hub**   | [kherrick.github.io/block-garden-knowledge-hub](https://kherrick.github.io/block-garden-knowledge-hub/) | [`kherrick/block-garden-knowledge-hub`](https://github.com/kherrick/block-garden-knowledge-hub) | Interactive documentation portal and technical reference guide for Block Garden—a 3D voxel sandbox exploration, procedural world generation, and farming game engine—featuring embedded custom elements, modding APIs, and in-game agent tools. |
| **pwgen Knowledge Hub**          | [kherrick.github.io/pwgen-knowledge-hub](https://kherrick.github.io/pwgen-knowledge-hub/)               | [`kherrick/pwgen-knowledge-hub`](https://github.com/kherrick/pwgen-knowledge-hub)               | Interactive documentation platform and demonstration engine for the classic Unix `pwgen` password generator compiled to WebAssembly, featuring `<x-pwgen>` custom elements, entropy analysis, and declarative password-generation agent tools.  |

---

## Static Publishing with ShadowClaw

Sites deployed across the `xt-ml` organization leverage ShadowClaw's dual-root static publishing pipeline and CLI.

### 1. Local Development (`shadow-claw`)

Template sites and knowledge hubs can be developed and previewed locally using the `shadow-claw` CLI:

```bash
# Start local development server on http://127.0.0.1:8888
npx shadow-claw dev

# Or compile static production distribution into ./dist/public
npx shadow-claw build --prod
```

### 2. GitHub Actions Deployment

Workflows check out repository content and compile static distribution bundles via GitHub Actions using one of several strategies:

- **Strategy A (Full Fork)**: Fork of `xt-ml/shadow-claw` with in-repo pages and custom components.
- **Strategy B (Pages-only Repo / Toolchain Checkout)**: Content-only repository checking out `xt-ml/shadow-claw` as a CI build dependency.
- **Strategy C (CLI / NPM Package)**: Direct `npx shadow-claw build --prod` workflow without repository cloning.
- **Creative & Audio Workbench Pattern**: [`shadow-claw-daw`](https://github.com/xt-ml/shadow-claw-daw) demonstrates an in-browser Digital Audio Workstation workbench, direct-rendered top-level AudioContext execution, TC39 Signals, Web Locks leader election, and 15 declarative `scdaw_*` WebMCP audio tools.
- **Hardware Sensory Workbench Pattern**: [`shadow-claw-light-meter`](https://github.com/xt-ml/shadow-claw-light-meter) demonstrates integrating physical microcontroller hardware (TinyDuino, Bluegiga BLE112, KY-018 photoresistor) with Web Bluetooth GATT and declarative WebMCP tools.
- **Single-File Distribution**: Zero-shim standalone `index.html` compiled with `npx shadow-claw build --single-file` and deployed directly to static hosting.

For full details on authoring pages, declarative skills, custom element allowlists, and site branding, see the [ShadowClaw Documentation](https://github.com/xt-ml/shadow-claw/tree/main/docs).
