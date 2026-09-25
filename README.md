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

**[Spondula](https://spondula.com)**: send to any S-Handle instead of account numbers,
sort codes, IBANs or wallet addresses. Transfers between S-Handles on the Spondula
network are free. Web, iOS and Android, one network.

**[Fincore.AI](https://github.com/The-Digital-Sandbox/Fincore.AI)**: design prototype
for a fintech app that reads your Big Five personality profile and reframes spending
decisions through it. 32 screens in Next.js. The splash is rendered to video by Remotion
from the same component that draws it in the app, so the two can never disagree.

**[token-gating-admin](https://github.com/The-Digital-Sandbox/token-gating-admin)**:
per-product token gating for a storefront. Contract address, token ID and chain, resolved
live to the collection, with a shopper preview of what a holder and a non-holder each
see. Vite, React, TypeScript, Tailwind v4.

**Crimson Desert mod loader** (private): a C++17 DLL that hooks the game's file API so
modded files load without repacking the archives, plus a decoder for the engine's
undocumented texture format. First use: swapping the game's dragon for Drogon.

**Thursday** (private): a personal assistant that answers on WhatsApp from a memory it
maintains itself, and runs the day to day of the company from a command centre.

---

TypeScript · Next.js · React · Kotlin · Jetpack Compose · Swift · SwiftUI · Rust ·
UniFFI · Firebase · Google Cloud · Playwright · GitHub Actions · Remotion · After Effects
