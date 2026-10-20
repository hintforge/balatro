# Balatro — Hintforge Companion

![Balatro companion status — coverage, how current it is, and spoiler control](assets/readme-status-card.svg)

A spoiler-controlled hint companion for **Balatro**, LocalThunk's poker roguelike where you build a scoring engine out of Jokers, Planet cards, Tarots and Vouchers and push it through eight antes of blinds. Built in the [Hintforge](https://github.com/hintforge/builder) format: a loyal sidekick that answers only from these guide files — never from guesswork — at the spoiler level you set.

## Use it

You need a Hintforge reader running in Claude Code, Codex, or OpenClaw. Point it at this repo:

> Load the Balatro guide from github.com/hintforge/balatro

Then just ask — *"what does this Joker combo with," "should I take the interest or reroll," "how do I unlock the next deck."* Runtime setup lives in [`hintforge/reader`](https://github.com/hintforge/reader).

## Spoilers

Balatro has no story to spoil; what it hides is what you have not found yet. Locked Jokers, the later decks and stakes, the secret hands and the rarest cards stay out of answers until you raise the dials, so a first run still gets to discover them. Every fact carries its source and says how sure it is, and where the sources disagree or say nothing, the guide says so instead of guessing.

## What's inside

A structured Markdown corpus — scoring and run mechanics (blinds, antes, the shop, interest, tags, stakes), all 150 Jokers by when they become available, consumables, vouchers, decks and build ideas, the dependencies between unlocks, things you can miss, controls, settings, and all 31 achievements. The companion reads and writes only the files you control.
