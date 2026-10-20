# Items -- Upgrades (Vouchers, enhancements, seals, editions)

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-10-20

Permanent and semi-permanent run upgrades: Vouchers (32, in 16 base and upgrade pairs), playing-card enhancements (8), seals (4), editions (4 plus base) and planet-driven hand levels. Page references: `P1-n` and `P2-Rn` resolve in the Sources list at the foot.

## Vouchers (expected 32, located 32)

Every voucher costs $10. Base vouchers are all available from the start; upgrades are locked by a condition. Two sources agree on every condition below except as noted: balatrowiki (P1-9, P2-R3) and a launch-day Prima Games list (P2-R11), with the Fandom wiki (P1-10) for effects.

_source: P1 + P2 research 2026-10-19 [P1-9][P1-10][P2-R3][P2-R11] · capture: web_fetch · confidence: high · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: item_

| Base voucher | Effect | Upgrade | Effect | Upgrade unlock condition |
|---|---|---|---|---|
| Overstock | +1 shop card slot | Overstock Plus | +1 more slot; refills empty slots when bought | spend $2,500 total in shops |
| Clearance Sale | 25% off cards and packs | Liquidation | 50% off; lowers owned Jokers' sell value | redeem 10 vouchers in one run |
| Hone | Foil, Holographic and Polychrome 2x as often (Polychrome on Jokers actually 3x) | Glow Up | 4x as often (Polychrome actually 7x) | own 5+ Jokers with Foil, Holographic, Polychrome or Negative |
| Reroll Surplus | rerolls $2 cheaper | Reroll Glut | another $2 cheaper | reroll 100 times total |
| Crystal Ball | +1 consumable slot | Omen Globe | Spectrals can appear in Arcana Packs (20% per card) | use 25 Tarots from packs |
| Telescope | Celestial Packs always include your most-played hand's Planet (ties go to the higher-tier hand) | Observatory | held Planets give X1.5 Mult for their hand | use 25 Planets from packs |
| Grabber | +1 hand per round | Nacho Tong | +1 more hand | play 2,500 cards total |
| Wasteful | +1 discard per round | Recyclomancy | +1 more discard | discard 2,500 cards total |
| Tarot Merchant | Tarots 2x more often in the shop | Tarot Tycoon | 4x | buy 50 Tarots from the shop |
| Planet Merchant | Planets 2x | Planet Tycoon | 4x | buy 50 Planets from the shop |
| Seed Money | interest cap $10 | Money Tree | interest cap $20 | max out interest 10 rounds in a row |
| Blank | does nothing | Antimatter | +1 Joker slot | redeem Blank 10 times total |
| Magic Trick | playing cards sold in the shop | Illusion | shop playing cards can have an enhancement, edition and/or seal | buy 20 playing cards from the shop |
| Hieroglyph | -1 Ante, -1 hand per round | Petroglyph | -1 Ante, -1 discard per round | reach Ante 12 (late-game) |
| Director's Cut | reroll the Boss once per Ante ($10) | Retcon | unlimited Boss rerolls ($10 each) | discover 25 Blinds |
| Paint Brush | +1 hand size | Palette | +1 more hand size | reduce your hand size to 5 cards |

_source: P1 + P2 research 2026-10-19 [P1-9][P1-10][P2-R3][P2-R11] · capture: web_fetch · confidence: high · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: item_

- Prima's launch-day list names Illusion "Electromagnet", Palette "Tesselation" and Nacho Tong "Nano Tong", gives two vouchers the effect text of their base vouchers; treat Prima's voucher names as obsolete (pre-release). `[Contradicted across sources -- see notes]` The Palette condition came from the Fandom wiki and P2's balatrowiki read, which now agree.
- Voucher unlock chain: an upgrade can appear only if its condition has been met on the profile and its base voucher was redeemed earlier in the same run. Every voucher has an equal chance per draw. The shop's voucher slot restocks after each Boss Blind; the Voucher Tag adds an extra voucher; an unbought voucher may come back; once every unlocked voucher has been seen or bought, only the blank voucher appears. Antimatter is displayed with the Negative edition.
- Illusion bug (v1.0.1o-FULL): shop playing cards from Illusion never get seals, and the two playing-card edition vouchers do not affect them. [Single source -- verify]. Discount-voucher prices round half down.
- Update 1.1 plans an "N-in-16" rule for upgrade appearances; today's rule is 1-in-16 per upgrade (out of scope).
- Visibility of locked vouchers before the key is met is `key: unknown` (placeholder shown is a hypothesis).

_source: P1 + P2 research 2026-10-19 [P1-9][P1-10][P2-R3][P2-R11] · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: item_

Achievement: Extreme Couponer (discover all 32 vouchers; needs every upgrade condition above, e.g. Petroglyph needs Ante 12, Retcon needs 25 Blinds).

_source: P1 + P2 research 2026-10-19 [P1-4][P1-9] · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: item · achievement: extreme_couponer · achievement-hidden: no · trigger_type: collection_

Achievement: ROI (buy 5 vouchers by the end of Ante 4; vouchers a deck starts with, Magic, Nebula and Zodiac, do not count). The window closes when Ante 4 ends.

_source: P1 research 2026-10-19 [P1-4] · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: item · missable: yes · achievement: roi · achievement-hidden: no · trigger_type: threshold_

