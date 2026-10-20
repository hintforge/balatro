# Balatro -- Achievements

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-10-20
**stub_source:** Stage 0: third-party PlayStation trophy list minus the Platinum. Confirmed in P1 ingestion 2026-10-19 against the TrueAchievements Xbox/Windows list (31 names, all read) and the Steam achievements page (header "31 achievements", 15 of 31 names rendered; all 15 match).
**stub_fetched:** 2026-10-19
**stub_count:** 31
**live_recount:** 2026-10-19, live total 31, name sets equal (31 expected, 31 listed, 0 missing, 0 extra). Receipt: `research_briefs/achievement_completeness_check.md`. The Steam page itself rendered only 15 names in two reads and one more attempt; the full-name comparison rests on the TrueAchievements list, which states 31 achievements and 1,000 Gamerscore. PlayStation adds a 32nd, "Platinum" (not on Steam).
**coverage:** 31 entries; 25 resolved, 6 deferred (mastery entries with no strategy claim in the research; see each entry). 0 unreachable.

## Why this file exists

This file is the corpus's single source of truth for "what achievements does this game have, and what do I need to do for each one." Trigger text is paraphrased, never the developer's wording. Every achievement is repeatable-run content, so none is permanently missable across a profile; the few that close inside a run say so under `ponr-window`. General rules: any deck and stake counts unless the condition says otherwise; challenge runs grant no achievements except the two challenge-completion achievements (see their entries below); some popups appear only when the next run starts or a run is won; "Unlock All" on the profile screen permanently disables achievements for that profile; whether seeded runs or mods block achievements was not found. Hidden flag: none of the 31 is marked hidden on the lists read (all 31 descriptions are public on TrueAchievements); the Steam page's "7 rare" is a completion-rate label, not a hidden flag. Version note: written against the 1.0.1 line; update 1.1 is unreleased.

Design note (zipper 2026-10-19): short achievement lines also appear in `mechanics.md`, `items/` and `sections/missables.md` so a player reading a topic file meets its achievement in place; each carries an `achievement:` key that resolves to an entry here, and this file owns the trigger and status. This overlap is intentional; do not merge it away.

Reference tags `P1-n` / `P2-Rn` resolve in the list at the foot. Shared source for every entry unless the entry says otherwise: P1 + P2 research 2026-10-19, capture web_fetch, confidence high (platform list plus wiki agree). Each section carries that source line above its first entry.

## Progression

_source: P1 + P2 research 2026-10-19 [P1-3][P1-4][P1-5] · capture: web_fetch · confidence: high · category: mainline · vector: achievement_

### Ante Up!
- **id:** ante_up
- **hidden:** no
- **trigger_type:** progression
- **trigger:** reach Ante 4 in any run; shares its trigger with a Joker unlock
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `mechanics.md` "Blinds, antes and rounds", run-structure achievements; `items/abilities.md` row 121
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **resolution:** resolved

> **Cross-system dependency** -- see `dependencies.md` DEP-017

### Ante Upper!
- **id:** ante_upper
- **hidden:** no
- **trigger_type:** progression
- **trigger:** reach Ante 8; shares its trigger with a Joker unlock
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `mechanics.md` "Blinds, antes and rounds", run-structure achievements; `items/abilities.md` row 122
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **resolution:** resolved

> **Cross-system dependency** -- see `dependencies.md` DEP-030

### Heads Up
- **id:** heads_up
- **hidden:** no
- **trigger_type:** progression
- **trigger:** win a run (beat the Ante 8 Showdown) on any deck and stake, not a challenge; unlocks a Joker
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `mechanics.md` "Blinds, antes and rounds", run-structure achievements; `items/abilities.md` row 123
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **resolution:** resolved

> **Cross-system dependency** -- see `dependencies.md` DEP-031

## Mastery

_source: P1 + P2 research 2026-10-19 [P1-3][P1-4][P1-5] · capture: web_fetch · confidence: high · category: mainline · vector: achievement_

