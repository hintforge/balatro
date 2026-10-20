# Balatro -- Mechanics

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-10-20

Core game-system rules. Built from P1 (2026-10-19) and P2 (2026-10-19) research. Item-level detail lives in `items/`. Reference tags: `P1-n` and `P2-Rn` point to the numbered URL lists at the foot of this file. Version note: facts describe the 1.0.1 line (the live PC build, see "Version" below); announced update 1.1 is unreleased and may change stakes, vouchers and Jokers.

Per-claim metadata is written once per block on the italic `_source:` line under the block heading. Conflicts between sources are named in the text and logged in `limitations.md`.

## Version and platform

- Live PC build: the 1.0.1 line. Last numbered patch notes on Steam are "1.0.1f - Patch notes" (2024-05-01); the last Steam build is 17459173, "Welcoming Friends of Jimbo 4!" (2025-02-24); SteamDB shows no later build. Two Fandom pages cite "1.0.1o-FULL" as current; the in-game version string itself was not confirmed. [P1-26][P1-2][P1-10][P2-R20][P2-R21]
- Update 1.1 is announced and unreleased (2026-09-16 and 2026-09-18 coverage); it will be free and will add new Jokers and a Tier 2 Voucher ("Lunker"), and it plans another stake rework. Treat every stake and voucher fact here as pre-1.1. [P1-27][P2-R20]
- Pre-1.0.1 differences that old guides still carry: two stake rules differed before 1.0.1, and the 1.0.1 experimental patch lowered ante scaling on two stakes (patch coverage snippet, not read). Details: see Decks and stakes. [P2-R10][hypothesis for the scaling change]

_source: P1 + P2 research 2026-10-19 · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: structure_

## Scoring (chips x mult, poker hands, hand levels)

A hand scores Chips x Mult. Each poker hand has a base Chips and Mult at level 1 and gains fixed Chips and Mult per level; Planet cards raise levels. [P1-17][P1-7]

_source: P1 research 2026-10-19 [P1-17][P1-7] · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: mechanic_

