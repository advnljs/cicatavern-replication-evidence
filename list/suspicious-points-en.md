[← Back to README](../README.md) · [Statement (EN)](../statement/statement-en.md) · [中文 PDF](suspicious-points-zh.pdf)

# CicaTavern: 29 suspicious points

*The Narrascape team · October 27, 2026 · companion to the statement [Copied, then called original](../statement/statement-en.md)*

Only items with a public basis are listed.

- **Narrascape evidence** comes from two places: our promo video (published October 14) and the in-app changelog (✦ in the top bar of [narrascape.space](https://narrascape.space)). Items marked "team account" come from our development history.
- **CicaTavern evidence** comes from his Xiaohongshu note and promo video, and his public CHANGELOG, GitHub commits, README and issues. For features, we use the version where each first appears.
- **His repository is archived** as a fork: [github.com/advnljs/CicaTavern](https://github.com/advnljs/CicaTavern) (archived Oct 27, frozen at v2.0.2 / commit `14a14e9`). Commits and versions below refer to that archive. Original: [github.com/Shikasar7/CicaTavern](https://github.com/Shikasar7/CicaTavern).

**Strength:**
- **Strong:** the timing is tight, and he had no such feature before.
- **Medium:** we were clearly earlier.
- **Weak:** common in the category, or only similar wording.

## A. Timing

| # | Point | Narrascape | CicaTavern | Strength |
|---|---|---|---|---|
| 1 | His repo created 4 days after our video | Oct 14: first promo video (video) | Oct 18 01:30: GitHub repo created | Medium |
| 2 | His Xiaohongshu promo note 6 days after our video | — | Around Oct 20 ("7 days ago" on Oct 27), featuring four action choices, illustration and read-aloud, cache hit rate | Medium |
| 3 | First version delivered in one piece | — | v1.0.0 as one 17,472-line commit; that day 20 commits, 6 versions, 33,533 lines added | Medium |
| 4 | Ten days of development speed | — | Oct 18–27: 48 commits, 30 versions, about 74,000 lines added | Medium |
| 5 | A changelog the day after ours launched | Oct 19: new "Changelog" (changelog) | v1.8.0, Oct 20: "What's new" | Weak |
| 6 | Problem reporting | Oct 18: new "Feedback" (changelog) | v1.9.3, Oct 25: send an error log when something goes wrong | Weak |

## B. Similar features (ours public first, his later)

| # | Feature | Narrascape | CicaTavern first appearance | Strength |
|---|---|---|---|---|
| 7 | Four action choices per turn, one breaking expectations | Finalized Aug 25 (team account); highlight of the Oct 14 video, choice 4 is out of bounds, e.g. "throw the whole bowl of hot soup at the two beams of light" (video); paired with the space-time judge, which on rejection says the restriction can be adjusted or turned off in Game Settings (app) | v1.0.0 only shows choices that come with a card as buttons; v1.6.0 on Oct 19 builds in "four… at least one surprising"; in his video the four buttons look identical and the fourth is a joke; no interceptor, no restriction setting | Strong |
| 8 | Turn illustrations: a model reads the story and writes the image prompt | Shipped Oct 11 (changelog); one-tap illustration in the Oct 14 video (video) | v1.0.0, Oct 18 | Medium |
| 9 | Illustrations drawn from each character's fixed look, consistent across turns | Oct 12 (changelog) | v1.0.0, Oct 18 (character roster + reference images) | Medium |
| 10 | Character portrait generation (avatar / standing portrait) | Oct 11: avatar and standing portrait generated together (changelog) | v1.0.0 reference images; standing portraits Oct 20; avatar generation Oct 22 | Medium |
| 11 | One art style per world / per card | Oct 12 (changelog) | v1.0.0, Oct 18 | Medium |
| 12 | One-tap read-aloud | Read-aloud button on screen in the Oct 14 video (video) | v1.0.0, Oct 18 | Medium |
| 13 | Generation finishes in the background, closing the page doesn't stop it | Oct 13: image jobs finish in the background (changelog) | v1.0.0, Oct 18 (turns keep writing in the background) | Medium |
| 14 | Old versions kept after a redraw, can switch back | Oct 17: past portraits viewable, can be set as default (changelog) | v2.0.0 "draw history", Oct 27 | Strong |
| 15 | Character looks written into memory, used when narrating | Oct 11 (changelog) | v1.0.0, Oct 18 character roster (fixed looks, outfit) | Medium |
| 16 | Promo wording | Tagline "Let's write a novel together~" (video) | "Step into a story yourself / so that every story has someone to write it with you" | Weak |
| 17 | Frozen baseline: fixed prefix, append-only, changing material last | Since Jun 16, live from the Jul 14 launch (team account) | v1.0.0, Oct 18; the top technical selling point in his video ("fixed prefix, append only at the end") | Weak |
| 18 | Context meter + automatic consolidation past the limit + user-set limit | In-app turn-process panel, "Context usage": current context / the window you set, consolidated only when the next turn would exceed it (app); "full context consolidation" fixes on Oct 18 (changelog) | v2.0.3 at 21:42 on Oct 27: used / limit, color change at the threshold, auto-compaction before the next turn, limit set in settings (original repo `d7974cb`, after the fork archive) | Medium |

## C. His features have no history

| # | Point | Narrascape | CicaTavern | Strength |
|---|---|---|---|---|
| 19 | Features appear finished, with no iteration | Illustrations changed in five rounds within a week (Oct 11, 12, 13, 16, 17), each in the changelog (changelog) | Illustrations, character roster, reference images, art style, read-aloud and background generation all in the single v1.0.0 commit; 2,489 lines of image and voice code, with 551 lines of tests | Strong |
| 20 | Features added without a reason | Transgression choice to lure players into the interceptor, then loosen it in settings; read-aloud for livestreams (team account · app) | Four action choices added as one preset toggle in v1.6.0, in a single line, with no reason for adding them, for "four", or for one being "surprising" | Medium |
| 21 | No user ever asked for these | — | 4 issue-tracker entries, the earliest on Oct 20: an import error, a search request, a provider suggestion, a security patch; nobody asked for four choices, illustrations or fixed looks | Medium |
| 22 | No earlier development trace | — | No earlier CicaTavern history in any of his public GitHub repositories; the first version is a single 17,472-line commit | Medium |

## D. Promotion

| # | Problem | Basis |
|---|---|---|
| 23 | The biggest number in his video, "97% cache hit rate", is out of users' reach | Small print in the video says an official Claude Opus 5.5 subscription was used; the README says the two Claude rows come from the author's personal setup via Claude Code, and elsewhere that a Claude subscription cannot be used as an API key; the DeepSeek row covers only 13 turns |

## E. UI and copy side by side (see [comparison cards](../comparison/))

| # | Point | Narrascape | CicaTavern | Strength |
|---|---|---|---|---|
| 24 | 「正在构思画面」 ("composing the scene"), word for word | Oct 11: while generating an illustration, shows 「正在构思画面」 → 「正在绘制」 | v1.0.0, Oct 18: [`web/media.js` line 164](https://github.com/Shikasar7/CicaTavern/blob/cac0f965d3b68583f2ee73c536702a9d0823a7a9/web/media.js#L164) 「正在构思画面」 → 「正在画」 | Strong |
| 25 | Time and place at the top of each turn | Oct 14 video frame: "Old-town Shaxian snack shop · Day 1 · early morning" | v1.6.0, Oct 19, "time box": time / place / weather | Medium |
| 26 | Per-turn undo, redo, branch | Jun 16 checkpoints: "undo the last turn", "redo the next turn"; Jun 17 "branch here" (team account) | Oct 18: "undo the last round" (in the card creator), rollback, "branch to a new chat" | Weak |
| 27 | Per-turn processing data in the right panel | Jun 16 "turn process summary"; Sep 24 two-window usage (team account) | v1.0.0, Oct 18: right panel "last turn" with cache hit, output, timing | Medium |
| 28 | "Consolidate context" ↔ "compress context" | Sep 25 automatic consolidation only when the window would overflow; Oct 16 "consolidate context" button (team account) | Oct 18 "compress context" button; Oct 27 automatic compaction | Medium |
| 29 | World creation: fields and chat editing | Jun 16 world generator "genre / tone (基调)"; Jun 17 "AI autofill"; Sep 25 "refine with AI": "What should change? (想怎么改？)" (team account) | Oct 18 card creator "tone (基调)", "filled in by the guide"; Oct 22 chat editing: "tell me what to change (说说想怎么改)" | Medium |
