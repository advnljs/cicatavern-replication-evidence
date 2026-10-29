**English** | [简体中文](README.zh-CN.md)

# Correction and apology — October 29, 2026

**Current conclusion: the available evidence is insufficient to substantiate my accusation that CicaTavern plagiarized Narrascape.** I withdraw the definite copying and replication claims previously made in this repository, and I apologize for jumping to conclusions. Thank you to the author for responding and providing additional details. This does not establish that the author never saw Narrascape or that development was wholly independent.

Key corrections and limits: the first full public commit is not the start of private development; the author showed screenshots of a private Git repository, but its full commit object and historical date have not been independently verified. SillyTavern community materials already contain precedents for action choices, time boxes, images and read-aloud. Matching short wording or the order in which features appeared does not by itself establish a source. Item 7 of the old list treated “at least one surprising” as a fixed fourth choice; item 13 compared a text turn that continues after closing with an image job; item 15 equated a roster used for drawing with dynamic narrative memory. These comparisons need correction. Related features cannot be multiplied as independent coincidences.

The corrections are grounded in the [author's response](https://github.com/Shikasar7/CicaTavern/issues/4#issuecomment-6477278101), the [four-choice rule](https://github.com/Shikasar7/CicaTavern/blob/48fa11bdfb9af6bda3614921208eb5c01524a705/server/basic.mjs#L100-L111), and the first public version's [text-turn](https://github.com/Shikasar7/CicaTavern/blob/cac0f965d3b68583f2ee73c536702a9d0823a7a9/server/http.mjs#L168-L178), [image-request](https://github.com/Shikasar7/CicaTavern/blob/cac0f965d3b68583f2ee73c536702a9d0823a7a9/server/http.mjs#L680-L714) and [narrative-prompt](https://github.com/Shikasar7/CicaTavern/blob/cac0f965d3b68583f2ee73c536702a9d0823a7a9/server/prompt.mjs#L63-L105) paths.

The material below is the original October 27 statement, preserved for the record. **Its accusations and conclusions are withdrawn and should not be cited as our current position.** Historical PDFs and images are preserved unchanged and may contain those withdrawn claims.

<details>
<summary>Read the withdrawn historical statement and images</summary>

**English** | [简体中文](README.zh-CN.md)

# Copied, then called original: CicaTavern vs. Narrascape

> **Try Narrascape: [narrascape.space](https://narrascape.space)**. It runs in the browser, no install, and has an English interface (EN in the top bar).

![Copied, then called original](evidence-en/01.png)

## TL;DR

- **We explored this in public since 2023** ([scripted-rpg](https://github.com/advnljs/scripted-rpg)), then built [Narrascape](https://narrascape.space) behind closed doors from **June 2026**. Our **first promo video went out on October 14, 2026**.
- **Four days later** the CicaTavern repository appeared on GitHub, its first version a single **17,472-line commit**. **Six days later** its promo note was on Xiaohongshu.
- We document **9 replications of our features and UI copy**, including a **word-for-word identical UI string** and a fourth "out of bounds" choice copied without the mechanism that gives it a purpose.
- On **every** overlapping feature we shipped first: by **5 days to 4 months**. All of his arrive bunched together, **4 to 13 days after our video**.
- **We do not claim the code was copied.** The tech stack is different. What was taken is the product: what to build, how it behaves, and what the screens say.

His repository is archived as a fork at **[advnljs/CicaTavern](https://github.com/advnljs/CicaTavern)** (frozen at `14a14e9`, v2.0.2, 48 commits), so every commit cited here stays verifiable.

## Read the evidence

| Document | English | Chinese |
|---|---|---|
| Full statement, with screenshot appendix | [Markdown](statement/statement-en.md) · [PDF](statement/statement-en.pdf) | [PDF](statement/statement-zh.pdf) |
| 29 suspicious points, graded | [Markdown](list/suspicious-points-en.md) | [PDF](list/suspicious-points-zh.pdf) |
| 9 side-by-side comparison cards | [`comparison/en/`](comparison/en/) | [`comparison/`](comparison/) |
| The full image set (17 images) | [`evidence-en/`](evidence-en/) | [`xiaohongshu/`](xiaohongshu/) |

## We started in 2023, in public

[**scripted-rpg**](https://github.com/advnljs/scripted-rpg) is our public repository from **June 2023**, 20 commits between June and November 2023. It turns a fixed story (Lovecraft's *The Rats in the Walls*) into a text RPG hosted by a language model, and already had:

- a **storybook with a hidden truth** the player uncovers;
- **key plot event points** that keep the story on track whatever the player does;
- **world events the player cannot control**: "the user only controls their character's choices, but cannot control all changes in the entire story world";
- a **knowledge agent** for memory;
- **Stable Diffusion illustrations** for scenes.

Narrascape is where that line of work went next. Its demo world is also Lovecraft: *At the Mountains of Madness*.

## The timeline

| When (UTC+8) | Narrascape | CicaTavern |
|---|---|---|
| Jun 2023 | [scripted-rpg](https://github.com/advnljs/scripted-rpg) public: text RPG + AI illustrations | — |
| Jun 15, 2026 | Day one: choices every turn, a space-time judge that blocks impossible actions, an action-restriction setting | — |
| Jun 16 | Frozen baseline (append-only context for cache hits); world generator; per-turn checkpoints | — |
| Jul 14 | Site launched, no promotion | — |
| Aug 25 | The fourth, out-of-bounds "transgression" choice is finalized | — |
| Sep 6 | Read-aloud, added for livestreams | — |
| Sep 25 | Context consolidated only when it would overflow; edit a new world by chat | — |
| Oct 11–17 | Turn illustrations, character portraits, one art style per world, background jobs, portrait history | — |
| **Oct 14** | **First public promo video** | — |
| Oct 18 01:30 | | GitHub repo created; v1.0.0 as **one 17,472-line commit**; 20 commits and 6 versions that day |
| Oct 19 | | v1.6.0: four built-in action choices, "at least one surprising"; a "time box" |
| ~Oct 20 | | Promo note on Xiaohongshu |
| Oct 22 | | Avatar generation; editing a card by chat |
| Oct 27 | | v2.0.0 "draw history"; v2.0.3 context meter with auto-compaction |

![We shipped every one first](charts/lead-en.png)

## The evidence, image by image

The 17 images below carry the whole case. Screenshots of the two products are in Chinese because both interfaces are Chinese-first; every claim is written out in English.

### 1. Half a year vs. one week

![Evidence 1](evidence-en/02.png)

From scripted-rpg in 2023 and day one in June 2026, it took us months to build this set. His public record covers ten days: 30 versions, over 70,000 lines. On October 18 alone he made 20 commits and shipped 6 versions, including an Android app, an exe launcher and in-app updates. No earlier CicaTavern development appears in any of his public repositories.

### 2. His first version arrived finished

![Evidence 2](evidence-en/03.png)

Illustrations, character roster, art style, read-aloud and background generation all appear together in the [v1.0.0 commit](https://github.com/Shikasar7/CicaTavern/commit/cac0f96): 2,489 lines of image and voice code, with 551 lines of tests already written. No simple first version, no iteration. His issue tracker has 3 issues, and nobody asked for any of these features.

### 3. Nine replications

![Nine replications](evidence-en/04.png)

| # | Replication | Narrascape | CicaTavern |
|---|---|---|---|
| 1 | Illustration placeholder **「正在构思画面」 ("composing the scene"), word for word** | Oct 11 | Oct 18 ([`web/media.js` L164](https://github.com/Shikasar7/CicaTavern/blob/cac0f965d3b68583f2ee73c536702a9d0823a7a9/web/media.js#L164)) |
| 2 | Under each turn: illustration + read aloud + regenerate | Sep 6 / Oct 11 | Oct 18 |
| 3 | Fourth choice: our "transgression" → his "surprising" | Aug 25 | Oct 19 ([`server/basic.mjs` L101–108](https://github.com/Shikasar7/CicaTavern/blob/48fa11bdfb9af6bda3614921208eb5c01524a705/server/basic.mjs#L101-L108)) |
| 4 | Each turn opens with time and place | in the Oct 14 video | Oct 19 |
| 5 | Per-turn checkpoints: undo / redo / branch | Jun 16–17 | Oct 18 |
| 6 | Right panel with each turn's processing data | Jun 16 | Oct 18 |
| 7 | "Consolidate context" ↔ "compress context", automatic at the limit | Sep 25 / Oct 16 | Oct 18 / Oct 27 ([`d7974cb`](https://github.com/Shikasar7/CicaTavern/commit/d7974cb)) |
| 8 | Portraits: generate, redraw, switch back to an older one | Oct 11 / Oct 17 | Oct 22 / Oct 27 ([`d276733`](https://github.com/Shikasar7/CicaTavern/commit/d276733)) |
| 9 | A world from a few lines, edited by chat ("基调" tone, "想怎么改" what to change) | Jun 16 / Sep 25 | Oct 18 / Oct 22 |

#### Replication 1: 「正在构思画面」, word for word

![Replication 1](evidence-en/05.png)

While an illustration is being made, both apps show the same six characters, 「正在构思画面」, then a second "painting" stage. Ours shipped on October 11; his is in the first commit on October 18.

#### Replication 2: under each turn, illustration + read aloud + regenerate

![Replication 2](evidence-en/06.png)

The illustration sits inside the turn, with read-aloud and regenerate right below. We added read-aloud on September 6 for livestreams; he gives no reason for his.

#### Replication 3: the fourth choice

![Replication 3](evidence-en/07.png)

Our fourth choice is the thing you most want to do but never would. It runs into our space-time judge, and a block points you to Game Settings to loosen the restriction. His fourth choice is "at least one surprising", with no judge and no restriction setting behind it.

#### Replication 4: time and place at the top of each turn

![Replication 4](evidence-en/08.png)

Our scene header with day and place was on screen in the October 14 video. His "time box" arrived on October 19.

#### Replication 5: per-turn checkpoints

![Replication 5](evidence-en/09.png)

"Undo the last turn", "redo", "branch here": ours since June 16–17. His undo, rollback and "branch to a new chat" all arrived on October 18.

#### Replication 6: the right-hand processing panel

![Replication 6](evidence-en/10.png)

Our "Turn Process" summary (since June 16) shows each turn's window usage and cache hits on the right. His "Last turn" panel shows cache hits and timing in the same place.

#### Replication 7: consolidate ↔ compress context

![Replication 7](evidence-en/11.png)

Ours consolidates "only when the next turn would exceed the window" (September 25), with a button since October 16. His "compress context" button arrived on October 18, and the automatic step on the evening of October 27.

#### Replication 8: portraits, history, switch back

![Replication 8](evidence-en/12.png)

We generate avatar and standing portrait together (October 11) and keep past portraits to switch back to (October 17). He added avatar generation on October 22 and "draw history" on October 27.

#### Replication 9: a world from a few lines, edited by chat

![Replication 9](evidence-en/13.png)

Same fields (including 基调, "tone"), autofill, and editing by chat with the same prompt wording ("想怎么改", "what to change"). Ours since June 16 and September 25; his October 18 and 22.

### 4. Made into his headline

![Evidence 4](evidence-en/14.png)

His video's end card lists 8 selling points. Five of them map one-to-one onto features we shipped first: high cache hit rate (our frozen baseline, June 16), illustration and read-aloud (September 6 / October 11), custom character looks (October 11), four action choices (August 25), background generation (October 13).

### 5. Even the numbers

![Evidence 5](evidence-en/15.png)

The biggest number in his video is "cache hit rate up to 97%". His own [README (L37–45)](https://github.com/Shikasar7/CicaTavern/blob/14a14e9687ff58c7fd9cc13213858d859013dc0a/README.md?plain=1#L37-L45) says the Claude rows come from the author's personal setup via Claude Code. Elsewhere it says a Claude subscription cannot be used as an API key. The DeepSeek row covers 13 turns.

### 6. Our conclusion

![Conclusion](evidence-en/16.png)

Six days from our first video to his promo note, and nine replications. We believe CicaTavern copied Narrascape.

### 7. Three questions

![Questions](evidence-en/17.png)

## Why the fourth choice matters most

The out-of-bounds choice is not a gimmick in Narrascape. It is one part of a loop:

1. Choice 4 is the thing you most want to do right now but never would: kiss her, flip the table, say the secret out loud.
2. The **space-time judge** may stop it. The turn doesn't happen, and a dialog explains why.
3. The dialog ends with: *"You can adjust or turn off Action realism in Game Settings."*
4. Players loosen the restriction, from Strict to Standard to Loose to **Unrestricted**, and discover how far the world will go with them.

Here is our client today, in English:

| The fourth choice, styled on its own | The restriction it leads to |
|---|---|
| ![Our choices in English](screenshots/en/en-choices.png) | ![Action realism setting](screenshots/en/en-settings.png) |

![Narrascape in English](screenshots/en/en-turn.png)

CicaTavern has no judge and no restriction setting. Its "surprising" fourth option has nothing to run into and nothing to unlock. Any single feature on our list may exist somewhere in a SillyTavern extension or in AI Dungeon. **This loop, and the combination and tuning around it, is not in mainstream products. It appeared in CicaTavern within days of our video.**

## Verify it yourself in five minutes

1. Open his [first commits](https://github.com/Shikasar7/CicaTavern/commits/main/?since=2026-10-17&until=2026-10-19): an "Initial commit" with a LICENSE, then [v1.0.0](https://github.com/Shikasar7/CicaTavern/commit/cac0f96) at +17,472 lines.
2. Open [`web/media.js` line 164](https://github.com/Shikasar7/CicaTavern/blob/cac0f965d3b68583f2ee73c536702a9d0823a7a9/web/media.js#L164) and find 「正在构思画面」.
3. Open [`server/basic.mjs` lines 101–108](https://github.com/Shikasar7/CicaTavern/blob/48fa11bdfb9af6bda3614921208eb5c01524a705/server/basic.mjs#L101-L108), added on October 19: "four choices… at least one surprising".
4. Open [narrascape.space](https://narrascape.space), click ✦ in the top bar for our changelog, then play a turn and tap the fourth choice.
5. Compare with the frozen fork at [advnljs/CicaTavern](https://github.com/advnljs/CicaTavern) if anything in the original has changed.

## FAQ

**Isn't each of these features common?**
Some are, taken alone. That is why we list the combination, the dates and the wording. Seven selling points, nine replications and an identical UI string, all arriving within two weeks of our first video, are not a coincidence.

**Are you saying he copied your code?**
No. His code is a different stack. We are saying he replicated the product: features, behaviour, selling points and UI copy.

**Why should we trust your dates?**
His dates are his own commits. Ours from October 11 are in the in-app changelog, and the October 14 video is public. Earlier ones are from our development records, and our 2023 work is in a [public repository](https://github.com/advnljs/scripted-rpg). The in-app changelog launched on October 19, and entries for the days before were filled in at launch.

**What do you want?**
An honest answer to the three questions, and a line in his README saying "inspired by Narrascape" if it was.

## What we ask

1. The first version was a finished 17,472-line commit. Where is the development history from before October 18?
2. Why does a product with no judge add a "surprising" fourth choice on October 19? Is it related to our October 14 video?
3. Before building all of this, had you played narrascape.space or watched our video?

Learning from others is no shame. Pretending not to know them is.

## Repository contents

| Folder | What is inside |
|---|---|
| [`evidence-en/`](evidence-en/) | The 17-image evidence set in English |
| [`xiaohongshu/`](xiaohongshu/) | The same set in Chinese, as posted on Xiaohongshu, with its caption |
| [`comparison/en/`](comparison/en/), [`comparison/`](comparison/) | Overview + 9 side-by-side cards, English and Chinese |
| [`charts/`](charts/) | "We shipped every one first" chart, English and Chinese |
| [`statement/`](statement/) | Full statement: [English](statement/statement-en.md) ([PDF](statement/statement-en.pdf)) and [Chinese PDF](statement/statement-zh.pdf) |
| [`list/`](list/) | 29 graded points: [English](list/suspicious-points-en.md) and [Chinese PDF](list/suspicious-points-zh.pdf) |
| [`screenshots/en/`](screenshots/en/) | Our live client in English |
| [`evidence/`](evidence/) | Raw screenshots: his GitHub pages (Oct 27), his video frames and transcript, his Xiaohongshu note, our livestream frames and live client |

## Notes on sources

- **CicaTavern dates** come from its public commit history and changelog. GitHub groups commits by UTC, so "Oct 17" in screenshots is October 18 in UTC+8.
- **Narrascape dates** from October 11 onward are in the in-app changelog (✦ on narrascape.space). The October 14 video is public. Earlier dates come from our development records, and our 2023 exploration is the public [scripted-rpg](https://github.com/advnljs/scripted-rpg) repository.
- Screenshots of his repository and videos are included for commentary and comparison.

— Narrascape · **[narrascape.space](https://narrascape.space)**


</details>