| Hand | Level-1 Chips x Mult | Per level (Chips / Mult) | Planet | Cards that score |
|---|---|---|---|---|
| High Card | 5 x 1 | +10 / +1 | Pluto | highest card only |
| Pair | 10 x 2 | +15 / +1 | Mercury | the 2 matching cards |
| Two Pair | 20 x 2 | +20 / +1 | Uranus | the 4 paired cards |
| Three of a Kind | 30 x 3 | +20 / +2 | Venus | the 3 matching cards |
| Straight | 30 x 4 | +30 / +3 | Saturn | all 5 |
| Flush | 35 x 4 | +15 / +2 | Jupiter | all 5 |
| Full House | 40 x 4 | +25 / +2 | Earth | all 5 |
| Four of a Kind | 60 x 7 | +30 / +3 | Mars | the 4 matching cards |
| Straight Flush | 100 x 8 | +40 / +4 | Neptune | all 5 |
| Royal Flush | 100 x 8 (shares Straight Flush's level) | as Straight Flush | Neptune | all 5 |

_source: P1 research 2026-10-19 [P1-17][P1-7] · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: mechanic_

Secret hands (shown only after first played; their Planets then appear in the shop for the rest of that run only; one late-game Spectral card still levels them):

_source: P1 research 2026-10-19 [P1-17][P1-7] · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: mechanic_

| Secret hand | Level-1 | Per level | Planet |
|---|---|---|---|
| Five of a Kind | 120 x 12 | +35 / +3 | Planet X |
| Flush House | 140 x 14 | +40 / +4 | Ceres |
| Flush Five | 160 x 16 | +50 / +3 | Eris |

_source: P1 research 2026-10-19 [P1-17][P1-7] · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: mechanic_

Scoring rules and exceptions:

_source: P1 research 2026-10-19 [P1-17][P1-2][P1-1][P1-18] · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: mechanic_

- Kickers: in High Card, Pair, Two Pair, Three of a Kind and Four of a Kind, the extra played cards do not score and trigger no "when scored" effects, so players use them as extra discards. This does not work on five-card hands.
- Splash makes every played card score. Stone cards have no rank or suit, give +50 Chips and always score.
- The highest-tier hand wins regardless of level (9-9-9-9-2 in one suit is Four of a Kind, not Flush).
- "Contains" Joker text fires when the played hand includes that type: Three of a Kind contains a Pair; Four of a Kind does not contain Two Pair.
- Four Fingers lets Flushes and Straights use 4 cards; a Straight may then include a duplicate rank.
- Card order does not change hand type but decides which card scores first (matters for first-scored-card Jokers).
- One boss's effect treats Royal Flush and Straight Flush as separate hand types even though they share one level.
- Debuffed Wild Cards score as their original suit.
- Rounding is not covered by the sources read; discount-voucher prices round half down, and endless requirements round to two significant figures. [location inventory incomplete]

Order of scoring operations [P1-21][P1-2][P1-36]:

_source: P1 research 2026-10-19 [P1-21][P1-2][P1-36] · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: mechanic_

1. Boss Blind effects resolve first (a few Boss Blinds change base Chips and Mult or lower the played hand's level).
2. "On played" Jokers fire (Space Joker, DNA, Midas Mask, Green Joker's gain).
3. Each scoring card fires left to right: base chips plus bonus chips; enhancement, then seal (only the Gold Seal pays here), then edition; each Joker's "on scored" effect left to right; then retriggers repeat those steps (Red Seal first, then retrigger Jokers left to right). Retriggers stack additively; one retrigger does not multiply another.
4. Held-in-hand effects fire left to right: Steel cards' X1.5, then "on held" Jokers (Baron, Raised Fist, Reserved Parking), then held retriggers (Red Seal, then Mime).
5. Jokers fire left to right. Within each Joker: Foil or Holographic bonus, then its independent effect (retriggers do not affect it), then Joker-on-Joker effects (Baseball Card), then its Polychrome X1.5 after its own ability.
6. With one voucher, Planet cards held in the consumable area give X1.5 Mult each (see `items/upgrades.md`).
7. One deck balances Chips and Mult at the very end.

Exceptions (rule of thumb "put xMult on the right" is not universal):

_source: P1 research 2026-10-19 [P1-21][P1-35][P1-36] · capture: web_fetch · confidence: low · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: mechanic_

- Only independent Joker effects depend on Joker position. On-scored xMult (Photograph, Ancient Joker and others) applies during card scoring, before any independent Joker, so moving it right does nothing unless another on-scored Joker interacts with it. Worked example: 40 chips and 4 Mult with a +4 Joker left of Ramen (X2) scores 640; reversed, 480. (Reddit comment 2025-03-23 plus wiki; one forum source.)
- A Steam thread did not settle whether the Red Seal fires before or after Joker retriggers; the wiki says Red Seal first. Midas Mask left of Vampire feeds Vampire's scaling; right of it, the Gold cards stay in the deck.

Achievement links (cards played and big hands): the achievements Royale (play a Royal Flush), Flushed (play a Flush of 5 Wild cards; 4 Wild plus Four Fingers also works; the secret hands do not count), Retrograde (get any poker hand to level 10), 10K (score 10,000+ Chips in one hand) and 1,000K (1,000,000+) are documented here and in `achievements.md`.

_source: P1 research 2026-10-19 [P1-4][P1-3][P1-5] · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: mechanic · achievement: royale, flushed, retrograde, 10k, 1000k · achievement-hidden: no · trigger_type: mastery, mastery, threshold, threshold, threshold_

> **Cross-system dependency** -- see `dependencies.md` DEP-004: only independent Joker effects depend on position; on-scored xMult resolves before them.
> **Cross-system dependency** -- see `dependencies.md` DEP-009: Midas Mask left of Vampire feeds Vampire's scaling.
> **Cross-system dependency** -- see `dependencies.md` DEP-010: Baron, Mime, Steel and Red Seal all resolve in the held-in-hand step.
> **Cross-system dependency** -- see `dependencies.md` DEP-011
> **Cross-system dependency** -- see `dependencies.md` DEP-014
> **Cross-system dependency** -- see `dependencies.md` DEP-016
> **Cross-system dependency** -- see `dependencies.md` DEP-033
> **Cross-system dependency** -- see `dependencies.md` DEP-034

The largest chips-in-one-hand achievement, 100,000K (100,000,000+; in practice needs Endless or a strong xMult engine), is documented here and in `achievements.md`.

_source: P1 research 2026-10-19 [P1-4][P1-3][P1-5] · capture: web_fetch · confidence: high · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: mechanic · achievement: 100000k · achievement-hidden: no · trigger_type: threshold_

> **Cross-system dependency** -- see `dependencies.md` DEP-035: The 100,000,000-chip hand that clears 100,000K is also Stuntman's unlock condition.

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: structure_

## Blinds, antes and rounds (Small / Big / Boss, hands and discards per round)

A run starts at Ante 1; each Ante has three blinds in order. Small and Big Blinds can be skipped for a Tag; the Boss Blind cannot. Failing any blind (last hand short of the target) ends the run; a locked Joker can prevent this once if at least 25% of the target was scored. A full non-skipping win is 24 rounds. [P1-13][P1-14][P1-1][P2-R10]

_source: P1 + P2 research 2026-10-19 [P1-13][P1-14][P2-R1][P2-R10] · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: structure_

| Blind | Score | Reward | Skippable |
|---|---|---|---|
| Small Blind | 1x base | $3 | yes, for a Tag |
| Big Blind | 1.5x base | $4 | yes, for a Tag |
| Boss Blind | 2x base (a few bosses differ: 1x to 4x) | $5 | no |
| Showdown Boss Blind (Ante 8/16/24/32) | 2x base (one Showdown boss 6x) | $8 | no |

_source: P1 + P2 research 2026-10-19 [P1-13][P1-14][P2-R1][P2-R10] · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: structure_

Unused hands pay $1 each at cash-out. A blind survived through that Joker pays no reward. The Small Blind also pays $0 in the Cruelty and The Omelette challenges. [P1-20][P2-R7][P2-R12]

Base chip requirement per Ante (multiply by the blind multiplier; one deck doubles every requirement). The second and third columns are the faster-scaling stakes (which stake uses which column: see Decks and stakes). Figures to Ante 16 agree between the English wiki and the Korean wiki (namu.wiki). Old guides from before May 2024 may differ (the 1.0.1 patch changed the scaling of two stakes).

_source: P1 + P2 research 2026-10-19 [P1-13][P1-14][P2-R1][P2-R10] · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: structure_

| Ante | Base scaling | Faster scaling | Fastest scaling |
|---|---|---|---|
| 0 and below | 100 | 100 | 100 |
| 1 | 300 | 300 | 300 |
| 2 | 800 | 900 | 1,000 |
| 3 | 2,000 | 2,600 | 3,200 |
| 4 | 5,000 | 8,000 | 9,000 |
| 5 | 11,000 | 20,000 | 25,000 |
| 6 | 20,000 | 36,000 | 60,000 |
| 7 | 35,000 | 60,000 | 110,000 |
| 8 (Showdown) | 50,000 | 100,000 | 200,000 |

_source: P1 + P2 research 2026-10-19 [P1-13][P1-14][P2-R1][P2-R10] · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: structure_

Ante 1 targets are 300 / 450 / 600 for Small / Big / Boss at every stake. At Ante 8 the base-scaling Showdown needs 100,000 (one Showdown boss triples that). A January 2026 guide that says the Ante 8 target is "roughly 300 million chips" is wrong for the base game (wiki tables put even the fastest-scaling worst case at 1.2 million); it is `[Contradicted across sources -- see notes]` in `limitations.md`. [P1-37]

### Per-ante gate sequence (the same loop every ante)

| # | Gate | Decision or checkpoint |
|---|---|---|
| 1 | Blind Select (Small) | Play, or skip for the Tag shown under it. Skipping forfeits that blind's cash-out and its shop (no money of any kind, no shop visit). |
| 2 | Small Blind play | Play hands and discard until the score reaches the target; running out of hands ends the run. |
| 3 | Cash Out | Automatic: blind reward, $1 per unused hand, Joker payouts, then interest. |
| 4 | Shop | Buy, sell, reroll, open packs, redeem the Voucher. Reroll price resets to $5 on entering each new shop. |
| 5 | Blind Select (Big) | Play, or skip for a Tag. |
| 6-7 | Big Blind play, Cash Out, Shop | As 2-4. |
| 8 | Blind Select (Boss) | Cannot be skipped. Optional Boss reroll: two vouchers (once per Ante, or unlimited), $10 each, or the Boss Tag. |
| 9 | Boss Blind play | The boss's effect is active. |
| 10 | Cash Out, Shop | Boss reward $5 ($8 Showdown). The Voucher slot restocks only after a Boss Blind is defeated. |
| 11 | Ante transition | Ante +1 after the Boss. Beating the Ante 8 Showdown wins the run. |

_source: P2 research 2026-10-19 [P2-R1][P2-R2][P2-R6][P2-R7][P2-R10] · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: structure_

- Whether the upcoming Boss is shown from the start of the ante is inferred, not stated by any source read. [Hypothesis -- unverified]
- Interest is paid at Cash Out after each blind actually played; a skipped blind has no Cash Out, so earns no interest (inferred). Shop reroll cost resets every shop, not every ante; the once-per-Ante boss reroll resets every ante. Tags resolve oldest first. How the Small and Big Blind Tags are chosen: `key: unknown`.
- Ante 4: reaching it gives the Ante Up! achievement and unlocks a Joker (`items/abilities.md`). In the Typecast challenge, beating the Ante 4 boss locks every Joker in place for the rest of the run and sets Joker slots to 0. Ante 8: reaching it gives Ante Upper! and unlocks a Joker; winning gives Heads Up and unlocks a Joker, and stamps a Stake Sticker (see Decks and stakes).
- From Ante 2 the Tag pool grows from 15 to 24; the boss pool grows by ante (below). Dropping from Ante 8 to Ante 7 with an ante-lowering voucher does not change an already-assigned Showdown blind.

Run-structure achievements: Ante Up! (reach Ante 4), Ante Upper! (reach Ante 8) and Heads Up (win a run on any deck and stake, not a challenge).

_source: P1 + P2 research 2026-10-19 [P1-4][P2-R3][P2-R11] · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: structure · achievement: ante_up, ante_upper, heads_up · achievement-hidden: no · trigger_type: progression, progression, progression_

Speedrunner (win a run in 12 or fewer rounds; the game counts blinds played, so at least 12 of the 16 Small and Big Blinds must be skipped, inferred from the 24-round run length) is lost for that run once a 13th round is played. It shares its condition with the Merry Andy unlock.

_source: P1 + P2 research 2026-10-19 [P1-4][P1-14][P2-R3] · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure · missable: yes · achievement: speedrunner · achievement-hidden: no · trigger_type: mastery_

> **Cross-system dependency** -- see `dependencies.md` DEP-017: Reaching Ante 4 clears the Showman unlock and the Ante Up! achievement together.
> **Cross-system dependency** -- see `dependencies.md` DEP-030: Reaching Ante 8 clears the Flower Pot unlock and the Ante Upper! achievement together.
> **Cross-system dependency** -- see `dependencies.md` DEP-031: The first win clears the Blueprint unlock and the Heads Up achievement together.
> **Cross-system dependency** -- see `dependencies.md` SEQ-001: Playing a 13th round (a 19th for Wee Joker) loses Speedrunner and the round-limit Joker unlocks for that run.
> **Cross-system dependency** -- see `dependencies.md` SEQ-003: ROI's five-voucher window closes when Ante 4 ends.
> **Cross-system dependency** -- see `dependencies.md` DEP-012

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

## Boss blinds (including the Ante 8 showdown boss)

Boss Blinds impose a negative effect. Rules: only bosses at or below their minimum Ante are eligible (Ante 1 draws from 8); no boss repeats until every eligible boss has appeared once, whether defeated or rerolled away; rerolling at Ante 8 (or any multiple of 8) always gives a Showdown boss; disabling a boss (by Joker) also returns the high-multiplier bosses to 2x. The collection holds 30 blinds (Small, Big, 23 bosses, 5 Showdown). One Showdown boss flips Jokers face down; four Jokers stay recognisable under it. [P1-13][P1-14][P2-R1]

_source: P1 + P2 research 2026-10-19 [P1-13][P1-14][P2-R1] · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: boss_

Regular Boss Blinds (23; reward $5; effects paraphrased). The regular-boss tier call (progression, not late-game) is explained in the CHECKPOINT changelog.

_source: P1 + P2 research 2026-10-19 [P1-13][P1-14][P2-R1] · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: boss_

| Boss | Effect | Min Ante | Score | Notes |
|---|---|---|---|---|
| The Hook | discards 2 random held cards after each hand played | 1 | 2x | the discards count for Mail-In Rebate, Castle, Hit the Road; they hurt Green Joker and Ramen |
| The Club | all Clubs debuffed | 1 | 2x | |
| The Psychic | must play 5 cards | 1 | 2x | not all 5 need to score |
| The Goad | all Spades debuffed | 1 | 2x | |
| The Window | all Diamonds debuffed | 1 | 2x | |
| The Manacle | -1 hand size | 1 | 2x | |
| The Pillar | cards already played this Ante are debuffed | 1 | 2x | a played card modified afterwards counts as new |
| The Head | all Hearts debuffed | 1 | 2x | |
| The House | first hand drawn face down | 2 | 2x | |
| The Wall | extra large blind | 2 | 4x | disabled: drops to 2x; selling Luchador while already above 2x wins instantly |
| The Wheel | 1 in 7 cards drawn face down | 2 | 2x | |
| The Arm | lowers the played hand's level by 1 (minimum 1) | 2 | 2x | until 1.0.0k it could reach level 0 |
| The Fish | cards drawn face down after each hand | 2 | 2x | |
| The Water | start with 0 discards | 2 | 2x | |
| The Mouth | only one hand type allowed this round | 2 | 2x | |
| The Needle | only one hand | 2 | 1x | not raised by boss-disabling Jokers |
| The Flint | base Chips and Mult halved | 2 | 2x | |
| The Mark | all face cards drawn face down | 2 | 2x | |
| The Eye | no repeated hand types this round | 3 | 2x | |
| The Tooth | lose $1 per card played | 3 | 2x | can push you into debt |
| The Plant | all face cards debuffed | 4 | 2x | |
| The Serpent | always draw exactly 3 after a play or discard | 5 | 2x | ignores hand size |
| The Ox | playing your most-played hand sets money to $0 | 6 | 2x | counts Royal Flush and Straight Flush separately |

_source: P1 + P2 research 2026-10-19 [P1-13][P1-14][P2-R1] · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: boss_

Showdown (Finisher) Boss Blinds (5; minimum Ante 8; reward $8):

_source: P1 + P2 research 2026-10-19 [P1-13][P1-14][P2-R1] · capture: web_fetch · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: boss_

| Boss | Effect | Score |
|---|---|---|
| Amber Acorn | flips and shuffles all Jokers face down | 2x |
| Verdant Leaf | all cards debuffed until 1 Joker is sold | 2x |
| Violet Vessel | very large blind | 6x |
| Crimson Heart | one random Joker disabled each hand | 2x |
| Cerulean Bell | forces one card to stay selected | 2x |

_source: P1 + P2 research 2026-10-19 [P1-13][P1-14][P2-R1] · capture: web_fetch · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: boss_

Counter-play: Luchador (sell to disable the current boss), Chicot (disables every boss), Director's Cut and Retcon ($10 per reroll), Boss Tag, Matador (pays $8 when a hand triggers the boss ability). Verdant Leaf, Crimson Heart and Amber Acorn punish builds that depend on one Joker (inference from effects). [P1-1][P1-9][P1-15][P1-13] [Hypothesis -- unverified for the build-fit remarks]

_source: P1 research 2026-10-19 [P1-1][P1-9][P1-15][P1-13] · capture: web_fetch · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: boss_

Boss pool by minimum Ante (names only; the pool is cumulative): Ante 1 adds 8 bosses (The Hook, The Club, The Psychic, The Goad, The Window, The Manacle, The Pillar, The Head); Ante 2 adds 10 (18 total); Ante 3 adds The Eye and The Tooth (20); Ante 4 adds The Plant (21); Ante 5 adds The Serpent (22); Ante 6 adds The Ox (23); Antes 8, 16, 24 and 32 draw only from the 5 Showdown bosses. [P2-R1][P2-R10]

_source: P2 research 2026-10-19 [P2-R1][P2-R10] · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: boss_

> **Cross-system dependency** -- see `dependencies.md` DEP-002: The Hook's forced discards count for Mail-In Rebate.
> **Cross-system dependency** -- see `dependencies.md` DEP-018: The Hook's forced discards count for Castle.
> **Cross-system dependency** -- see `dependencies.md` DEP-019: The Hook's forced discards count for Hit the Road when a Jack is among them.
> **Cross-system dependency** -- see `dependencies.md` DEP-020: The Hook's forced discards work against Green Joker.
> **Cross-system dependency** -- see `dependencies.md` DEP-021: The Hook's forced discards work against Ramen.
> **Cross-system dependency** -- see `dependencies.md` DEP-003
> **Cross-system dependency** -- see `dependencies.md` DEP-013: Narrowing the deck to one suit exposes it to the matching suit-debuff boss.

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

## Shop, money and interest, rerolls, skip Tags

_source: P1 + P2 research 2026-10-19 [P1-20][P1-22][P1-9][P1-10][P1-11][P1-29][P2-R2][P2-R7][P2-R10] · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: mechanic_

- **Interest:** $1 per $5 held at cash-out, capped at $5 (money above $25 earns nothing). Interest vouchers raise the cap to $10 and $20; one Joker adds $1 per $5 on top. One deck earns no interest (it pays $2 per remaining hand and $1 per remaining discard), so those do nothing there.
- **Blind rewards:** $3 / $4 / $5 / $8 plus $1 per unused hand.
- **Rerolls:** first reroll in a shop costs $5, each further reroll +$1; resets at the next shop. Two vouchers lower the reroll start to $3 and $1; one Joker gives one free reroll per shop; the D6 Tag starts rerolls at $0. Rerolls replace only the random card slots, never the packs or the voucher.
- **Sell value:** floor(buy cost / 2), minimum $1. Egg adds $3 per round; Gift Card adds $1 per round to every Joker and consumable; one voucher lowers owned Jokers' sell value.
- **Prices:** Common Jokers $1-6, Uncommon $4-8, Rare $7-10; Legendary valued at $20 but never sold in the shop. Tarot and Planet $3, Spectral $4, playing card $1. Packs $4 / $6 / $8 (Normal / Jumbo / Mega). Vouchers $10. Edition surcharges: Foil +$2, Holographic +$3, Polychrome +$5, Negative +$5. Price is (base + edition) x discount, minimum $1; the discount vouchers take 25% and 50% off; the Coupon Tag makes the next shop's cards and packs free (not the voucher).
- **Debt:** money normally floors at $0; Credit Card allows -$20; a few Boss Blind and Joker-sticker charges can push below $0; a few effects set money to $0, which clears debt. Economy Tag and The Hermit do not double debt.

_source: P1 + P2 research 2026-10-19 [P1-20][P1-22][P1-18][P2-R2][P2-R10] · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: item_

**Shop structure.** The shop appears after every blind actually played. It holds 2 random card slots (3 or 4 with the slot vouchers; mostly Jokers), 2 booster packs (restocked every shop) and 1 Voucher (restocks only after a Boss Blind, so in practice one new Voucher per ante, inferred; the Voucher Tag adds an extra). The first shop of a run always has a Normal Buffoon Pack. Card-slot weights: Joker 20 (71.4%), Tarot 4, Planet 4; playing cards weigh 4 only with a playing-card voucher, Spectral 2 only with one deck. Joker rarity on generation: Common 70%, Uncommon 25%, Rare 5%. Some Jokers enter the pool only once the deck has the card type they need (Steel Joker, Stone Joker, Lucky Cat and others need a matching Steel/Stone/Lucky/Gold/Glass card in the deck; Cavendish appears only after Gros Michel has self-destructed that run). If every Joker of a rarity is taken (and no duplicate-allowing Joker is held) further spawns of that rarity become the base Joker card. The weights of the two Tarot-shop vouchers are given as 9.6 and 32 on a base 4; this does not match their own 2x / 4x labels (8 and 16) `[Contradicted across sources -- see notes]`, see `limitations.md`.

_source: P1 + P2 research 2026-10-19 [P1-22][P1-2][P2-R2] · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: structure_

**What is lost when you leave the shop** (limited window): unbought random cards and packs are gone; packs restock in each new shop; an unbought voucher can reappear later. Inferred from the restock rules. [Hypothesis -- unverified]

_source: P1 research 2026-10-19 [P1-22][P1-9][P1-10] · capture: web_fetch · confidence: low · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: mechanic · missable: yes_

**Skip Tags (24).** Tags stack and resolve oldest first; each Tag is equally likely when offered; 15 can appear at Ante 1. Edition Tags and the Rare Tag also need their Joker or edition already discovered. one deck gives a Double Tag after each Boss; selling one Joker gives a Double Tag; several Double Tags give (number of Doubles + 1) copies.

_source: P1 + P2 research 2026-10-19 [P1-15][P2-R6][P2-R10] · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: item_

| Tag | Reward | Min Ante |
|---|---|---|
| Uncommon Tag | next shop has a free Uncommon Joker | 1 |
| Rare Tag | next shop has a free Rare Joker (needs a Rare already discovered) | 1 |
| Negative Tag | next base-edition shop Joker is free and becomes Negative | 2 |
| Foil Tag | same, Foil | 1 |
| Holographic Tag | same, Holographic | 1 |
| Polychrome Tag | same, Polychrome | 1 |
| Investment Tag | $25 after defeating the Boss Blind | 1 |
| Voucher Tag | adds a Voucher to the next shop | 1 |
| Boss Tag | rerolls the Boss Blind | 1 |
| Standard Tag | free Mega Standard Pack | 2 |
| Charm Tag | free Mega Arcana Pack | 1 |
| Meteor Tag | free Mega Celestial Pack | 2 |
| Buffoon Tag | free Mega Buffoon Pack | 2 |
| Handy Tag | $1 per hand played this run | 2 |
| Garbage Tag | $1 per unused discard this run | 2 |
| Ethereal Tag | free Spectral Pack | 2 |
| Coupon Tag | initial cards and packs in the next shop are free | 1 |
| Double Tag | copies the next Tag selected (not another Double Tag) | 1 |
| Juggle Tag | +3 hand size next round | 1 |
| D6 Tag | rerolls in the next shop start at $0 | 1 |
| Top-up Tag | create up to 2 Common Jokers | 2 |
| Speed Tag | $5 per blind skipped this run | 1 |
| Orbital Tag | upgrade one poker hand by 3 levels | 2 |
| Economy Tag | double your money (max +$40) | 1 |

_source: P1 + P2 research 2026-10-19 [P1-15][P2-R6][P2-R10] · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: item_

Skip strategy is disputed: a top-difficulty guide says skip Tags are "almost always useless" except a Round 1 Investment Tag skip or on the Double-Tag deck; another guide values skip-scaling Jokers; an unread guide recommends skipping the first two blinds early. Skipping both blinds in Ante 1 means facing the Boss with no Jokers (search snippet, unread). `[Contradicted across sources -- see notes]` [P1-37][P1-38]

_source: P1 research 2026-10-19 [P1-37][P1-38] · capture: web_fetch · confidence: low · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: build_

Reroll achievement: You Get What You Get (win a run without ever rerolling the shop; any shop reroll ends it for that run; whether Chaos the Clown's free reroll counts was not found).

_source: P1 research 2026-10-19 [P1-4][P1-5] · capture: web_fetch · confidence: high · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: mechanic · missable: yes · achievement: you_get_what_you_get · achievement-hidden: no · trigger_type: mastery_

Money achievement: Nest Egg (hold $400 or more at once in a single run; also unlocks Satellite; money can be rebuilt, so no window closes).

_source: P1 research 2026-10-19 [P1-4][P1-5] · capture: web_fetch · confidence: high · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: mechanic · achievement: nest_egg · achievement-hidden: no · trigger_type: threshold_

> **Cross-system dependency** -- see `dependencies.md` DEP-001: Green Deck pays no interest, so the interest vouchers and To the Moon do nothing there.
> **Cross-system dependency** -- see `dependencies.md` DEP-005: Steel Joker, Stone Joker, Lucky Cat, Golden Ticket and Glass Joker enter the shop pool only once the deck holds a card of their type; the matching Tarots (and Marble Joker for Stone) create one.
> **Cross-system dependency** -- see `dependencies.md` DEP-006: Cavendish appears only after Gros Michel has been destroyed that run.
> **Cross-system dependency** -- see `dependencies.md` DEP-008
> **Cross-system dependency** -- see `dependencies.md` DEP-032: The $400 threshold that clears Nest Egg is also Satellite's unlock condition.

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

## Jokers (rarity, editions, sell value, slots)

150 Jokers: Common 61, Uncommon 64, Rare 20, Legendary 5 (the Chinese wiki tallies 61 / 65 / 19 / 5, machine-counted, low confidence); 105 available from the start and 45 locked. Editions (Foil, Holographic, Polychrome, Negative) and the stake stickers ride on Jokers. Full list, unlock chains and notes: `items/abilities.md`. [P1-1][P1-2][P1-31]

_source: P1 research 2026-10-19 [P1-1][P1-2][P1-28] · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: item_

## Card enhancements, seals and editions on playing cards

See `items/upgrades.md` for the tables. A playing card carries one enhancement, one seal and one edition at once; a new enhancement or seal replaces the old; a debuffed card loses every modifier except Negative and Stone.

## Decks and stakes (difficulty ladder)

15 decks and 8 stakes (plus 20 challenge decks). Deck modifiers and unlocks are in `items/builds.md` (deck table) and the unlock chain below.

_source: P1 + P2 research 2026-10-19 [P1-11][P1-12][P2-R3][P2-R4][P2-R10][P2-R12] · capture: web_fetch · confidence: high · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

**Stakes** (each keeps all earlier stakes' rules):

_source: P1 + P2 research 2026-10-19 [P1-12][P1-29][P2-R4][P2-R10] · capture: web_fetch · confidence: high · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: structure_

| # | Stake | Rule added |
|---|---|---|
| 1 | White | base (first column of the Ante table above; Red uses it too) |
| 2 | Red | Small Blind pays no money |
| 3 | Green | faster score scaling per Ante (second column of the Ante table; Black and Blue use it too) |
| 4 | Black | 30% of shop and pack Jokers may be Eternal (cannot be sold or destroyed) |
| 5 | Blue | -1 discard per round (the 1.1 update plans a rework) |
| 6 | Purple | even faster score scaling (third column of the Ante table; Orange and Gold use it too) |
| 7 | Orange | 30% of Jokers may be Perishable (debuffed after 5 rounds) |
| 8 | Gold | 30% of Jokers may be Rental ($1 to buy, -$3 every round end) |

_source: P1 + P2 research 2026-10-19 [P1-12][P1-29][P2-R4][P2-R10] · capture: web_fetch · confidence: high · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: structure_

Stake unlock chain: each deck starts with White only; winning on a deck's highest unlocked stake unlocks the next stake for that deck only. Winning with any deck at a stake or higher unlocks the decks listed in `items/builds.md`. The Blue Stake effect text fetched from one wiki mixed in the Plasma Deck wording; the -1 discard reading is used (confirmed by the Korean wiki). Before 1.0.1, Orange used "+$1 booster cost per ante" and Gold used "-1 hand size"; the 1.0.1 experimental patch lowered ante scaling on White and Green (patch coverage snippet, not read; hypothesis for the scaling change). The $3 Rental charge is taken before the round payout, so it can lower that round's interest. [P2-R4][P2-R10][P1-20][P1-22]

_source: P1 + P2 research 2026-10-19 [P1-12][P1-29][P2-R4][P2-R10][P1-20][P1-22] · capture: web_fetch · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: structure_

Stake Stickers: a Joker owned when the Ante 8 Showdown is beaten earns that stake's sticker, and so does the deck; only the highest shows and earning one fills lower ones. Jokers sold before the summary screen or bought after Ante 8 get none; debuffed Jokers still do. Profile > Progress tracks 1,200 Joker stickers (150 x 8) and 120 deck stickers (15 x 8). Sticker rules: Eternal and Perishable never combine; Rental can combine with either; on Orange and Gold 40% of Jokers carry neither Eternal nor Perishable; on Gold 28% carry no in-run sticker. Perishable payout Jokers (Golden Joker, Cloud 9, others) effectively last 4 rounds, not 5, because the debuff lands before cash-out. A Rental Gros Michel that dies still charges $3. [P1-29]

_source: P1 research 2026-10-19 [P1-29][P1-12] · capture: web_fetch · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: structure_

Stake achievements: Low Stakes (win on Red Stake or higher; unlocks Zodiac Deck) and Mid Stakes (win on Black Stake or higher; unlocks Anaglyph Deck; needs White, Red and Green wins with the same deck).

_source: P1 research 2026-10-19 [P1-4][P1-12][P2-R4] · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure · achievement: low_stakes, mid_stakes · achievement-hidden: no · trigger_type: mastery, mastery_

> **Cross-system dependency** -- see `dependencies.md` DEP-007
> **Cross-system dependency** -- see `dependencies.md` DEP-022
> **Cross-system dependency** -- see `dependencies.md` DEP-023
> **Cross-system dependency** -- see `dependencies.md` DEP-015: A win on Red Stake or higher unlocks the Zodiac Deck.
> **Cross-system dependency** -- see `dependencies.md` DEP-024: A win on Green Stake or higher unlocks the Painted Deck.
> **Cross-system dependency** -- see `dependencies.md` DEP-025: A win on Black Stake or higher unlocks the Anaglyph Deck.
> **Cross-system dependency** -- see `dependencies.md` DEP-026: A win on Blue Stake or higher unlocks the Plasma Deck.
> **Cross-system dependency** -- see `dependencies.md` DEP-027: A win on Orange Stake or higher unlocks the Erratic Deck.
> **Cross-system dependency** -- see `dependencies.md` DEP-028: Low Stakes is the same Red Stake win as the Zodiac Deck unlock.
> **Cross-system dependency** -- see `dependencies.md` DEP-029: Mid Stakes is the same Black Stake win as the Anaglyph Deck unlock.

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

The top-stake achievement, High Stakes (win on Gold Stake; needs wins on all 7 lower stakes with that deck), is documented here and in `achievements.md`.

_source: P1 research 2026-10-19 [P1-4][P1-12][P2-R4] · capture: web_fetch · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: structure · achievement: high_stakes · achievement-hidden: no · trigger_type: mastery_

## Unlocks, collection and profiles

_source: P1 + P2 research 2026-10-19 [P1-2][P1-6][P1-9][P1-25][P2-R3][P2-R8][P2-R9][P2-R11] · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

- "Unlocked" means eligible to appear; "discovered" means obtained or used in an unseeded run. Seeded runs discover nothing. Buying then quitting to the menu to undo the purchase still discovers the item. Unlock conditions are visible only before unlocking, by hovering a locked card in the Collection (some Steam-thread evidence); whether every locked item shows its condition is `key: unknown` on the sources read.
- The Collection counts 340 items and tracks Jokers, Decks, Vouchers, Tarot, Planet and Spectral cards, Editions, Booster Packs, Tags and Blinds. Enhancements (8) and Seals (4) start discovered. The collection-count deck unlocks (discovered-item thresholds) live in the `items/builds.md` deck table, their one home.
- **Profiles:** 3 slots. Create one from an empty tab (name up to 16 characters); switch via Profile menu > tab > Load Profile; Reset Profile (click twice) wipes the loaded profile; Delete Profile (click twice) empties an unloaded slot. Per profile: Collection discoveries, unlocks, completed challenges, Joker Stake Stickers, deck and stake wins, statistics, achievements. Shared across profiles: settings and deck (card-skin) customisation. "Unlock All" on the profile screen unlocks all 340 Collection items and permanently disables achievements for that profile (two pages agree).
- Progress syncs only between copies from the same store; moving from Apple Arcade "Balatro+" to standard Balatro is supported (Korean wiki). Steam Cloud can re-download a deleted save or overwrite local progress; a 2024-02-27 report describes cloud sync on a PC that had run the demo partly re-locking decks. To keep a restore point, copy the save folder and turn Steam Cloud off.
- Missability: everything can be re-earned on a later run; nothing is permanently missable in the sources read. Within a run, windows close: unbought shop cards and packs, secret Planets (only after their hand is played, only in that run) and skipped pack contents. [Hypothesis -- unverified for the profile-wide claim]

_source: P1 + P2 research 2026-10-19 [P1-2][P1-6][P1-9][P1-25][P2-R3][P2-R8][P2-R9][P2-R11] · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

Collection achievements: Completionist (discover 100% of the collection; one Steam thread frames it as the Joker collection only, `[Contradicted across sources -- see notes]`) and Completionist+ (win with every deck, 15, on Gold Stake; bug: not awarded on the run that earns the final Gold deck sticker, so play one more run on any stake). 100% also needs all 20 challenges (Steam thread).

_source: P1 + P2 research 2026-10-19 [P1-4][P2-R18][P2-R4] · capture: web_fetch · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: structure · achievement: completionist, completionist_plus · achievement-hidden: no · trigger_type: collection, mastery_

Completionist++ (earn a Gold Stake Sticker on all 150 Jokers): each Joker must be held when a Gold Stake Ante 8 Showdown is beaten; lost for that run if the Joker is sold or destroyed first. Legendary Jokers need The Soul during a Gold Stake run (inferred).

_source: P1 + P2 research 2026-10-19 [P1-4][P1-29][P2-R18] · capture: web_fetch · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: structure · missable: yes · achievement: completionist_plus_plus · achievement-hidden: no · trigger_type: mastery_

> **Cross-system dependency** -- see `dependencies.md` SEQ-004: A Joker sold or destroyed before the Gold Stake Ante 8 Showdown is beaten misses its Gold Sticker for that run.
> **Cross-system dependency** -- see `dependencies.md` SEQ-005: Planet X, Ceres and Eris show in the shop only after their secret hand has been played that run.

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: structure_

### Challenges (20) and Challenge Mode

White Stake only. Challenge Mode opens after winning regular runs with 5 different decks (the Dot Esports guide says "five runs using any decks", `[Contradicted across sources -- see notes]`); that opens the first 5 challenges (assumed to be #1-5 in list order), and each new challenge won unlocks one more; 15 wins unlock all 20. Challenge runs grant no achievements or unlocks except Rule Bender and Rule Breaker; statistics still update. Challenges: The Omelette, 15 Minute City, Rich get Richer, On a Knife's Edge, X-ray Vision, Mad World, Luxury Tax, Non-Perishable, Medusa, Double or Nothing, Typecast, Inflation, Bram Poker, Fragile, Monolith, Blast Off, Five-Card Draw, Golden Needle, Cruelty, Jokerless. Short rules: The Omelette (no blind, hand or interest money; 5 Eggs; money vouchers and Jokers banned), 15 Minute City (Eternal Ride the Bus and Shortcut; face-card deck without A, 2, 3), Rich get Richer (chips capped at current $; start with $100, Seed Money, Money Tree), On a Knife's Edge (Eternal pinned Ceremonial Dagger), X-ray Vision (1 in 4 cards face down), Mad World (Eternal Negative Pareidolia and Business Card; ranks 2-9; no hand or interest money), Luxury Tax (-1 hand size per $5 held; base hand size 10), Non-Perishable (all Jokers Eternal), Medusa (Eternal Marble Joker; face cards replaced by Stone), Double or Nothing (all cards Red Seal; played cards debuffed after scoring), Typecast (after Ante 4 boss, Jokers Eternal, Joker slots 0), Inflation (prices +$1 per purchase; Credit Card; Clearance Sale and Liquidation banned), Bram Poker (no Jokers in the shop; Eternal Vampire; The Emperor, The Empress; Magic Trick, Illusion), Fragile (all-Glass deck; 2 Eternal Negative Oops! All 6s), Monolith (Eternal Obelisk; Eternal Negative Marble Joker), Blast Off (2 hands, 2 discards, 4 Joker slots; Eternal Constellation and Rocket; Planet Merchant and Tycoon), Five-Card Draw (6 discards, hand size 5, 7 Joker slots; Card Sharp, Joker), Golden Needle (1 hand, 6 discards costing $1 each; Credit Card), Cruelty (Small and Big Blinds pay nothing; 3 Joker slots), Jokerless (0 Joker slots). The per-challenge unlock order beyond "one per new challenge win" is `key: unknown`. [P1-19][P2-R5][P2-R12]

_source: P1 + P2 research 2026-10-19 [P1-19][P2-R5][P2-R12] · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

Challenge achievements: Rule Bender (complete any one challenge) and Rule Breaker (complete all 20).

_source: P1 research 2026-10-19 [P1-4][P1-19] · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure · achievement: rule_bender, rule_breaker · achievement-hidden: no · trigger_type: mastery, mastery_

## Save, resume and persistence

_source: P2 research 2026-10-19 [P2-R13][P2-R14][P2-R15][P2-R16][P2-R17][P2-R19] · capture: web_fetch · confidence: low · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: mechanic_

- No manual save button. The run auto-saves on quitting or returning to the main menu; returning to the main menu does not end the run, and "Continue" resumes it. To abandon a run, lose it or hold R to restart. (Several forum sources agree; one Joker's unlock condition, "continue a saved run from the main menu", also presupposes it.) [Confirmed: 5 sources, 1 language, per P2; forum class]
- Save checkpoints reported: starting a blind, playing a hand or discarding, opening a booster pack, rerolling. Whether shop purchases are saved is `[Contradicted across sources -- see notes]`: one thread says purchases are saved, another (2024-05) says quitting in the shop reverts them and refunds money; possibly version-dependent.
- Quitting while a hand is scoring restores the state before that hand. Random outcomes are fixed in the save (a Wheel of Fortune result does not change on reload, but a different pack card can be picked) -- single forum source; the Reddit thread was unreachable.
- Exploit status: players call it an exploit; no developer statement was read. A search snippet says the developer patched a pack-peeking trick and an earlier free-reroll-on-continue bug (itch.io posts, not read) [Hypothesis -- unverified]. Quitting during some actions (mainly opening a pack gained by skipping a blind) can softlock the run.
- Windows save files: `%AppData%\Roaming\Balatro\<1|2|3>\` (the number is the profile slot). `save.jkr` is the current run, `profile.jkr` holds per-profile progress including per-deck win counts; `meta.jkr` is undocumented (`key: unknown`). Deleting `save.jkr` loses the run; what else survives is `[Contradicted across sources -- see notes]`.
- Hubs: no fast travel. The main menu (reached from the in-run options menu), the Collection (from the main menu or the in-run options menu), the Challenges entry in the New Run menu (once unlocked), and the Profile menu (from the main menu) are the only hubs. Hold R restarts the run.

_source: P2 research 2026-10-19 [P2-R13][P2-R14][P2-R15][P2-R16][P2-R17][P2-R19] · capture: web_fetch · confidence: low · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: mechanic_

## Endless mode and run end conditions

Winning the Ante 8 Showdown wins the run; continuing into Endless Mode is a choice. Endless starts at Ante 9; Showdown bosses recur at Antes 16, 24 and 32; requirements grow faster than exponentially. Score display tops out near 1.7e308 and shows "naneinf". At Ante 39 the requirement exceeds float range and is NaN, so no score beats it: Ante 39 is the effective ceiling. One wiki frames reaching Ante 39 as completing Endless; the Korean wiki says Ante 38 is the practical end and Ante 39 is always a game over. `[Contradicted across sources -- see notes]` The in-game collection shows ante bases only to Ante 16. Hieroglyph or Petroglyph can push the ante to 0 or below (base 100); Ante -1 needs both vouchers in reach plus Yellow Deck money, a Voucher Tag and fast buying at slow game speed (a glitch-style technique). Petroglyph itself unlocks by reaching Ante 12.

_source: P1 + P2 research 2026-10-19 [P1-13][P1-14][P2-R1][P2-R10] · capture: web_fetch · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: structure_

Endless base requirements (base / faster / fastest scaling columns; the English wiki's closed-form formula does not reproduce its own table, so the table is authoritative): Ante 9: 110,000 / 230,000 / 460,000; 10: 560,000 / 1.1M / 2.2M; 11: 7.2e6 / 1.4e7 / 2.9e7; 12: 3.0e8 / 6.0e8 / 1.2e9; 13: 4.7e10 / 9.4e10 / 1.8e11; 14: 2.9e13 / 5.8e13 / 1.1e14; 15: 7.7e16 / 1.5e17 / 3.0e17; 16 (Showdown): 8.6e20 / 1.7e21 / 3.4e21; 24 (Showdown): 1.6e77 / 3.3e77 / 6.6e77; 32 (Showdown): 2.7e179 / 5.4e179 / 1.0e180; 39: 4.8e309 (naneinf).

_source: P1 + P2 research 2026-10-19 [P1-13][P2-R1][P2-R10] · capture: web_fetch · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: mechanic_

## Sources

P1 (balatro_p1.result.md): P1-1 https://balatrowiki.org/w/Jokers · P1-2 https://balatrogame.fandom.com/wiki/Jokers · P1-3 https://steamcommunity.com/achievements/2379780 · P1-4 https://balatrowiki.org/w/Achievements · P1-5 https://www.trueachievements.com/game/Balatro/achievements · P1-6 https://balatrowiki.org/w/Tarot_Cards · P1-7 https://balatrowiki.org/w/Planet_Cards · P1-9 https://balatrowiki.org/w/Vouchers · P1-10 https://balatrogame.fandom.com/wiki/Vouchers · P1-11 https://balatrowiki.org/w/Decks · P1-12 https://balatrowiki.org/w/Stakes · P1-13 https://balatrowiki.org/w/Blinds_and_Antes · P1-14 https://balatrogame.fandom.com/wiki/Blinds_and_Antes · P1-15 https://balatrowiki.org/w/Tags · P1-17 https://balatrowiki.org/w/Poker_Hands · P1-18 https://balatrowiki.org/w/Card_Modifiers · P1-19 https://balatrowiki.org/w/Challenges · P1-20 https://balatrowiki.org/w/Money · P1-21 https://balatrowiki.org/w/Scoring · P1-22 https://balatrowiki.org/w/The_Shop · P1-25 https://balatrowiki.org/w/Settings · P1-26 https://steamdb.info/app/2379780/patchnotes/ · P1-27 https://godisageek.com/2026/09/balatro-1-1-update-new-jokers-lunker/ · P1-28 https://store.steampowered.com/app/2379780/Balatro/ · P1-29 https://balatrogame.fandom.com/wiki/Stickers · P1-31 https://wiki.biligame.com/balatro/小丑牌 (zh-Hans) · P1-35 https://www.reddit.com/r/balatro/comments/1jhqi23/a_question_for_the_ages/ (2025-03-23) · P1-36 https://steamcommunity.com/app/2379780/discussions/0/604155219069118124 (2025-05-03) · P1-37 https://www.twoaveragegamers.com/balatro-strategy-guide-the-joker-combos-that-actually-win-runs/ (2026-01-29) · P1-38 https://mancunion.com/2025/09/01/a-guide-to-gold-stake-balatro/ (2025-09-01).

P2 (balatro_p2.result.md): P2-R1 https://balatrowiki.org/w/Blinds_and_Antes · P2-R2 https://balatrowiki.org/w/Shop · P2-R3 https://balatrowiki.org/w/Unlocks · P2-R4 https://balatrowiki.org/w/Stakes · P2-R5 https://balatrowiki.org/w/Challenges · P2-R6 https://balatrowiki.org/w/Tags · P2-R7 https://balatrowiki.org/w/Money · P2-R8 https://balatrowiki.org/w/Collection · P2-R9 https://balatrowiki.org/w/Profile · P2-R10 https://namu.wiki/w/Balatro (ko, modified 2026-10-06) · P2-R11 https://primagames.com/gaming/how-to-unlock-everything-in-balatro-jokers-decks-vouchers-and-more (2024-02-20) · P2-R12 https://dotesports.com/indies/news/balatro-deck-list-how-to-unlock (2025-12-18) · P2-R13 https://steamcommunity.com/app/2379780/discussions/0/4329726622428319721 · P2-R14 https://steamcommunity.com/app/2379780/discussions/0/6589424052366037244 · P2-R15 https://steamcommunity.com/app/2379780/discussions/0/4346606879508568602 · P2-R16 https://steamcommunity.com/app/2379780/discussions/0/4365754355272937675 · P2-R17 https://steamcommunity.com/app/2379780/discussions/0/4308326918573418851 · P2-R18 https://steamcommunity.com/app/2379780/discussions/0/604143165271744486 · P2-R19 https://www.reddit.com/r/balatro/comments/1i1mxw6/confession_i_save_scum/ · P2-R20 https://api.steampowered.com/ISteamNews/GetNewsForApp/v2/?appid=2379780&count=15&maxlength=300 · P2-R21 https://steamdb.info/app/2379780/patchnotes/.