> **Cross-system dependency** -- see `dependencies.md` DEP-001: Green Deck pays no interest, so the interest vouchers and To the Moon do nothing there.
> **Cross-system dependency** -- see `dependencies.md` DEP-011
> **Cross-system dependency** -- see `dependencies.md` DEP-012
> **Cross-system dependency** -- see `dependencies.md` SEQ-003: ROI's five-voucher window closes when Ante 4 ends.
> **Cross-system dependency** -- see `dependencies.md` DEP-038: The 2,500-card play total that clears Card Player is also the Nacho Tong unlock threshold.
> **Cross-system dependency** -- see `dependencies.md` DEP-039: The 2,500-card discard total that clears Card Discarder is also the Recyclomancy unlock threshold.

_source: stitch pass 2026-10-20, derived from the dependencies.md rows these lines cite · capture: derived · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression · vector: structure_

Achievements tied to the two cumulative-card vouchers: Card Player (play 2,500 cards in total across runs; the same threshold as one voucher's unlock) and Card Discarder (discard 2,500 cards in total; the same as the other voucher's unlock). The two unlocks are in the Vouchers table above.

_source: P1 research 2026-10-19 [P1-4][P1-9] · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: item · achievement: card_player, card_discarder · achievement-hidden: no · trigger_type: threshold, threshold_

## Enhancements (8), Seals (4), Editions (4 + base)

| Kind | Name | Effect |
|---|---|---|
| Enhancement | Bonus | +30 Chips |
| Enhancement | Mult | +4 Mult |
| Enhancement | Wild | counts as every suit (reverts to its base suit when debuffed) |
| Enhancement | Glass | X2 Mult; 1 in 4 chance to shatter when scored |
| Enhancement | Steel | X1.5 Mult while held in hand |
| Enhancement | Stone | +50 Chips; no rank or suit; always scores |
| Enhancement | Gold | $3 if held at end of round |
| Enhancement | Lucky | 1 in 5 chance of +20 Mult; 1 in 15 chance of $20 |
| Seal | Gold | $3 when scored |
| Seal | Red | retriggers the card once |
| Seal | Blue | creates the Planet for the final hand of the round if held |
| Seal | Purple | creates a Tarot when discarded |
| Edition | Foil | +50 Chips (+$2 price) |
| Edition | Holographic | +10 Mult (+$3) |
| Edition | Polychrome | X1.5 Mult (+$5) |
| Edition | Negative | +1 Joker slot (Jokers) or +1 consumable slot; never on playing cards (+$5) |

_source: P1 research 2026-10-19 [P1-18] · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: item_

- A playing card can carry one enhancement, one seal and one edition at once. A new enhancement or seal replaces the old; editions and stickers cannot be changed. A debuffed card loses every modifier except Negative and Stone. DNA and one late-game Spectral card copy every modifier; one more Spectral card and one locked Joker copy the edition (except Negative) and the stickers.
- Base Joker edition odds in the shop: Foil 2%, Holographic 1.4%, Polychrome 0.3%, Negative 0.3%. Playing-card edition chance is 1.2% base, 2.4% and 4.8% with the two edition vouchers.

Achievement: Shattered (break 2 Glass cards in a single hand; Glass cards come from Justice or packs).

_source: P1 research 2026-10-19 [P1-4][P1-18] · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: item · achievement: shattered · achievement-hidden: no · trigger_type: mastery_

Deck-size achievements: Tiny Hands (thin the deck to 20 or fewer cards; removal via The Hanged Man, Trading Card, Glass breaks) and Big Hands (have 80 or more cards in the deck; additions via DNA, Marble Joker, Standard Packs).

_source: P1 research 2026-10-19 [P1-4][P1-5] · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: item · achievement: tiny_hands, big_hands · achievement-hidden: no · trigger_type: threshold, threshold_

> **Cross-system dependency** -- see `dependencies.md` DEP-010: the Red Seal retrigger and Steel's X1.5 resolve in the held-in-hand step with Baron and Mime.

## Hand levels

Levels come from Planets, Space Joker, the Orbital Tag (+3 levels) and the Blue Seal. One boss's effect lowers them. Reaching level 10 on any hand gives Retrograde (see `mechanics.md`). Per-hand base values are in `mechanics.md`.

_source: P1 research 2026-10-19 [P1-7][P1-8][P1-1][P1-15][P1-14] · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none · vector: item_

> **Cross-system dependency** -- see `dependencies.md` DEP-016

## Sources

P1-1 https://balatrowiki.org/w/Jokers · P1-4 https://balatrowiki.org/w/Achievements · P1-5 https://www.trueachievements.com/game/Balatro/achievements · P1-7 https://balatrowiki.org/w/Planet_Cards · P1-8 https://balatrowiki.org/w/Spectral_Cards · P1-9 https://balatrowiki.org/w/Vouchers · P1-10 https://balatrogame.fandom.com/wiki/Vouchers · P1-14 https://balatrogame.fandom.com/wiki/Blinds_and_Antes · P1-15 https://balatrowiki.org/w/Tags · P1-18 https://balatrowiki.org/w/Card_Modifiers · P2-R3 https://balatrowiki.org/w/Unlocks · P2-R11 https://primagames.com/gaming/how-to-unlock-everything-in-balatro-jokers-decks-vouchers-and-more (2024-02-20).
