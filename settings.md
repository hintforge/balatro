# Balatro -- Settings

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-10-20

Settings that affect difficulty, perception or comfort, organised by the in-game Settings tabs. Tab and option names come from the wiki's Settings page; the exact menu labels were not verified in the game. Every setting applies across all profiles. Reference tags resolve in the list at the foot.

_source: P1 research 2026-10-19 [P1-25][P1-24][P1-39] · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: settings_

| Tab | Setting | Values (default) | Effect on perception or difficulty |
|---|---|---|---|
| Game | Game Speed | 0.5 / 1 / 2 / 4 (1) | animation speed only; slow speed (0.5-1) is recommended for frame-tight tricks such as buying vouchers before a Voucher Tag fires |
| Game | Play/Discard button position | Play-Discard or Discard-Play | prevents mis-clicks for left- or right-handed play |
| Game | Screenshake | 0-100% (30% desktop, 50% mobile) | motion comfort |
| Game | Display Stake Stickers during Run | off/on (off) | shows each Joker's best stake sticker in-run; useful for tracking a late-game achievement (see `mechanics.md`, Stake Stickers) |
| Game | High Contrast Cards | off/on (off) | Clubs light blue, Diamonds orange, Hearts more saturated red, Spades darker black, higher-contrast face cards; the main colour-blind aid |
| Game | Reduced Motion | off/on (off) | disables idle, trigger, background and text animation and forces screenshake off; added in 1.0.1 (from a patch-coverage snippet, not read) [Single source -- verify] |
| Video | Monitor, Window Mode (Windowed / Fullscreen / Borderless, default Borderless), Resolution, VSync (on; off uncaps to about 500 FPS) | -- | video changes apply on "Apply" and restart the game; not on mobile |
| Graphics | Shadows (on), Pixel Art Smoothing (on), CRT 0-100% (70% desktop, 30% mobile), CRT Bloom (on) | -- | lowering CRT removes scanlines and distortion; readability aid (inferred) |
| Audio | Master 80%, Music 100%, Game 100% | -- | -- |

_source: P1 research 2026-10-19 [P1-25][P1-24][P1-39] · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: settings_

- Customize Deck switches the face-card art (the free Friends of Jimbo cosmetic updates) and carries the same High Contrast toggle.
- No setting changes game difficulty; difficulty comes only from stakes and decks (not confirmed as exhaustive). [Hypothesis -- unverified]
- Save-file location and profile handling: see `mechanics.md`.
> **Cross-system dependency** -- see `dependencies.md` SEQ-004
- Role split with `controls.md`: this file owns the option values; `controls.md` owns input and the accessibility summary (it points here for the setting values).

## Sources

P1-24 https://balatrowiki.org/w/Options · P1-25 https://balatrowiki.org/w/Settings · P1-39 https://www.familygamingdatabase.com/accessibility/Balatro
