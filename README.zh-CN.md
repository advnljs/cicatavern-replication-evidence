[English](README.md) | **简体中文**

# 抄就抄了，别装原创：CicaTavern 与 Narrascape

> **Narrascape 产品地址：[narrascape.space](https://narrascape.space)**，网页打开就能玩，不用安装。

[Narrascape](https://narrascape.space) 是一个 AI 跑团、互动小说的网页应用。点子琢磨了几年，2026 年 6 月起关起门做了小半年，**10 月 14 日第一次发宣传片**。

6 天后（10 月 20 日前后），一个叫 **CicaTavern** 的项目开始在小红书宣传，它的主打功能，一项一项对得上我们已经上线、已经展示过的东西。

**我们认为 CicaTavern 复刻了 Narrascape 的功能、卖点和界面文案。** 我们不说他抄代码，技术栈不一样；他拿走的是产品本身：做什么、怎么表现、界面上写什么。

下面每一条都链接到公开材料。他的仓库已 fork 存档：**[advnljs/CicaTavern](https://github.com/advnljs/CicaTavern)**（停在 `14a14e9`，2.0.2，48 个提交），原仓库之后怎么改，这份都还在。

![9 处复刻总览](comparison/card-00.png)

## 一、时间对不上

| 时间（北京时间） | Narrascape | CicaTavern |
|---|---|---|
| 6 月 15 日 | 项目第一天：每回合选项、能拦下不合理行动的“时空裁判”、行为限制设置 | — |
| 6 月 16 日 | 冻结基线（只往后追加，每轮命中缓存）；世界生成器 | — |
| 8 月 25 日 | 第四个“越界”选项定型 | — |
| 9 月 6 日 | 朗读（为直播加的） | — |
| 10 月 11—17 日 | 回合插图、角色形象、统一画风、后台任务、历史形象 | — |
| **10 月 14 日** | **第一次公开发宣传片** | — |
| 10 月 18 日 01:30 | | 仓库创建；1.0.0 **一次提交 17,472 行**；当天 20 个提交、6 个版本 |
| 10 月 19 日 | | 1.6.0 内置四个行动选项，“至少一项出人意料” |
| 10 月 20 日前后 | | 小红书宣传笔记 |
| 10 月 27 日 | | 2.0.0 抽图历史；2.0.3 上下文用量表 + 自动压缩 |

作者所有公开仓库里，找不到任何更早的 CicaTavern 开发痕迹。功能一出现就是成品（第一笔提交里配图和朗读代码 2,489 行，连 551 行测试一起写好），没有迭代，也没说为什么加。issue 区一共 3 条，没有人提过这些需求。

## 二、9 处复刻

| # | 对照点 | Narrascape | CicaTavern |
|---|---|---|---|
| 1 | 出图提示 **「正在构思画面」一字不差** | 10-11 | 10-18（[`web/media.js` 第 164 行](https://github.com/Shikasar7/CicaTavern/blob/cac0f965d3b68583f2ee73c536702a9d0823a7a9/web/media.js#L164)） |
| 2 | 每回合下面：插图 + 朗读 + 重新生成 | 9-6 / 10-11 | 10-18 |
| 3 | 第四个选项：我们的“越界”→ 他的“出人意料” | 8-25 | 10-19（[`server/basic.mjs` 第 101–108 行](https://github.com/Shikasar7/CicaTavern/blob/48fa11bdfb9af6bda3614921208eb5c01524a705/server/basic.mjs#L101-L108)） |
| 4 | 回合开头先标时间和地点 | 10-14 宣传片可见 | 10-19 |
| 5 | 按回合撤回 / 重做 / 分支 | 6-16—6-17 | 10-18 |
| 6 | 右栏放每轮处理数据 | 6-16 | 10-18 |
| 7 | 整理上下文 ↔ 压缩上下文，超限自动 | 9-25 / 10-16 | 10-18 / 10-27（[`d7974cb`](https://github.com/Shikasar7/CicaTavern/commit/d7974cb)） |
| 8 | 角色形象：生成、重画、换回旧版 | 10-11 / 10-17 | 10-22 / 10-27（[`d276733`](https://github.com/Shikasar7/CicaTavern/commit/d276733)） |
| 9 | 几句话建世界，再用对话改（“基调”“想怎么改”） | 6-16 / 9-25 | 10-18 / 10-22 |

每一处都有一张左右对照图，见 [`comparison/`](comparison/)。

单拿某一项，酒馆插件、AI Dungeon 里也许能找到类似的。**但这一整套组合，以及它打磨的调性，主流产品里没有。** 比如一个专门去撞裁判、被拦下后引导玩家去设置里放开限制的第四个选项。我们磨了好几个月，他在我们宣传片发出后几天就有了。

## 三、越界选项：照猫画虎

Narrascape 每回合的第四个选项故意越界：你此刻最想干、平时不敢干的那件事。时空裁判可能拦下它，弹窗里提示“可在游戏设置中调整或关闭主角行为限制”。它的用处就是勾着玩家去撞裁判，然后发现这个世界能陪你玩到多疯。

CicaTavern 在我们宣传片发出后第 5 天（10 月 19 日）加上“四个行动选项，至少一项出人意料”。它没有裁判，也没有行为限制设置，这个选项什么也撞不到，也没有什么可以解锁。恶趣味抄走了，机制怎么来的，他不知道。

| Narrascape（10-14 宣传片） | CicaTavern（他的宣传片约 00:38） |
|---|---|
| ![我们的选项](statement/our-choices.jpg) | ![他的选项](statement/his-choices.jpg) |

## 四、97% 这个数字

他宣传片里最大的数字是“缓存命中实测可高达 97%”。他自己的 README（[第 37–45 行](https://github.com/Shikasar7/CicaTavern/blob/14a14e9687ff58c7fd9cc13213858d859013dc0a/README.md?plain=1#L37-L45)）写着，Claude 两行来自作者自用的版本、走 Claude Code；同一份 README 另一处写着 Claude 订阅不能当 API Key 用；DeepSeek 那行只统计了 13 轮。

## 给个说法

1. 第一个版本就是 17,472 行的成品。10 月 18 日之前的开发记录在哪？
2. 一个没有裁判的产品，10 月 19 日加一个“出人意料”的第四个选项干什么？和我们 10 月 14 日的宣传片有没有关系？
3. 做这一整套之前，玩没玩过 narrascape.space，看没看过我们的宣传片？

如果确实参考了，在 README 里写一句“灵感来自 Narrascape”。参考别人不丢人，装不认识才丢人。

## 仓库内容

| 目录 | 内容 |
|---|---|
| [`statement/`](statement/) | 完整声明（`statement-zh.pdf`，源文件 `index.html`），含截图附录 |
| [`list/`](list/) | 29 项分级可疑点清单（`suspicious-points-zh.pdf`） |
| [`comparison/`](comparison/) | 总览 + 9 张功能与文案对照图 |
| [`xiaohongshu/`](xiaohongshu/) | 小红书 17 张图和文案 |
| [`evidence/their-repo/`](evidence/their-repo/) | 他 GitHub 页面截图（2026-10-27 截取）、2.0.3 更新说明原文 |
| [`evidence/their-video/`](evidence/their-video/) | 他宣传片的截帧和转写 |
| [`evidence/their-xiaohongshu/`](evidence/their-xiaohongshu/) | 他的小红书笔记（10-27 显示“7 天前”） |
| [`evidence/our-video/`](evidence/our-video/)、[`evidence/our-live/`](evidence/our-live/) | 我们 10-13 直播截帧（用于 10-14 宣传片）和线上客户端截图 |

## 关于时间来源

- **CicaTavern 的日期**来自他公开的提交记录和更新日志。GitHub 按 UTC 分组，截图里的“Oct 17”即北京时间 10 月 18 日。
- **Narrascape 10 月 11 日起的日期**在 app 更新日志里可查（narrascape.space 顶栏 ✦）。更新日志 10 月 19 日上线，之前几天的条目是上线时补录的。
- **Narrascape 10 月 11 日之前的日期**来自我们的开发记录；10 月 14 日宣传片是它所展示内容的公开时间点。
- 引用他仓库和视频的截图，用于评论与对比。

— Narrascape · [narrascape.space](https://narrascape.space)
