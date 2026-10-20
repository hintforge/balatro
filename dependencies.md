# Dependencies -- Balatro

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-10-20

<!-- hintforge · stitch pass · last run: 2026-10-20 -->
<!-- Every stitch run re-audits ALL existing edges + adds new ones. The per-edge convergence audit (open each cited source, verify the specific value) applies to every row in this file on every run, not just new candidates. A game patch, DLC, or new ingestion phase can change facts that existing edges cite -- only a full re-audit catches that. See `stitch_and_zipper.md` Phase B "Re-run scope: always full." Inconsistencies (cited source contradicts edge text) land in the `## Corpus inconsistencies` section; the edge row stays in place. -->

Balatro is a procedural roguelike with no permanent lockouts documented (every window below closes inside one run and can be retried), so the PoNR table is empty and run-scoped windows sit in the Missable / sequencing table. Version note: facts describe the 1.0.1 line; update 1.1 is unreleased. Each table below is one spoiler tier (its tag sits on the line below it), set by the highest-tier item any row in it names; every row also carries that tier in its `tier` column.

## Cross-system edges

Edges that name only items available from the start:

_source: stitch pass 2026-10-19, derived from the corpus files each row cites · capture: derived · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: structure_

| Edge ID | System A | System B | Dependency description | Confidence | tier | Source files |
|---------|----------|----------|------------------------|------------|------|--------------|
| DEP-004 | Scoring order (on-scored effects resolve during card scoring; independent Joker effects resolve left to right) | Joker placement advice (xMult on the right) | Only independent Joker effects depend on position; on-scored xMult Jokers such as Photograph resolve before any independent Joker, so moving them right changes nothing unless another on-scored Joker interacts. | medium | none | mechanics.md, items/builds.md, items/abilities.md |
| DEP-006 | Gros Michel (1 in 6 chance to be destroyed each round end) | Cavendish (X3 Mult; shop spawn) | Cavendish appears in the shop only after Gros Michel has been destroyed in that run. | high | none | mechanics.md, items/abilities.md |
| DEP-009 | Midas Mask (scored face cards become Gold) | Vampire (strips enhancements for X Mult) | Midas Mask to the left of Vampire feeds Vampire's scaling; to the right, the Gold cards stay in the deck. | medium | none | mechanics.md, items/abilities.md |
| DEP-010 | Scoring step 4 (held-in-hand effects: Steel X1.5, then held Jokers, then held retriggers) | Baron plus Mime with Steel and Red Seal Kings | Baron's per-held-King xMult, Mime's held retrigger, Steel's X1.5 and the Red Seal retrigger all resolve in the held-in-hand step, which is why the Kings build stacks. | medium | none | mechanics.md, items/abilities.md, items/upgrades.md, items/builds.md |

_source: stitch pass 2026-10-19, derived from the corpus files each row cites · capture: derived · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: structure_

Edges that name locked Jokers, regular Boss Blinds, locked decks or vouchers, stakes or progression achievements:

_source: stitch pass 2026-10-19, derived from the corpus files each row cites · capture: derived · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