### Low Stakes
- **id:** low_stakes
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** win a run on Red Stake or higher; unlocks Zodiac Deck
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** Red Stake unlocked on some deck (one White Stake win with that deck)
- **vector-binding:** `mechanics.md` "Decks and stakes", stake achievements; `items/builds.md` Zodiac row
- **enemy-tier:** 1
- **puzzle-tier:** 1
- **spoiler:** progression
- **resolution:** deferred -- no strategy claim in the research for this stake band; deferred-to: P3 (P3 skipped at setup, so a later top-up). The trigger itself is resolved.

> **Cross-system dependency** -- see `dependencies.md` DEP-028: Low Stakes is the same Red Stake win as the Zodiac Deck unlock.

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

### Mid Stakes
- **id:** mid_stakes
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** win a run on Black Stake or higher; unlocks Anaglyph Deck
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** White, Red and Green wins with the same deck
- **vector-binding:** `mechanics.md` "Decks and stakes", stake achievements; `items/builds.md` Anaglyph row
- **enemy-tier:** 1
- **puzzle-tier:** 1
- **spoiler:** progression
- **resolution:** deferred -- no strategy claim for this stake band; deferred-to: P3 (skipped at setup). Trigger resolved.

> **Cross-system dependency** -- see `dependencies.md` DEP-029: Mid Stakes is the same Black Stake win as the Anaglyph Deck unlock.

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

### High Stakes
- **id:** high_stakes
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** win on Gold Stake (the top stake)
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** Gold Stake unlocked on that deck: wins on all 7 lower stakes with that deck
- **vector-binding:** `mechanics.md` "Decks and stakes", stake achievements; strategy: `items/builds.md` "Deck- and stake-specific advice (Gold Stake, one guide)"
- **enemy-tier:** 2
- **puzzle-tier:** 2
- **spoiler:** late-game
- **resolution:** resolved

### Speedrunner
- **id:** speedrunner
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** win a run in 12 or fewer rounds; same condition as the Merry Andy unlock. The count appears to be blinds played, so at least 12 of the 16 Small and Big Blinds must be skipped (inferred from the 24-round run length)
- **missable:** yes (within a run)
- **ponr-window:** lost for that run once a 13th round is played
- **prereqs:** none
- **vector-binding:** `mechanics.md` "Blinds, antes and rounds" (Speedrunner block); skip-Tag strategy: `mechanics.md` "Skip Tags"
- **enemy-tier:** 1
- **puzzle-tier:** 1
- **spoiler:** progression
- **resolution:** resolved (route is the skip-Tag play; the counting rule is `[Hypothesis -- unverified]`)

> **Cross-system dependency** -- see `dependencies.md` SEQ-001: Playing a 13th round (a 19th for Wee Joker) loses Speedrunner and the round-limit Joker unlocks for that run.

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

### You Get What You Get
- **id:** you_get_what_you_get
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** win a run without ever rerolling the shop. Whether Chaos the Clown's free reroll counts was not found (probably counts)
- **missable:** yes (within a run)
- **ponr-window:** any shop reroll ends it for that run
- **prereqs:** none
- **vector-binding:** `mechanics.md` "Shop, money and interest, rerolls, skip Tags" (reroll achievement block)
- **enemy-tier:** 1
- **puzzle-tier:** 1
- **spoiler:** progression
- **resolution:** deferred -- no strategy claim; deferred-to: P3 (skipped at setup). Trigger resolved.

### Royale
- **id:** royale
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** play a Royal Flush (A-K-Q-J-10 of one suit)
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `mechanics.md` "Scoring", achievement links
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **notes:** boundary call mastery vs discovery: the mechanic is obvious, executing it is the achievement (Rule A)
- **resolution:** deferred -- no strategy claim; deferred-to: P3 (skipped at setup). Trigger resolved.

### Flushed
- **id:** flushed
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** play a Flush made of 5 Wild cards; 4 Wild cards plus Four Fingers also works; the secret hands do not count
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** Wild cards via The Lovers, a shop voucher or Standard Packs
- **vector-binding:** `mechanics.md` "Scoring", achievement links; Wild source: `items/consumables.md` The Lovers, `items/upgrades.md` Wild
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **resolution:** resolved (route via the Wild sources)

