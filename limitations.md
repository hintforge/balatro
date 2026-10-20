# Balatro -- Limitations & Blocked Sources

Sources I found that look useful but couldn't fully fetch -- paywalls, Cloudflare, age gates, video-only content, etc. URLs preserved so the player (or another contributor) can open them in a real browser.

## How to read this file
- Each entry: topic, URL, block type, what I could glean, best alternative I did get to.
- Each per-topic file (in `puzzles/`, `[areas]/`, `items/`, `sections/`) also lists its own blocked sources at the bottom -- the player rarely needs to come hunting here.
- This file is the catch-all for sources that didn't fit a specific topic.

## Block types
- **paywall** -- content gated behind a subscription or article limit
- **cloudflare** -- Cloudflare bot challenge / 403 / 503 from WebFetch
- **video-only** -- YouTube or other video where the answer is shown visually; no readable text equivalent
- **age-gate** -- content blocked behind age verification
- **cookie-wall** -- popup or consent flow that broke the fetch
- **search-snippet-only** -- search engine returned a snippet but the page itself wasn't reachable
- **dead-link** -- URL was in another source but no longer resolves

- **robots-restriction** -- the external research runtime reports a robots access restriction
- **terms-restriction** -- a stated retrieval restriction was reported; preserve the actual evidence
- **javascript-dependent** -- useful content requires page execution the available tool did not perform
- **login-required** -- a signed-in session is required
- **access-not-checked** -- no content/access check was performed; never call this robots-blocked

## Companion tools

For every useful map, tracker, database or completion tool supplied, recalled or found:

- Name and URL if verified (otherwise mark unknown/unverified)
- Apparent coverage, evidence for it, and uncertainty; unread coverage is not confirmed game data
- Reason not read, access-check result, policy evidence if available, and check date
- How a person could use it, best readable alternative, and wider-spoiler warning where relevant

Merge repeated URLs with dated evidence retained. Read tools can also be recorded here when they offer a useful location fallback. Record an honest empty statement when no candidates were found; do not imply exhaustive discovery.

- Balatro Compendium (Raycast extension) -- https://www.raycast.com/azyz/balatro-compendium -- apparent coverage: 12 commands (Jokers, Tarot, Decks, Planets, Spectrals, Vouchers, Upgraded Vouchers, Enhancements, Seals, Skip Tags, Blinds, Boosters). macOS only; works offline; only version entry "1.0 Release Candidate" (2024-07-28); data source not named. Access: store page read by the P1 researcher 2026-10-19 (earlier "not checked" on 2026-10-19 is superseded; one check). Wider-spoiler warning: lists all content including unlock conditions. How to use: macOS Raycast users can look up any card; not usable from this PC.
- games.gg unlock guide -- https://games.gg/balatro/guides/how-to-unlock-everything-balatro/ -- P1: read (page dated 2026-06-07); does NOT list per-Joker unlock conditions despite its title (covers the Unlock All button, general unlock categories, tracking tips). P2: fetch refused by the permission system on the same date, never retried. Conflicting access results kept as reported. Low value for unlock chains. A Japanese translation (https://games.gg/ja/balatro/guides/balatro全要素の解除方法/) was read by P1; its one example Joker condition ("play Flush 20 times") matches no real Joker, so it is a poor source. `[Contradicted across sources -- see notes]`
- balatrowiki.org Unlocks, Collection and Profile pages -- https://balatrowiki.org/w/Unlocks -- read by P2 2026-10-19; the readable complete-collection inventory behind the unlock tables.
- Other tools found in search, not read (check dates 2026-10-19; unread coverage is not confirmed game data): awesome-balatro index https://github.com/jie65535/awesome-balatro (calculators, seed finders, save editors); Balatro Calculator (Saffron), Balatrolator (kleinfreund), Balatro HQ, west-games calculator https://west-games.com/balatro-score-calculator/ (score calculators); two seed analyzers by MathIsFun, Balatro4J (seed searchers; useful for Ante -1 seeds); BalatroSaveEditor https://github.com/TeddyHuang-00/BalatroSaveEditor (P2: fetch refused by the permission system, not retried) and BalatroEditor https://github.com/lchad/BalatroEditor (save and profile editors); Save Rewinder mod https://www.nexusmods.com/balatro/mods/706; Nexus Mods keyboard mod https://www.nexusmods.com/balatro/mods/49 and the "typist" mod (keyboard play); Steamodded and Balamod (mod loaders), Zoker's Mod Menu; a speedrun timing mod (name withheld, URL not found). Wider-spoiler warning: calculators and editors expose all content.
- Discovery limit: found by search, not exhaustive. No interactive map exists in this spatial-less game as far as found. Absence of other results does not prove no other tools exist.