| Edge ID | System A | System B | Dependency description | Confidence | tier | Source files |
|---------|----------|----------|------------------------|------------|------|--------------|
| DEP-001 | Green Deck (no interest) | Interest economy: Seed Money, Money Tree, To the Moon | Green Deck pays no interest (it pays $2 per remaining hand and $1 per remaining discard), so the interest-cap vouchers and To the Moon do nothing there. | high | progression | mechanics.md, items/builds.md, items/abilities.md, items/upgrades.md |
| DEP-002 | Boss Blind The Hook (discards 2 random held cards after each hand) | Mail-In Rebate (pays per discarded card of the target rank) | The Hook's forced discards count for Mail-In Rebate. | medium | progression | mechanics.md, items/abilities.md |
| DEP-018 | Boss Blind The Hook (discards 2 random held cards after each hand) | Castle (gains Chips per discarded card of the target suit) | The Hook's forced discards count for Castle. | medium | progression | mechanics.md, items/abilities.md |
| DEP-019 | Boss Blind The Hook (discards 2 random held cards after each hand) | Hit the Road (gains Mult per Jack discarded) | The Hook's forced discards count for Hit the Road when a Jack is among them. | medium | progression | mechanics.md, items/abilities.md |
| DEP-020 | Boss Blind The Hook (discards 2 random held cards after each hand) | Green Joker (-1 Mult per discard) | The Hook's forced discards work against Green Joker (-1 per discard). | medium | progression | mechanics.md, items/abilities.md |
| DEP-021 | Boss Blind The Hook (discards 2 random held cards after each hand) | Ramen (loses X per card discarded) | The Hook's forced discards work against Ramen (it loses X per card discarded). | medium | progression | mechanics.md, items/abilities.md |
| DEP-005 | Deck-card-type Jokers: Steel Joker, Stone Joker, Lucky Cat, Golden Ticket, Glass Joker | Card sources: Tarots The Chariot (Steel), The Tower (Stone), The Magician (Lucky), The Devil (Gold), Justice (Glass); Marble Joker (adds Stone) | These Jokers enter the shop pool only once the deck holds a card of their type, and the Tarots (and Marble Joker for Stone) are the in-run way to create one. | medium | progression | mechanics.md, items/abilities.md, items/consumables.md |
| DEP-013 | Suit-debuff Boss Blinds: The Club, The Goad, The Window, The Head | Mono-suit builds (The Star, The Moon, The Sun, The World, Sigil, Checkered Deck, Smeared Joker) | Narrowing the deck to one suit leaves it exposed to the matching suit-debuff boss; with Smeared Joker each suit boss hits half the deck (inferred). | medium | progression | mechanics.md, items/builds.md, items/consumables.md |
| DEP-014 | Plasma Deck (blind requirements doubled; Chips and Mult balanced at the end of scoring) | Chips versus xMult build choice | Because Plasma balances Chips and Mult after every Joker, Chips matter as much as Mult there, and the doubled requirement applies to every blind. | medium | progression | mechanics.md, items/builds.md |
| DEP-015 | Stake win on Red Stake or higher (each stake keeps all earlier rules; a deck starts at White only) | Zodiac Deck unlock | A win on Red Stake or higher unlocks the Zodiac Deck. | high | progression | mechanics.md, items/builds.md |
| DEP-024 | Stake win on Green Stake or higher | Painted Deck unlock | A win on Green Stake or higher unlocks the Painted Deck. | high | progression | mechanics.md, items/builds.md |
| DEP-025 | Stake win on Black Stake or higher | Anaglyph Deck unlock | A win on Black Stake or higher unlocks the Anaglyph Deck. | high | progression | mechanics.md, items/builds.md |
| DEP-026 | Stake win on Blue Stake or higher | Plasma Deck unlock | A win on Blue Stake or higher unlocks the Plasma Deck. | high | progression | mechanics.md, items/builds.md |
| DEP-027 | Stake win on Orange Stake or higher | Erratic Deck unlock | A win on Orange Stake or higher unlocks the Erratic Deck. | high | progression | mechanics.md, items/builds.md |
| DEP-028 | Stake win on Red Stake or higher | Low Stakes achievement | The Low Stakes achievement is the same Red Stake win as the Zodiac Deck unlock. | high | progression | mechanics.md, achievements.md |
| DEP-029 | Stake win on Black Stake or higher | Mid Stakes achievement | The Mid Stakes achievement is the same Black Stake win as the Anaglyph Deck unlock, and it needs White, Red and Green wins with the same deck first. | high | progression | mechanics.md, achievements.md |
| DEP-016 | Boss Blind The Arm (lowers the played hand's level by 1, minimum 1) | Hand levels and the Retrograde achievement (any hand to level 10) | The Arm resolves first in scoring and lowers the played hand's level, working against Planet-driven leveling toward level 10. | medium | progression | mechanics.md, items/upgrades.md, achievements.md |
| DEP-017 | Run milestone: reach Ante 4 | Showman Joker unlock and the Ante Up! achievement | Reaching Ante 4 clears the Showman unlock and the Ante Up! achievement with the same trigger. | high | progression | mechanics.md, items/abilities.md, achievements.md |
| DEP-030 | Run milestone: reach Ante 8 | Flower Pot Joker unlock and the Ante Upper! achievement | Reaching Ante 8 clears the Flower Pot unlock and the Ante Upper! achievement with the same trigger. | high | progression | mechanics.md, items/abilities.md, achievements.md |
| DEP-031 | Run milestone: first run won | Blueprint Joker unlock and the Heads Up achievement | The first win clears the Blueprint unlock and the Heads Up achievement with the same trigger. | high | progression | mechanics.md, items/abilities.md, achievements.md |
| DEP-032 | Nest Egg achievement (hold $400 or more at once in a run) | Satellite Joker unlock | The $400 threshold that clears Nest Egg is also Satellite's unlock condition. | medium | progression | mechanics.md, items/abilities.md, achievements.md |
| DEP-033 | 10K achievement (score 10,000+ Chips in one hand) | Oops! All 6s unlock | The 10,000-chip hand that clears 10K is also Oops! All 6s's unlock condition. | medium | progression | mechanics.md, items/abilities.md, achievements.md |
| DEP-034 | 1,000K achievement (score 1,000,000+ Chips in one hand) | The Idol unlock | The 1,000,000-chip hand that clears 1,000K is also The Idol's unlock condition. | medium | progression | mechanics.md, items/abilities.md, achievements.md |
| DEP-036 | Astronomy achievement (discover all 12 Planets, secret ones included) | Astronomer unlock | Discovering every Planet clears Astronomy and is also Astronomer's unlock condition. | medium | progression | items/consumables.md, items/abilities.md, achievements.md |
| DEP-037 | Cartomancy achievement (discover all 22 Tarots) | Cartomancer unlock | Discovering every Tarot clears Cartomancy and is also Cartomancer's unlock condition. | medium | progression | items/consumables.md, items/abilities.md, achievements.md |
| DEP-038 | Card Player achievement (play 2,500 cards in total across runs) | Nacho Tong voucher unlock | The 2,500-card play total that clears Card Player is also the Nacho Tong unlock threshold. | medium | progression | items/upgrades.md, achievements.md |
| DEP-039 | Card Discarder achievement (discard 2,500 cards in total across runs) | Recyclomancy voucher unlock | The 2,500-card discard total that clears Card Discarder is also the Recyclomancy unlock threshold. | medium | progression | items/upgrades.md, achievements.md |

_source: stitch pass 2026-10-19, derived from the corpus files each row cites · capture: derived · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

Edges that name Legendary Jokers, Showdown bosses, late-game vouchers or achievements, or the Eternal and Rental sticker rules attached to the Black and Gold Stakes:

_source: stitch pass 2026-10-19, derived from the corpus files each row cites · capture: derived · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: structure_

| Edge ID | System A | System B | Dependency description | Confidence | tier | Source files |
|---------|----------|----------|------------------------|------------|------|--------------|
| DEP-003 | Joker counters: Luchador (sell) and Chicot | Boss Blind effects, including the 4x The Wall and 6x Violet Vessel multipliers | Disabling a Boss Blind (Chicot, Luchador) returns The Wall and Violet Vessel to 2x; selling Luchador while a Wall or Vessel target sits above 2x wins the blind instantly. | medium | late-game | mechanics.md, items/abilities.md |
| DEP-011 | Observatory (held Planets give X1.5 Mult) | Perkeo (Negative copy of a random held consumable) | Planets kept in the consumable slots score under Observatory, and Perkeo duplicates a held consumable at the end of each shop. | low | late-game | mechanics.md, items/upgrades.md, items/abilities.md, items/builds.md |
| DEP-012 | Ante-lowering vouchers Hieroglyph (-1 Ante, -1 hand) and Petroglyph (-1 Ante, -1 discard) | Showdown boss assignment and Ante 8 timing | Lowering the ante can push it to 0 or below; dropping from Ante 8 to Ante 7 does not change an already-assigned Showdown blind; Petroglyph itself unlocks only at Ante 12. | medium | late-game | mechanics.md, items/upgrades.md |
| DEP-007 | Eternal sticker (30% of shop and pack Jokers on Black Stake and above; cannot be sold or destroyed) | Destroy effects: Hex, Ankh | Eternal Jokers are not destroyed by Hex or Ankh. | medium | late-game | mechanics.md, items/consumables.md |
| DEP-022 | Eternal sticker (30% of shop and pack Jokers on Black Stake and above; cannot be sold or destroyed) | Ceremonial Dagger (destroys the Joker to its right) | An Eternal neighbour stops Ceremonial Dagger from scoring. | medium | late-game | mechanics.md, items/abilities.md |
| DEP-023 | Eternal sticker (30% of shop and pack Jokers on Black Stake and above; cannot be sold or destroyed) | Madness (destroys a random Joker on Small and Big blind select) | Madness scales without losses when every Joker is Eternal. | medium | late-game | mechanics.md, items/abilities.md, items/builds.md |
| DEP-008 | Rental sticker (Gold Stake: $1 to buy, -$3 each round end, sells for $1) | Buy-and-sell Jokers: Chaos the Clown, Campfire | A Rental Joker bought and sold within one round costs nothing net, which makes Chaos the Clown and the Campfire scaling cheap Rental targets on Gold Stake. | low | late-game | mechanics.md, items/abilities.md, items/builds.md |
| DEP-035 | 100,000K achievement (score 100,000,000+ Chips in one hand) | Stuntman unlock | The 100,000,000-chip hand that clears 100,000K is also Stuntman's unlock condition. | medium | late-game | mechanics.md, items/abilities.md, achievements.md |

_source: stitch pass 2026-10-19, derived from the corpus files each row cites · capture: derived · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: structure_

### Optional cluster links

Each independently testable relationship gets its own DEP row and audit. A genuinely indivisible relationship stays one row. When several rows describe facets of one cluster, the Cross-system edges table may add `Related DEP(s)` after Source files; list only DEP IDs that exist in this file. The default six-column table remains valid, and existing guides require no migration. A shared name alone does not justify a relationship.

## PoNR / lockout edges

| Edge ID | Trigger | Locked out | Notes | tier | Source files |
|---------|---------|------------|-------|------|--------------|

No permanent lockouts are documented in the sources read (negative claim, unverified); every window is run-scoped, see the next section.

## Missable / sequencing dependencies

Windows that name locked Jokers, vouchers, secret hands or progression achievements:

_source: stitch pass 2026-10-19, derived from the corpus files each row cites · capture: derived · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

| Edge ID | Action | Window | Consequence | tier | Source files |
|---------|--------|--------|-------------|------|--------------|
| SEQ-001 | Playing a 13th round (or a 19th for Wee Joker) in a run | Speedrunner and Merry Andy need a win in 12 or fewer rounds; Wee Joker needs 18 or fewer; the game counts blinds played and a full non-skipping win is 24 rounds | Skipping Small and Big Blinds for Tags is the only way under the limit (inferred for 12: at least 12 of 16 skipped); once the limit is passed the achievement and the Joker unlock are lost for that run | progression | mechanics.md, items/abilities.md, sections/missables.md, achievements.md |
| SEQ-002 | Playing a Pair, Three of a Kind, Four of a Kind, Straight or Flush in a run | The Duo, The Trio, The Family, The Order and The Tribe each need a win without ever playing their hand type | The first time that hand is played, that Joker's unlock is lost for the run; the payoff Joker of a hand-type build is locked behind avoiding that hand | progression | items/abilities.md, sections/missables.md, items/builds.md |
| SEQ-003 | Buying vouchers during Antes 1 to 4 (Voucher slot restocks only after a Boss Blind; the Voucher Tag adds one) | ROI needs 5 vouchers bought by the end of Ante 4; vouchers a deck starts with (Magic, Nebula, Zodiac) do not count | When Ante 4 ends the window closes for that run | progression | items/upgrades.md, mechanics.md, sections/missables.md, achievements.md |
| SEQ-005 | Playing a secret hand (Five of a Kind, Flush House, Flush Five) | Planet X, Ceres and Eris show in the shop only after their hand has been played, and only for the rest of that run | Astronomy (discover all 12 Planets) needs the secret hands played first; a new run needs the hand played again | progression | items/consumables.md, mechanics.md, sections/missables.md, achievements.md |

_source: stitch pass 2026-10-19, derived from the corpus files each row cites · capture: derived · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

Windows that name late-game achievements:

_source: stitch pass 2026-10-19, derived from the corpus files each row cites · capture: derived · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: structure_

| Edge ID | Action | Window | Consequence | tier | Source files |
|---------|--------|--------|-------------|------|--------------|
| SEQ-004 | Selling or destroying a Joker before the Gold Stake Ante 8 Showdown is beaten (or buying one after Ante 8) | Completionist++ needs each of the 150 Jokers held when a Gold Stake Showdown is beaten | That Joker's Gold Sticker is not earned for the run; the settings option that shows stake stickers in-run tracks it | late-game | mechanics.md, sections/missables.md, achievements.md, settings.md |

_source: stitch pass 2026-10-19, derived from the corpus files each row cites · capture: derived · confidence: medium · enemy-tier: 2 · puzzle-tier: 2 · category: mainline · spoiler: late-game · vector: structure_

## Stitch run log

| Date | Scope | Edges written | Edges proposed (pending) | Inconsistencies surfaced | Model |
|------|-------|---------------|--------------------------|--------------------------|-------|
| 2026-10-19 | full | 22 | 0 | 1 (resolved in 5b) | sonnet-class |
| 2026-10-19 | doctor Branch C repair: DEP-002, DEP-007, DEP-015, DEP-017 split into one ID per link (+14 DEP, now 31 DEP + 5 SEQ = 36) | 14 | 0 | 0 | sonnet-class |
| 2026-10-20 | full (36 existing edges re-audited against their cited files; 8 new edges added; `tier` column added to every table) | 8 | 0 | 0 | sonnet-class |

<!-- Inconsistencies surfaced: count from the per-edge convergence audit (stitch_and_zipper.md Phase B). Counts must be derived by reading this file, not recalled. A non-zero count requires an explicit chat call-out and, in the Corpus inconsistencies section below, either at least one populated row (inconsistencies still open) or, when every one was resolved in stitch step 5b and its row removed, the cell written as `N (resolved in 5b)`. -->

## Corpus inconsistencies

Stitch's per-edge convergence audit (see [`stitch_and_zipper.md`](https://github.com/hintforge/builder/blob/main/stitch_and_zipper.md) Phase B) populates this section when a candidate edge's cited sources contradict each other. Each row records the contradiction; resolving it is the user's call (or a follow-up doctor / ingestion run). Edges blocked on an unresolved entry are NOT written to the tables above until the inconsistency is closed.

| Detected | Files | Conflicting values | Suspected authoritative source | Status |
|----------|-------|--------------------|--------------------------------|--------|

<!-- Status vocabulary: open (just surfaced) | resolved (user picked authoritative value + corrected the other file) | accepted (user accepted both -- rare; usually means the claim is genuinely ambiguous in-game). When status flips to resolved, the next stitch run can re-evaluate the edge. -->
<!-- One inconsistency was surfaced and resolved in the 2026-10-19 run (5b): mechanics.md "Shop structure" named two Jokers by shortened names; items/abilities.md (authoritative) corrected the mechanics.md line. Propagation grep for the old wording found no other match. -->