### Shattered
- **id:** shattered
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** break 2 Glass cards in a single hand
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** Glass cards via Justice or packs
- **vector-binding:** `items/upgrades.md` "Enhancements" (Shattered block); Glass: 1 in 4 shatter chance per scored card
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **resolution:** resolved (route via Justice and the Glass odds)

### Rule Bender
- **id:** rule_bender
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** complete any one challenge run
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** Challenge Mode: wins with 5 different decks (one source says "five runs using any decks")
- **vector-binding:** `mechanics.md` "Challenges (20) and Challenge Mode"
- **enemy-tier:** 1
- **puzzle-tier:** 1
- **spoiler:** progression
- **resolution:** deferred -- no per-challenge strategy in the research; deferred-to: P3 (skipped at setup). Trigger resolved.

### Rule Breaker
- **id:** rule_breaker
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** complete all 20 challenge runs
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** the chained challenge unlocks (15 challenge wins open all 20)
- **vector-binding:** `mechanics.md` "Challenges (20) and Challenge Mode"
- **enemy-tier:** 1
- **puzzle-tier:** 1
- **spoiler:** progression
- **resolution:** deferred -- no per-challenge strategy; deferred-to: P3 (skipped at setup). Trigger resolved.

### Completionist+
- **id:** completionist_plus
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** win with every deck (15) on Gold Stake. Bug: not awarded on the run that earns the final Gold deck sticker; play one more run on any stake
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** all 15 decks unlocked and Gold Stake reached on each
- **vector-binding:** `mechanics.md` "Unlocks, collection and profiles"; strategy: `items/builds.md` Gold Stake advice
- **enemy-tier:** 2
- **puzzle-tier:** 2
- **spoiler:** late-game
- **notes:** boundary call: finite set (15 decks) suggests collection, but the Gold Stake win is the demanding part, so mastery wins by the first-yes order
- **resolution:** resolved

### Completionist++
- **id:** completionist_plus_plus
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** earn a Gold Stake Sticker on all 150 Jokers; each must be held when a Gold Stake Ante 8 Showdown is beaten. Debuffed Jokers count; Jokers sold before the summary or bought after Ante 8 do not. Legendary Jokers need The Soul during a Gold Stake run (inferred)
- **missable:** yes (within a run)
- **ponr-window:** lost for that run if the Joker is sold or destroyed before winning
- **prereqs:** Gold Stake access; every Joker unlocked
- **vector-binding:** `mechanics.md` "Unlocks, collection and profiles" (Completionist++ block); `mechanics.md` "Decks and stakes" (sticker rules)
- **enemy-tier:** 2
- **puzzle-tier:** 2
- **spoiler:** late-game
- **notes:** boundary call: finite set (150 Jokers) suggests collection; the Gold Stake win per Joker makes it mastery by the first-yes order
- **resolution:** resolved (Rental and Campfire sticker advice in `items/builds.md`)

> **Cross-system dependency** -- see `dependencies.md` SEQ-004: A Joker sold or destroyed before the Gold Stake Ante 8 Showdown is beaten misses its Gold Sticker for that run.

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: structure_

## Collection

_source: P1 + P2 research 2026-10-19 [P1-3][P1-4][P1-5] · capture: web_fetch · confidence: high · category: mainline · vector: achievement_

### Astronomy
- **id:** astronomy
- **hidden:** no
- **trigger_type:** collection
- **trigger:** discover all 12 Planets, including Planet X, Ceres and Eris (play their secret hands first); unlocks Astronomer
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `items/consumables.md` "Planet"; secret hands `mechanics.md` "Scoring"
- **enemy-tier:** 1
- **puzzle-tier:** 1
- **spoiler:** progression
- **resolution:** resolved (12 of 12 located)

