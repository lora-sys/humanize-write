# humanize-write

<p>
  <strong>消除 AI 味，但不要过度 — 让文字读起来自然专业</strong>
</p>

写作业、比赛计划、论文、报告时，用这套工作流把 AI 草稿变成真正有质感的内容。

---

## 效果对比

| AI 草稿（V0） | V2（自然专业） |
|---|---|
| 这是一个**fascinating**的市场机会…… | 市场规模 260 亿，头部三家占 60% 份额…… |
| 随着**数字化转型**的不断深入…… | 过去三年，这个行业的数字化投入增长了 3 倍…… |
| 这**不仅仅是**一款产品，**更是**一个解决方案…… | 产品解决了具体问题：…… |
| 综上所述，**不难发现**…… | 结果很明确：…… |

---

## V2 核心升级

**V1 问题**：去 AI 味用力过猛，导致文字过于口语化、随意。

**V2 解决方案**：

1. **风格校准器（Moderator）**：在写手和裁判之间加入 Moderator，防止过度润色
2. **自由迭代循环**：你说哪里不满意 → AI 修订 → 再审查 → 直到你说「可以了」
3. **场景风格模板（MODES）**：根据不同场景（学术/商业/作业/演讲/邮件）适配温度

---

## 工作流

```
V0 → Moderator审查 → 裁判审查 → V1
  ↑                              ↓
  ← ← ← ← ← ← ← ← ← ← ← ← ← ← ←
           （自由迭代）
                ↓
             你确认
                ↓
               V2
```

### 三步开始

**第一步 — V0：写手生成草稿**

```
场景：[学术论文/商业计划/课程作业/演讲稿/私人邮件]
主题：[你的主题]
受众：[受众描述]
目的：[目标]
口语温度偏好：[1-10，越高越口语，不填默认3-4]

参考材料：[粘贴笔记/大纲/数据]

规则：见 skills/humanize-write/RULES.md
```

**第二步 — Moderator + 裁判审查**

打开新窗口（新模型），先Moderator后裁判：

```
你在审查一份草稿是否存在「过度口语化」和「AI套话残留」问题...

规则：见 skills/humanize-write/MODERATOR.md + RULES.md
草稿：[粘贴 V0 内容]
```

**第三步 — 迭代直到满意**

V1 出来后，说出具体问题：
- 「第三段太口语了，改专业一点」
- 「第二段加个例子」
- 「可以了」→ 进入 V2 最终确认

---

## 场景风格参考

| 场景 | 口语温度 | 说明 |
|---|---|---|
| 学术论文 | 2-3 | 正式严谨，术语准确 |
| 商业计划 | 3-4 | 专业有说服力，务实 |
| 课程作业 | 4-5 | 学生腔但不过度 |
| 演讲稿 | 5-6 | 口语化，适合朗读 |
| 私人邮件 | 6-7 | 轻松自然，像朋友写信 |

详细说明见 MODES.md。

---

## 禁用词清单

以下词汇出现，读者立刻知道是 AI 写的：

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
- 「综上所述」「不难发现」「不难看出」

**过度口语化警告：**
- 语气词过多（嘛、啊、呢、哈、呀、呗）
- 感叹号过多
- 像在发微信/发语音转文字
- 网络用语、俚语（yyds、绝绝子等）

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

安装后触发词：「写作业」「写论文」「写比赛计划」「写计划」「消除AI味」「让AI写的更像人」「润色」「改稿」

---

## 文件结构

```
skills/humanize-write/
├── SKILL.md         # 技能定义和工作流（主文件）
├── RULES.md         # 反AI味核心规则 + 过度口语化规则
├── MODERATOR.md     # 风格校准器提示词
├── MODES.md         # 场景风格模板
└── EXAMPLES.md      # 完整示例
```

---

## 核心原则

1. **第一版只是 V0** — 从来不是你要接受的草稿
2. **Moderator 是平衡器** — 防止去 AI 味用力过猛，变得过于随意
3. **迭代直到满意** — 不要接受不完整的 V1，说出具体问题
4. **你才是主人** — AI 是工具，不是执笔者
5. **版本思维** — V0 搭架子 → V1 去 AI 味 + 校准平衡 → V2 注灵魂

---

## 许可证

MIT
