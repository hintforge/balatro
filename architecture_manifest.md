# Balatro -- Architecture manifest

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-10-20
**research_run:** P1 + P2, 2026-10-19

Nav-skip corpus: Balatro is a procedural roguelike with no spatial zones (game-type `procedural`, localization-mechanism `none`, both confirmed by P1 and P2), so `nav/` is intentionally absent and the five spatial primitives (zone graph, chapter-zone mapping, optional content, support topology, locks-and-keys) are omitted by design. The non-spatial equivalents are in `mechanics.md`: the per-ante gate loop (zone graph), the save, profile and shop topology (support topology) and the unlock chains (locks-and-keys, mostly in `items/`).

## Hintforge manifest

```
corpus-core-version: 6
game-version: "1.0.1 line (live PC build; last Steam build 17459173, 2025-02-24; in-game string not confirmed)"
game-version-platform: "PC / Steam"
game-version-as-of: 2026-10-19
vector-extensions: none
```

## Vector extensions

None. P1 and P2 found no puzzles, no named-NPC cast, no factions, crew or reputation systems, no endings or branching paths and no optional zones, so no entity-class folder was scaffolded. The five Legendary Jokers are collectible cards, not characters.

Game-type label: procedural
Localization-mechanism class: none
Source-language set: English (developer, Canada). Official Steam localizations are English, French, Italian, German, Spanish (Spain), Dutch, Japanese, Polish, Portuguese (Brazil), Simplified Chinese, Spanish (Latin America) and Traditional Chinese. Russian and Korean are NOT Steam languages, which corrects the Stage 0 guess. Non-English sources read: Simplified Chinese (Joker wiki), Japanese (low quality) and Korean (namu.wiki, used for ante tables, stakes and saves). The ranking of top player-region languages was not verifiable. [Hypothesis -- unverified for the ranking]

## DLC and out-of-scope content

- Balatro Soundtrack: a paid Steam DLC ($2.99); music only, no game content. Out of scope.
- Friends of Jimbo 1-4: free cosmetic collaboration updates (alternate face-card art; Steam builds 2024-08-27, 2024-10-24, 2024-12-12, 2025-02-24). Cosmetic; out of scope.
- Update 1.1: announced, unreleased as of 2026-09-18. Previewed: at least four new Jokers, a Tier 2 Voucher "Lunker", a "card drawn" trigger, a voucher-selection change and another stake rework; free, with a profile toggle to turn the new content off and a Steam branch keeping the 1.0 build. Out of scope; stake and voucher facts here are pre-1.1.

## Run structure

Ante 1 to Ante 8, three blinds each (Small, Big, Boss); beating the Ante 8 Showdown boss wins the run; Endless Mode continues from Ante 9 with Showdown bosses at 16, 24 and 32, and Ante 39 is the effective ceiling. Details, targets and the gate loop: `mechanics.md`.

## Optional content registry

Everything unlockable is `always-available` in the sense that runs repeat and nothing on a profile is permanently lost (unverified negative claim). Failure modes: progress and achievements are per profile (3 slots); seeded runs discover nothing; challenge runs grant no achievements except the two challenge-completion achievements; "Unlock All" disables achievements for that profile; one collection achievement has a final-run bug (see `achievements.md`). Locked content: 45 Jokers, 14 decks, 16 vouchers, 7 stakes per deck and Challenge Mode with 20 challenges (103 locks); where each is documented: `items/abilities.md`, `items/builds.md`, `items/upgrades.md`, `mechanics.md`.

## Collection totals (expected / located)

Jokers 150/150; Tarot 22/22; Planet 12/12 (the Steam store page says 11); Spectral 18/18; Vouchers 32/32; Decks 15/15; Stakes 8; Boss Blinds 23 + 5 Showdown; Tags 24/24; Enhancements 8; Seals 4; Editions 4 plus base; Challenges 20/20; Booster pack variants 15 by type and size (the Collection reportedly counts 32 entries; unexplained). Achievements 31/31.