> **Cross-system dependency** -- see `dependencies.md` SEQ-005: Planet X, Ceres and Eris show in the shop only after their secret hand has been played that run.
> **Cross-system dependency** -- see `dependencies.md` DEP-036: Discovering every Planet, secret ones included, clears Astronomy and unlocks Astronomer.

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

### Cartomancy
- **id:** cartomancy
- **hidden:** no
- **trigger_type:** collection
- **trigger:** discover all 22 Tarots (one late-game Spectral card does not count); unlocks a Joker
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `items/consumables.md` "Tarot" (22 of 22 listed)
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **resolution:** resolved

> **Cross-system dependency** -- see `dependencies.md` DEP-037

### Clairvoyance
- **id:** clairvoyance
- **hidden:** no
- **trigger_type:** collection
- **trigger:** discover all 18 Spectrals, including The Soul and Black Hole (about 0.3% each per card)
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `items/consumables.md` "Spectral" (18 of 18 listed)
- **enemy-tier:** 2
- **puzzle-tier:** 2
- **spoiler:** late-game
- **resolution:** resolved

### Extreme Couponer
- **id:** extreme_couponer
- **hidden:** no
- **trigger_type:** collection
- **trigger:** discover all 32 vouchers
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** every upgrade unlock condition (for example Petroglyph needs Ante 12, Retcon needs 25 Blinds)
- **vector-binding:** `items/upgrades.md` "Vouchers" (32 of 32 listed)
- **enemy-tier:** 1
- **puzzle-tier:** 1
- **spoiler:** progression
- **resolution:** resolved

### Completionist
- **id:** completionist
- **hidden:** no
- **trigger_type:** collection
- **trigger:** discover 100% of the collection (340 counted items). One Steam thread frames it as the Joker collection only; the Steam and TrueAchievements text says "your collection"
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** every unlock listed in the corpus; "Unlock All" disables achievements on that profile
- **vector-binding:** `mechanics.md` "Unlocks, collection and profiles"
- **enemy-tier:** 2
- **puzzle-tier:** 2
- **spoiler:** late-game
- **notes:** scope conflict logged in `limitations.md`
- **resolution:** resolved

## Threshold

_source: P1 + P2 research 2026-10-19 [P1-3][P1-4][P1-5] · capture: web_fetch · confidence: high · category: mainline · vector: achievement_

### Card Player
- **id:** card_player
- **hidden:** no
- **trigger_type:** threshold
- **trigger:** play 2,500 cards in total across runs; same threshold as a voucher unlock (see `dependencies.md` DEP-038)
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `items/upgrades.md` "Vouchers" (Card Player / Card Discarder block)
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **resolution:** resolved

> **Cross-system dependency** -- see `dependencies.md` DEP-038

### Card Discarder
- **id:** card_discarder
- **hidden:** no
- **trigger_type:** threshold
- **trigger:** discard 2,500 cards in total across runs; same threshold as a voucher unlock (see `dependencies.md` DEP-039)
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `items/upgrades.md` "Vouchers" (Card Player / Card Discarder block)
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **resolution:** resolved

> **Cross-system dependency** -- see `dependencies.md` DEP-039

### Nest Egg
- **id:** nest_egg
- **hidden:** no
- **trigger_type:** threshold
- **trigger:** hold $400 or more at once during a single run; also unlocks Satellite
- **missable:** no
- **ponr-window:** n/a (money can be rebuilt)
- **prereqs:** none
- **vector-binding:** `mechanics.md` "Shop, money and interest, rerolls, skip Tags" (money achievement block)
- **enemy-tier:** 1
- **puzzle-tier:** 1
- **spoiler:** progression
- **resolution:** resolved

> **Cross-system dependency** -- see `dependencies.md` DEP-032: The $400 threshold that clears Nest Egg is also Satellite's unlock condition.

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

### ROI
- **id:** roi
- **hidden:** no
- **trigger_type:** threshold
- **trigger:** buy 5 vouchers by the end of Ante 4; vouchers a deck starts with (Magic, Nebula, Zodiac) do not count
- **missable:** yes (within a run)
- **ponr-window:** closes when Ante 4 ends
- **prereqs:** none
- **vector-binding:** `items/upgrades.md` "Vouchers" (ROI block)
- **enemy-tier:** 1
- **puzzle-tier:** 1
- **spoiler:** progression
- **resolution:** resolved

