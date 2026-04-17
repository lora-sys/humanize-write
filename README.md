# humanize-write

<p>
  <strong>消除 AI 味，让文字像人写的</strong>
</p>

写作业、比赛计划、论文、报告时，用这套工作流把 AI 草稿变成真正有质感的内容。

---

## 效果对比

| AI 草稿（V0） | humanize 后（V2） |
|---|---|
| 这是一个**fascinating**的市场机会…… | 市场规模 260 亿，头部三家占 60% 份额…… |
| 随着**数字化转型**的不断深入…… | 过去三年，这个行业的数字化投入增长了 3 倍…… |
| 这**不仅仅是**一款产品，**更是**一个解决方案…… | 产品解决了具体问题：…… |
| 综上所述，**不难发现**…… | 结果很明确：…… |

---

## 工作流

```
V0（AI草稿）→ 裁判审查 → V1（AI自修）→ 人类润色 V2
```

### Step 1 — V0：写手生成草稿

```
写一篇关于[主题]的[格式]。
受众是[受众]。
目的是[目标]。

参考材料：[粘贴笔记/大纲/数据]

规则：见 skills/humanize-write/RULES.md
```

### Step 2 — 裁判审查

打开新窗口（新模型），输入：

```
你在审查一份草稿是否存在AI味和风格问题。不要重写。

这是规则：[粘贴 RULES.md 全部内容]
这是草稿：[粘贴 V0 内容]

对每个违规问题，用一句话指出怎么修。
```

### Step 3 — V1：AI 修订

把裁判意见甩给写手窗口：

```
这是你原来的草稿和审查报告。
[粘贴审查报告]

重写，只修这些问题。结构和论点不变。
```

### Step 4 — V2：人类最后一遍

**你才是稿件真正的主人。**

- **结构**：段落顺序是你口头给朋友讲这个故事的逻辑吗？
- **准确**：数字、人名、结论是你确认过的吗？AI 会一本正经地胡说八道。
- **质感**：这篇文章看起来像你写的吗？符合你的立场和风格吗？

---

## 安装

```bash
# Claude Code
npx skills add lora-sys/humanize-write

# Cursor
npx skills add lora-sys/humanize-write -a cursor

# Windsurf
npx skills add lora-sys/humanize-write -a windsurf

# Cline
npx skills add lora-sys/humanize-write -a cline

# GitHub Copilot
npx skills add lora-sys/humanize-write -a github-copilot
```

安装后触发：**「写作业」「写论文」「写比赛计划」「消除 AI 味」「让 AI 写的更像人」**

---

## 禁用词清单

以下词汇出现在文字里，读者立刻知道是 AI 写的：

| 禁用词 | 禁用词 | 禁用词 |
|---|---|---|
| amazing | fascinating | mind-blowing |
| groundbreaking | paradigm-shifting | transformative |
| pivotal | delve | realm |
| tapestry | vibrant | leverage |
| harness | seamlessly integrates | crucial |
| unlock the potential | — | — |

**禁止句式：**
- 「这不仅仅是 X，更是 Y……」
- 「X 不仅仅是 Y，它是 Z……」
- 「这就是 X 发挥作用的地方……」
- 「既然我们已经探讨了 X，下面让我们看看 Y」

**禁止套话：**
- 「在当今快节奏的世界」
- 「随着我们要应对复杂性」
- 「综上所述」

---

## 核心原则

1. **第一版只是 V0** — 从来不是你要接受的草稿
2. **你才是主人** — AI 是工具，不是执笔人
3. **版本思维** — V0 搭架子 → V1 去 AI 味 → V2 注灵魂

---

## 文件结构

```
skills/humanize-write/
├── SKILL.md      # 技能定义和工作流
├── RULES.md      # 反 AI 味核心规则
└── EXAMPLES.md   # 完整示例
```

---

## 许可证

MIT
