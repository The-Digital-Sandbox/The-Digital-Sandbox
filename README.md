## Wael El Hajjar

Software engineer in Manchester, UK. I build production web and mobile systems and go as
deep as the problem needs: a Rust ledger, a C++ DLL hooking a game engine's file API, an
AI assistant that runs on WhatsApp, motion graphics rendered from the same components as
the app. For the last year that has meant founding and shipping a payments network.

Most recently, [Spondula](https://spondula.com): a global payments network where your
S-Handle is your payment identity, the payment equivalent of a username. Live in beta
since June 2026, on the [App Store](https://apps.apple.com/gb/app/spondula/id6798353183)
and [Google Play](https://play.google.com/store/apps/details?id=com.spondula.wallet).
A TypeScript web wallet and gateway, a Kotlin and Compose Android app, a SwiftUI iOS app,
and a Rust core underneath. The signing code both apps depend on is one Rust crate
exposed to Swift and Kotlin, because a wallet that signs payments on two platforms
should have one implementation of the maths, not two. Before that, a small studio
shipping web products for clients.

The habit that runs through most of what I build: **when a fix fails twice, stop
guessing and get evidence.** An animation that would not settle was recorded frame by
frame from the simulator until the broken transition was visible. The key derivation
has a golden vector pinned at three layers, Rust, the FFI boundary and the iOS test, so
a platform port cannot drift. Every large change gets an adversarial review from a
second, independent reviewer before it merges.

**Currently looking for my next role:** full-stack, mobile or product engineering, on a
team that ships. Available now. Remote UK, or hybrid and on site anywhere I can reach
from Manchester. [wael@thedigitalsandbox.co.uk](mailto:wael@thedigitalsandbox.co.uk)

---

### Products

**[Spondula](https://spondula.com)**: send to any S-Handle instead of account numbers,
sort codes, IBANs or wallet addresses. Transfers between S-Handles on the Spondula
network are free. Nine repos: the web wallet, the gateway, the admin console, a merchant
gateway, the status page, an article studio, the iOS app, the Android app and the ledger.
Plus a motion kit in Remotion whose compositions are prop-driven templates, so a corridor
teaser is rendered from data rather than re-edited.

**The Digital Sandbox** (private, live at [thedigitalsandbox.co.uk](https://thedigitalsandbox.co.uk)):
a customer-messaging platform for small businesses. Embeddable chat widget, campaigns
and flows, Meta integrations for Facebook, Instagram and WhatsApp, and a React Native
companion app. Next.js, deployed on Google Cloud.

**Autotube** (private): a multi-tenant short-video generator. Brand configuration drives
the Remotion compositions, so one video engine serves every tenant with their own fonts,
colours and presenter overlays. Tenant-scoped data rules, a render job queue, and a
generic reel composition fed by scene data.

**DigiSkale** (private, team project): a Flutter social app on Firebase, posts, stories,
follows and notifications. My part is the posting and profile features and the data
rules behind them.

**[Fincore](https://github.com/The-Digital-Sandbox/Fincore.AI)**: design prototype for
a fintech app that reads your Big Five personality profile and reframes spending
decisions through it. 38 screens in Next.js and an Expo twin. The splash is rendered to
video by Remotion from the same component that draws it in the app, so the two can never
disagree.

**[token-gating-admin](https://github.com/The-Digital-Sandbox/token-gating-admin)**:
per-product token gating for a storefront. Contract address, token ID and chain, resolved
live to the collection, with a shopper preview of what a holder and a non-holder each
see. Vite, React, TypeScript, Tailwind v4.

### Agents, libraries and tooling

**Thursday** (private): a personal chief of staff that answers on WhatsApp and email from
a memory it maintains itself. A Node server with a React ops deck, a headless CLI runner
for the model with per-thread session continuity, and nightly routines that walk the
day's session captures into atoms, reconcile duplicate entities, and link and abstract
the notes into a graph. Morning brief, end-of-day review and an obligation ledger on top.

**[vault-brain](https://github.com/The-Digital-Sandbox/vault-brain)**: Thursday's memory
pipeline released on its own. Three nightly stages over a markdown vault: walk session
captures into typed atoms on entity notes, reconcile duplicate entities and repoint every
wikilink, then type the relationships between notes and promote well-connected ones into
insight hubs. Ledgers make every stage idempotent, a budget governor can skip a night,
and the model is any command that reads a prompt on stdin. No dependencies, 51 tests.

**[sr25519-uniffi](https://github.com/The-Digital-Sandbox/sr25519-uniffi)**: one Rust
crate for BIP39 mnemonics, sr25519 key derivation, signing, verification and SS58
addresses, exposed to Swift and Kotlin through UniFFI so an iOS app and an Android app
share one implementation of the maths instead of two ports that drift. The golden vector
is pinned at three layers and the signature path is cross-checked against the reference
JavaScript implementation in both directions.

**Hermes Mobile** (private): a platform adapter and Android app that make a phone a
first-class channel for an open-source agent framework. Python plugin, push
notifications, and speech synthesised on send so replies arrive as audio. Kotlin and
Compose chat console. 43 plugin tests and 20 app tests.

**Pixel Agents fork** (private): a fork of a VS Code extension that draws running coding
agents as pixel characters in an office. Added a tower view that stacks workspaces as
floors, tool-name pills above subagents, and a sticky fade on stop so short-lived agents
are visible at all.

### Reverse engineering and hardware

**[crimson-desert-got-dragon-mod](https://github.com/The-Digital-Sandbox/crimson-desert-got-dragon-mod)**:
reverse engineering an undocumented skinned-mesh format. The engine does not store 3D
positions at all; the vertex shader reconstructs them from quantised bytes and a
per-submesh bounding box, found by tracing a draw in PIX and reading the DXIL. A codec
that decodes and re-encodes the format, patchers that redirect assets without touching
game files, and CPU replays of the shader stages checked against the capture. The C++
loader DLL that hooks the game's file API lives in a separate repo.

**BD-1** (in progress): a desk-scale walking companion droid. Twelve bus servos, five per
leg plus head pan and tilt, one IMU, printed PETG spars on bought metal brackets, with
the fan-made shell used as cladding only. Walking chosen over wheels on purpose, because
the character is the point. Radio control first, voice later.

---

TypeScript · Next.js · React · Kotlin · Jetpack Compose · Swift · SwiftUI · Rust ·
UniFFI · Firebase · Google Cloud · Playwright · GitHub Actions · Remotion · After Effects