> **Cross-system dependency** -- see `dependencies.md` SEQ-003: ROI's five-voucher window closes when Ante 4 ends.

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

### Retrograde
- **id:** retrograde
- **hidden:** no
- **trigger_type:** threshold
- **trigger:** get any poker hand to level 10 (one boss's effect can lower levels)
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `mechanics.md` "Scoring", achievement links; `items/upgrades.md` "Hand levels"
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **resolution:** resolved

> **Cross-system dependency** -- see `dependencies.md` DEP-016

### 10K
- **id:** 10k
- **hidden:** no
- **trigger_type:** threshold
- **trigger:** score 10,000 or more chips in one hand; unlocks a Joker
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `mechanics.md` "Scoring", achievement links; `items/abilities.md` row 126
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **resolution:** resolved

> **Cross-system dependency** -- see `dependencies.md` DEP-033

### 1,000K
- **id:** 1000k
- **hidden:** no
- **trigger_type:** threshold
- **trigger:** score 1,000,000 or more chips in one hand; unlocks a Joker
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `mechanics.md` "Scoring", achievement links; `items/abilities.md` row 127
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **resolution:** resolved

> **Cross-system dependency** -- see `dependencies.md` DEP-034

### 100,000K
- **id:** 100000k
- **hidden:** no
- **trigger_type:** threshold
- **trigger:** score 100,000,000 or more chips in one hand; unlocks Stuntman
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** in practice Endless Mode or a strong xMult engine [Hypothesis -- unverified]
- **vector-binding:** `mechanics.md` "Scoring", achievement links; `items/abilities.md` row 136
- **enemy-tier:** 2
- **puzzle-tier:** 2
- **spoiler:** late-game
- **resolution:** resolved

> **Cross-system dependency** -- see `dependencies.md` DEP-035: The 100,000,000-chip hand that clears 100,000K is also Stuntman's unlock condition.

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: structure_

### Tiny Hands
- **id:** tiny_hands
- **hidden:** no
- **trigger_type:** threshold
- **trigger:** thin the deck to 20 or fewer cards
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** removal via The Hanged Man, Trading Card, Glass breaks and similar
- **vector-binding:** `items/upgrades.md` "Enhancements, Seals, Editions" (deck-size block)
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **resolution:** resolved

### Big Hands
- **id:** big_hands
- **hidden:** no
- **trigger_type:** threshold
- **trigger:** have 80 or more cards in the deck
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** additions via DNA, Marble Joker, Standard Packs
- **vector-binding:** `items/upgrades.md` "Enhancements, Seals, Editions" (deck-size block)
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **resolution:** resolved

## Discovery

_source: P1 + P2 research 2026-10-19 [P1-3][P1-4][P1-5] · capture: web_fetch · confidence: high · category: mainline · vector: achievement_

### Legendary
- **id:** legendary
- **hidden:** no
- **trigger_type:** discovery
- **trigger:** discover a Legendary Joker by using The Soul, in an unseeded run
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `items/abilities.md` "Legendary Jokers"
- **enemy-tier:** 2
- **puzzle-tier:** 2
- **spoiler:** late-game
- **resolution:** resolved

## Genre vocabulary

No corpus-specific `genre:` values were added.

## Sources

P1-3 https://steamcommunity.com/achievements/2379780 (Steam page, redirected from /stats/2379780/achievements; recount 2026-10-19) · P1-4 https://balatrowiki.org/w/Achievements · P1-5 https://www.trueachievements.com/game/Balatro/achievements (full 31-name list re-read 2026-10-19) · P1-29 https://balatrogame.fandom.com/wiki/Stickers · P2-R3 https://balatrowiki.org/w/Unlocks · P2-R18 https://steamcommunity.com/app/2379780/discussions/0/604143165271744486 · P2-R4 https://balatrowiki.org/w/Stakes.
