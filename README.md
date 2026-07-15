# Shigeru Miyamoto Perspective Skill

[中文](#中文) · [English](#english)

一个从宫本茂公开访谈与游戏设计实践中提炼的 Codex Skill。它从玩家的手、动作、反馈与第一次游玩出发，帮助你评审游戏概念、核心循环、操作手感、关卡、教程、原型与开发取舍。

A Codex Skill distilled from Shigeru Miyamoto's public interviews and documented game-design practices. It reviews game concepts, core loops, controls, levels, tutorials, prototypes, and production trade-offs through player action, feedback, and the first-play experience.

> [!IMPORTANT]
> 本项目不是宫本茂本人、任天堂或其关联方的官方作品，也不代表其真实立场。它是基于公开资料提炼的分析视角。
>
> This is not an official project by Shigeru Miyamoto, Nintendo, or their affiliates, and it does not represent Miyamoto's actual views. It is an analytical perspective distilled from public sources.

---

## 中文

### 它解决什么问题

这个 Skill 不先问“故事够不够宏大”或“功能够不够多”，而是先追问：

> 玩家做什么 → 系统怎样回应 → 玩家为什么愿意再做一次？

适合用于：

- 评审游戏概念与 10—30 秒核心循环
- 改善移动、跳跃、镜头、输入与即时反馈
- 检查教程、前 5 分钟与前 30 分钟体验
- 设计关卡、探索空间、道具、敌人与自然引导
- 判断新技术是否真正改变玩家动作，而不只是提升规格
- 把团队争论改写成当天可以验证的最小可玩原型
- 识别内容膨胀、竞品模仿与“核心尚未成立”的风险

它不自动用于电影、主题公园、博物馆、IP 授权或一般商业战略。对于强作者叙事、长期运营和专业模拟等类型，也应结合其他方法与真实玩家测试。

### 六个核心模型

1. **先让手动起来**：动作—反馈是体验原子。
2. **`dokuso`，换一条跑道**：独特性不等于把竞品做得更大。
3. **做出来才知道**：原型用于发现问题，不是证明会议结论。
4. **借回第一次游玩者的眼睛**：入口要自然，深度从试错中长出来。
5. **让世界替规则说话**：用形状、重量、位置和结果建立可猜测的因果。
6. **留白让玩家完成作品**：给出一致规则与可发现线索，不替玩家规定唯一经历。

完整模型、适用边界和证据依据见 [`SKILL.md`](SKILL.md)。

### 安装

将仓库克隆到 Codex 的 skills 目录：

```bash
git clone https://github.com/SherryCW/shigeru-miyamoto.git \
  ~/.codex/skills/shigeru-miyamoto-perspective
```

重新打开 Codex 任务后，即可通过名称调用：

```text
使用 $shigeru-miyamoto-perspective 评审这个游戏概念。
```

如果目标目录已经存在，可在该目录中更新：

```bash
git -C ~/.codex/skills/shigeru-miyamoto-perspective pull
```

### 使用示例

**核心循环**

```text
使用 $shigeru-miyamoto-perspective 分析这个循环：
玩家捕捉风，把风装进瓶子，再释放它推动船和机关。
请指出动作—反馈中最弱的一环，并设计一个一天内可验证的原型。
```

**教程与第一次游玩**

```text
使用 $shigeru-miyamoto-perspective 检查我的前 10 分钟教程。
区分操作障碍与核心挑战，并告诉我哪些文字可以让环境来表达。
```

**新技术与差异化**

```text
使用 $shigeru-miyamoto-perspective 判断体感输入是否真的改变了玩法。
请写清假设、对照版本、观察指标和失败后的降级方案。
```

为了得到更具体的结论，最好同时提供：平台与版本、目标玩家、玩家的高频动词、输入方式，以及录像、截图、设计稿或行为数据中的至少一种。

### 工作方式

Skill 会按问题选择最相关的 1—3 个模型，而不是机械展示整套框架。涉及具体游戏或版本事实时，它优先依据：

1. 可玩构建与用户材料
2. 官方开发访谈和补丁说明
3. 完整实机视频
4. 可靠评测与行为数据
5. 二手摘要

输出通常会收敛到一个可以证伪的下一步实验，而不是只给抽象评价。

### 项目结构

```text
.
├── SKILL.md                   # Skill 主说明与完整思维模型
├── agents/openai.yaml         # Codex 显示名称与默认提示词
├── references/research/       # 研究、验证、时间线与综合材料
└── scripts/                   # 研究整理和质量检查工具
```

### 质量与诚实边界

- `SKILL.md` 已通过仓库内质量检查脚本的 6/6 项检查。
- 研究资料区分公开立场、团队证词、外部观察和模型推断。
- 不伪造引语，不使用误归于宫本茂的 “A delayed game is eventually good...” 作为其原话。
- 大型游戏是团队成果；具体贡献应以实际署名和开发记录为准。
- 调研截止日期为 **2026-07-13**，之后的新事实需要重新核验。

运行质量检查：

```bash
python3 scripts/quality_check.py SKILL.md
```

---

## English

### What it helps with

Instead of starting with story scale or feature count, this Skill begins with one chain:

> What does the player do → how does the system respond → why would the player do it again?

Use it to:

- Review a game concept and its 10–30 second core loop
- Improve movement, jumping, camera behavior, input, and immediate feedback
- Audit tutorials and the first 5 or 30 minutes of play
- Design levels, exploration spaces, items, enemies, and environmental guidance
- Test whether new technology changes player action instead of merely improving specifications
- Turn team disagreements into small, playable prototypes that can be tested quickly
- Detect content bloat, competitor imitation, and expansion before the core interaction works

It is not intended by default for films, theme parks, museums, IP licensing, or general business strategy. Author-driven narrative games, live-service systems, and specialist simulations should also be evaluated with complementary methods and real player research.

### Six core models

1. **Get the hands moving first**: action and feedback are the atoms of experience.
2. **`Dokuso`: change the playing field**: originality is not making a competitor's game bigger.
3. **Build to find out**: a prototype discovers the problem; it does not merely prove a meeting right.
4. **Borrow the eyes of a first-time player**: make entry intuitive and let depth emerge through trial and error.
5. **Let the world explain the rules**: use shape, weight, position, and consequence to create readable causality.
6. **Leave room for the player to finish the work**: provide consistent rules and discoverable clues without prescribing one experience.

See [`SKILL.md`](SKILL.md) for the complete models, evidence, limitations, and operating protocol.

### Installation

Clone the repository into your Codex skills directory:

```bash
git clone https://github.com/SherryCW/shigeru-miyamoto.git \
  ~/.codex/skills/shigeru-miyamoto-perspective
```

Start a new Codex task and invoke the Skill by name:

```text
Use $shigeru-miyamoto-perspective to review this game concept.
```

If the target directory already exists, update it in place:

```bash
git -C ~/.codex/skills/shigeru-miyamoto-perspective pull
```

### Example prompts

**Core loop**

```text
Use $shigeru-miyamoto-perspective to analyze this loop:
the player catches wind, stores it in bottles, and releases it to move boats and mechanisms.
Identify the weakest action-feedback link and propose a prototype we can test in one day.
```

**Tutorial and first play**

```text
Use $shigeru-miyamoto-perspective to audit the first ten minutes of my tutorial.
Separate control friction from the intended challenge, and show which text can be replaced by environmental teaching.
```

**New technology and differentiation**

```text
Use $shigeru-miyamoto-perspective to test whether motion input truly changes the game.
State the hypothesis, control version, observation metrics, and fallback if the idea fails.
```

For a more concrete review, include the platform and version, target players, frequent player verbs, input method, and at least one of the following: footage, screenshots, design documents, or behavioral data.

### How it works

The Skill selects the 1–3 models most relevant to the question instead of mechanically displaying the entire framework. When external facts about a particular game or version matter, it prioritizes:

1. Playable builds and user-provided materials
2. Official developer interviews and patch notes
3. Complete gameplay footage
4. Reliable reviews and behavioral data
5. Secondary summaries

Its output usually converges on a falsifiable next experiment rather than stopping at an abstract critique.

### Repository structure

```text
.
├── SKILL.md                   # Main Skill instructions and complete framework
├── agents/openai.yaml         # Codex display metadata and default prompt
├── references/research/       # Research, validation, timeline, and synthesis
└── scripts/                   # Research-processing and quality-check tools
```

### Quality and epistemic boundaries

- `SKILL.md` passes all 6 checks in the included quality-check script.
- Research materials distinguish public positions, team testimony, external observations, and model-based inference.
- The Skill does not fabricate quotations and does not attribute “A delayed game is eventually good...” to Miyamoto.
- Large games are team achievements; specific contributions should follow actual credits and development records.
- The research cutoff is **2026-07-13**. Later facts require fresh verification.

Run the quality check:

```bash
python3 scripts/quality_check.py SKILL.md
```

---

## Credits

本 Skill 由 [女娲 · Skill造人术](https://github.com/alchaincyf/nuwa-skill) 生成，创建者为 [花叔](https://x.com/AlchainHust)。

This Skill was generated with [Nuwa Skill](https://github.com/alchaincyf/nuwa-skill) and created by [花叔](https://x.com/AlchainHust).