## Entries

### Sportskeeda -- achievements list
- Source: https://www.sportskeeda.com/esports/balatro-complete-list-achievements-trophies
- Block type: cloudflare (plain fetch returned HTTP 405; read successfully through a headless-browser fetch tool on 2026-10-19)
- Why I think it has the answer: lists all 32 PlayStation trophy names.
- What I could glean before the block: full list of names; Steam-specific list and hidden flags not shown.
- Best alternative I did get to: `research_briefs/achievement_stubs.md`.

### Other blocked or unread pages (P1 and P2, 2026-10-19)
- Fandom wiki -- https://balatrogame.fandom.com/wiki/Jokers and /Vouchers, /Blinds_and_Antes, /Stickers -- cloudflare (WebFetch HTTP 402). P1 read them via the local browser fetch tool (capture-method browser_fetch in practice; claims carry the default `web_fetch` tag because the research tool did the capture); P2 could not read /Unlocks. Pages still wanted from a browser: https://balatrogame.fandom.com/wiki/Unlocks.
- itch.io posts -- https://itch.io/post/12293014 and https://itch.io/post/16001980 -- cloudflare (403). Reported developer replies on save, continue and pack-peeking fixes; the save-exploit status is therefore unverified.
- Reddit "Does save scumming work with wheel of fortune?" -- [Reddit source unreachable -- canonical URL: https://www.reddit.com/r/balatro/comments/1qrxc2g/does_save_scumming_work_with_wheel_of_fortune/] -- the claim that random outcomes are fixed in a save rests on one forum source.
- Steam Community achievements page -- https://steamcommunity.com/stats/2379780/achievements -- javascript-dependent: only 15 to 26 of 31 names render in a plain read (lazy loading); the full list was read from TrueAchievements instead.
- SteamDB, TrueAchievements, GodisaGeek -- cloudflare (403) for a plain fetch; read through the local browser fetch tool.
- Unread guides (search snippets only): Comicbook.com strategies https://comicbook.com/gaming/news/best-balatro-strategies-how-to-win/ ; Twinfinite builds https://twinfinite.net/guides/best-builds-in-balatro-best-balatro-strategies-explained/ ; Pro Game Guides Joker order https://progameguides.com/balatro/best-joker-order-in-balatro/ ; PC Gamer forum https://forums.pcgamer.com/threads/balatro-tips-and-strategies-add-your-own.148962 ; Press Start 1.0.1f notes https://press-start.com.au/news/2024/04/08/the-latest-balatro-update-has-some-massive-changes-that-should-make-winning-easier/ ; Windows Central 1.0.1f https://www.windowscentral.com/gaming/balatro-update-patch-101f ; PCGamesN 1.0.1 experimental https://www.pcgamesn.com/balatro/patch-1-0-1-experimental ; Dot Esports achievements https://dotesports.com/indies/news/how-to-get-all-trophies-and-achievements-in-balatro ; TrueAchievements Completionist guide https://i1.trueachievements.com/a424947/completionist-achievement ; platget trophy guide https://platget.com/guides/balatro-trophy-guide (older stake names) ; pixiv dic https://dic.pixiv.net/a/Balatro (ja) ; hackmd zh note https://hackmd.io/@CcwBnBSiSOi5tUmGXfXYFQ/BJP0w4Xp6 (read by P2, nothing usable). Access not checked for all of them.
- Not covered by P1 or P2: no video segment was transcribed; the 5-independent-source floor was not met for any fact (balatrowiki and the Fandom wiki share history); no datamining or decompiled-source page was read (Standard Pack modifier odds and one rare Spectral card's odds under a voucher are missing); no non-English source for scoring or stakes except the Korean wiki; Chinese Joker wiki read once; remaps and controller-on-PC specifics are snippet-only; hidden-achievement flags and seeded-run achievement rules are unverified (the lists read show no hidden marker).

## Source conflicts logged (P1 and P2, 2026-10-19)
Each entry: the two values, who gave them, how the corpus treats it. None is resolved by a read primary source.
- **Planet count:** Steam store page 11; balatrowiki and Fandom 12 (9 regular + 3 secret). Corpus uses 12, medium confidence.
- **Booster Pack count:** wiki 15 type-and-size variants; P2 says the Collection counts 32 Booster Pack entries (cause unknown, possibly art variants). Corpus lists 15 and notes the 32.
- **Ante 8 target:** wiki tables 50,000 to 200,000 base; one January 2026 editorial guide says "roughly 300 million". Corpus uses the wiki tables (confirmed by the Korean wiki).
- **Endless formula:** the English wiki's closed form gives about 98,000 for Ante 9 against 110,000 in its own table. Corpus uses the table and omits the formula.
- **Ante 39 outcome:** one wiki counts reaching it as completing Endless; the Korean wiki says Ante 38 is the practical end and Ante 39 is always a game over. Corpus states both.
- **Tarot-shop voucher weights (the two vouchers that multiply Tarot appearances):** given as 9.6 and 32 on a base of 4, which does not match their 2x and 4x labels (8, 16). Corpus gives both numbers and labels the mismatch.
- **Rarity counts:** English wikis Common 61, Uncommon 64, Rare 20, Legendary 5; the Chinese wiki (machine-counted) 61/65/19/5. One locked Joker's cost: $7 in English wikis, $5 on the Chinese wiki. Corpus uses English values.
- **Challenge Mode unlock:** "win with five different decks" (balatrowiki) against "five runs using any decks" (Dot Esports). Corpus states the specific wording and the alternative.
- **Collection-achievement scope:** "100% of the collection" (platform text, balatrowiki) against "whole Joker collection" (one Steam thread). Corpus uses the platform text.
- **Shop purchases on quit:** one thread says purchases are saved on quit; another (2024-05) says they revert and refund. Possibly version-dependent.
- **Deleting save.jkr:** forum posters disagree on whether stake progress survives.
- **Launch-day Prima deck and voucher lists** (2024-02-20): other thresholds and non-existent names (Braided, Silver, Foil, Holographic, Polychrome decks; Electromagnet, Tesselation, Nano Tong vouchers). Corpus treats them as obsolete.
- **Boss-blind spoiler tier:** P1 tagged the regular boss table late-game; P2 tagged the boss pool progression. Corpus classification: progression for the 23 regular bosses, late-game for the 5 Showdown bosses and Endless.
- **Skip strategy:** guides disagree on whether skipping Tags is worthwhile (builds and mechanics files record each side).
- **Unlock All and achievements:** P1 could not find the effect; P2 found it (permanently disables achievements on that profile). Corpus uses P2's two-page evidence; this is a gap filled, not a conflict.
- **Steam version:** the exact in-game version string is unconfirmed; two Fandom pages cite "1.0.1o-FULL".

## Always-blocked categories

- Randomized content per run (shop contents, pack contents, boss blind order, which joker appears) cannot be researched per save; the corpus records rules, odds and pools, not outcomes.
- Exact unlock conditions for each locked item are visible in-game by hovering in the collection screen; no external source substitutes for checking the player's own profile state.
