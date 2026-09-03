# Monster Rancher 2 validation receipt

## Scope

- Game: Monster Rancher 2, USA, `SLUS-00917`
- Version: `0.1.0`
- Catalog ID: `monster-rancher-2-psx`
- Release repository: `Alexbeav/monster-rancher-2-recomp`
- Publication state: not published

## Frozen inputs

- The source disc identity is in `catalog_identity.json`.
- The required BIOS is a legal SCPH-1001 dump. OpenBIOS is not supported.
- The owned disc has one data track. Its size, MD5, and SHA-1 match the
  published Redump-sourced identity. The generic one-track warning does not
  mean that an audio track is missing for this title.
- Generated retail code, the game executable, the disc, and BIOS remain
  outside Git.

## Required release gates

The release candidate must pass generation, Release build, headless startup,
clean source package, payload, license, and clean-path checks. Alex must then
pass visible gameplay from the exact package.

## Local preparation evidence

- Studio audit: no required failure; two optional box-art warnings
- Code generation: 44 shards and 3,273 dispatch entries
- Full Release build: passed
- Hidden 25-second startup: frame and VBlank counts reached 3,278
- Fatal state: none
- Automatic or failed freeze dumps: none

The hidden test proves bounded startup progress. It does not prove gameplay,
input, audio, saves, or package installation.
