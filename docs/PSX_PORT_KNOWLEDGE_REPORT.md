# Monster Rancher 2 port knowledge report

## Identity and lane

- Supported revision: USA `SLUS-00917`
- Architecture: PSXRecomp static recompilation with interpreter fallback
- License boundary: project files use `GPL-3.0-only`; framework and game data
  keep separate rights and licenses
- Source provenance gap: the legacy Wave 1 package has no
  `project-manifest.toml` or `docs/FEASIBILITY.md`

## Current result

This work prepares a RetComM setup-host candidate. It does not establish a
portfolio quality state. Operator-visible gameplay, input, audio, saves, and
package-install checks remain open until their evidence exists.

Generation and the full Release build pass. A bounded hidden run reached
frame 3,278 with 3,278 VBlank raises. It had no fatal state and no automatic
or failed freeze dump. This evidence is a startup result only.

## Corpus consulted

The run checked the required portfolio and release corpus. The source disc is
a complete one-data-track identity: 451,280,592 bytes, MD5
`b41f1f33d1075f22cab7e180f812c0ac`, and SHA-1
`e7418d1491e1809490b2e5fe20d738cb730e5e22`. These values match a
Redump-sourced external identity. The scaffold warning is generic.

## Publication update — 2026-09-03

The next standalone package candidate is `v0.1.1` for Windows x64, Linux
x64, macOS ARM64, and macOS x64. It uses package-only framework child
`e081d29da2fa9862204f63e6b2004d76f1d0cb2d`. Build-only CI and native package gates remain open. This
does not change the title's quality claim.

## 2026-09-04 v0.1.2 POSIX setup-copy candidate

This candidate pins PSXRecomp 40ce47896026be52bcaae7de03b69766e0bd03e4 and recomp-ui be8ac1d03ee19d55394b5a5f2d9d1506edd56659.
Linux and macOS packages use native CMake, Ninja, Python, C, and C++ tools.
Windows keeps the portable toolchain route. This change does not change game
code or the graduation state. Build-only CI and every exact-package release
gate must pass before publication.
