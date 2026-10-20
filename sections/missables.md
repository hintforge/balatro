# Sections -- Missables

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-10-20

Design note (zipper 2026-10-19): this file is an index over claims owned elsewhere (each entry names its primary claim file) and over the `ponr-window` lines in `achievements.md`; the overlap is intentional, so a player asking "what can I lose" has one entry point.

Aggregated catalog of what a player can lose, built from every `missable: yes` claim in the corpus. Balatro runs are repeatable, so **nothing here is permanently lost for a profile**: every window below closes inside one run and can be tried again on the next. Across the profile, no permanent loss was found in the sources read (this is a negative claim, marked unverified by P1).

_source: P1 + P2 research 2026-10-19 [P1-4][P1-22][P2-R3] · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: missable_

## Inside a shop

- **Unbought shop cards and packs** are gone once you leave the shop or reroll; packs restock in each new shop; an unbought voucher can return later (inferred from the restock rules). Primary claim: `../mechanics.md`, "Shop, money and interest, rerolls, skip Tags", the block "What is lost when you leave the shop".

- **Secret Planets** (Planet X, Ceres, Eris): shown only after their hand has been played, and only for the rest of that run. Primary claim: `../items/consumables.md`, "Planet", the block "Secret-Planet window".
> **Cross-system dependency** -- see `dependencies.md` SEQ-005: Planet X, Ceres and Eris show in the shop only after their secret hand has been played that run.

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

## Achievements with a within-run window

- **ROI** -- buy 5 vouchers by the end of Ante 4; lost for that run when Ante 4 ends. Primary claim: `../items/upgrades.md`, Vouchers.
- A round-limit achievement (win in 12 or fewer rounds) -- lost for that run once a 13th round is played. Primary claim: `../mechanics.md`, "Blinds, antes and rounds"; the entry is in `../achievements.md`. Shares its condition with a Joker unlock.
- A no-reroll achievement -- win without rerolling the shop; any reroll ends it for that run; the entry is in `../achievements.md`. Primary claim: `../mechanics.md`, "Shop, money and interest, rerolls, skip Tags".
> **Cross-system dependency** -- see `dependencies.md` SEQ-003: ROI's five-voucher window closes when Ante 4 ends.
> **Cross-system dependency** -- see `dependencies.md` SEQ-001: Playing a 13th round (a 19th for Wee Joker) loses Speedrunner and the round-limit Joker unlocks for that run.

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

The late-game achievement with a within-run window is Completionist++: each of the 150 Jokers must be held when a Gold Stake Ante 8 Showdown is beaten; a Joker sold or destroyed first is lost for that run. Primary claim: `../mechanics.md`, "Unlocks, collection and profiles".

_source: P1 + P2 research 2026-10-19 [P1-4][P1-29][P2-R18] · capture: web_fetch · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: missable_

> **Cross-system dependency** -- see `dependencies.md` SEQ-004: A Joker sold or destroyed before the Gold Stake Ante 8 Showdown is beaten misses its Gold Sticker for that run.

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: structure_

## Joker unlocks decided inside one run

two round-limit Jokers (win in 18 or 12 or fewer rounds), the five hand-type X-Mult Jokers (win without ever playing a Pair, Three of a Kind, Four of a Kind, Straight or Flush) and one Joker that needs a win without holding more than 4 Jokers at any time. Primary claim: `../items/abilities.md`, "Run-scoped unlock windows". Each can be retried on a later run.

> **Cross-system dependency** -- see `dependencies.md` SEQ-002: Playing a Pair, Three of a Kind, Four of a Kind, Straight or Flush loses the matching hand-type Joker unlock for that run.

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_
