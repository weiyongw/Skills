# Claude Code Skills Collection

一组为 [Claude Code](https://docs.anthropic.com/en/docs/claude-code) 打造的自定义 Skills，覆盖写作、思考、设计、效率等场景。

## 什么是 Claude Code Skills？

Skills 是 Claude Code 的自定义指令包。把 Skill 文件夹放到 `.claude/skills/` 目录下，Claude Code 就能在对话中自动识别并调用对应能力。

详见官方文档：[Custom Slash Commands](https://docs.anthropic.com/en/docs/claude-code/slash-commands)

---

## Skills 一览

| Skill | 一句话介绍 | 适合场景 |
|-------|-----------|---------|
| [idea-forge](#idea-forge) | 把零散想法锻造成结构清晰的文章 | 录音转文字、会议纪要、随手笔记 → 成文 |
| [evergreen-writing](#evergreen-writing) | 写一篇能活十年的长青文章 | 深度内容创作、专栏写作 |
| [Humanizer-zh](#humanizer-zh) | 去除中文文本的 AI 味 | 润色 AI 生成的文稿 |
| [brainstorm](#brainstorm) | 思维陪练，帮你发散和深挖 | 想法探索、创意激发 |
| [prd](#prd) | 对话式 PRD 写作助手 | 产品需求文档、用户故事 |
| [design-sprint](#design-sprint) | 从模糊想法到设计方案 | 新功能/模块的 UI 设计探索 |
| [priority-sort](#priority-sort) | 四象限优先级排序 | 理不清待办、不知道先做哪个 |
| [quick-start](#quick-start) | 帮你迈出第一步 | 拖延症发作、不敢开始 |

---

## 详细介绍

### idea-forge

**想法锻造** — 把零散素材通过对话提炼成结构清晰的文章。

- 支持三种输入模式：对话挖掘 / 文档输入 / 混合模式
- 五个阶段：素材提取 → 观点提炼 → 观点验证 → 成文辅助 → 终审发布
- 附带完整案例（录音转文字 → 成稿）

```
idea-forge/
├── SKILL.md              # 主文件
├── stages/               # 各阶段详细指引
├── templates/            # 洞察记录 & 写作记录模板
└── examples/             # 完整案例
```

### evergreen-writing

**长青写作助手** — 专注于创作跨越时间、持续产生价值的内容。

核心理念：*写一篇能活十年的文章，比写十篇活一年的文章更有价值。*

- 五维度长青度评估：时间检验、抽象层次、人性根基、可迁移性、独特视角
- 五个阶段：诊断 → 思维挖掘 → 选题确定 → 框架讨论 → 内容产出
- 根据观点清晰度和长青度自动调整流程路径

```
evergreen-writing/
├── SKILL.md              # 主文件（理念、流程、调度）
└── stages/               # 各阶段详细指引
```

### Humanizer-zh

**去除 AI 写作痕迹** — 基于维基百科 AI 写作特征指南，覆盖 23 类常见 AI 写作模式。

5 条核心规则：
1. 删除填充短语
2. 打破公式结构
3. 变化节奏
4. 信任读者
5. 删除金句

输出包含：重写文本 + 改写报告表格 + 质量评分表格。

> 翻译自 [blader/humanizer](https://github.com/blader/humanizer)，参考 [hardikpandya/stop-slop](https://github.com/nicepkg/stop-slop)

### brainstorm

**头脑风暴助手** — 思维陪练，帮你往两个方向走：

- **发散**：横向扩展，打开思路（类似的例子？反过来想？极端情况？）
- **深挖**：纵向追问，找到根本（为什么？背后的假设？再往下一层？）

一次只问一个问题，适时总结，保持好奇。

### prd

**PRD 写作助手** — 通过对话把脑子里的想法变成研发和业务都能看懂的需求文档。

- 先问为什么，再聊做什么
- 支持 Mermaid 流程图 + ASCII 线框图
- 附带 PRD 模板和完整示例

```
prd/
├── SKILL.md              # 主文件
├── assets/               # PRD 模板
└── references/           # 示例（PRD、Mermaid、线框图）
```

### design-sprint

**设计冲刺** — 从模糊想法到可交付的设计参考文档。

工作流程：需求收敛 → 技术调研 → ASCII 批量探索（5-8 方案）→ 确认设计风格 → HTML 设计稿 → 全状态覆盖 → 需求总结归档

产出三个文件：需求总结.md、设计稿.html、全状态设计参考.html

### priority-sort

**优先级排序助手** — 艾森豪威尔四象限 + 清晰度过滤，帮你锁定当下最该做的事。

- 第一层：按紧急/重要分入四象限
- 第二层：对 Q1/Q2 任务判断清晰度（想清楚了 vs 还没想清楚）
- 产出分层行动清单 + markdown 文档

### quick-start

**启动助手** — 帮有拖延症的你在 5 分钟内进入行动状态。

核心策略：
- **2 分钟启动法**：任何任务都能拆成一个 2 分钟的第一步
- **15 分钟承诺**：不承诺做完，只承诺做 15 分钟
- **烂版本优先**：Done is better than perfect
- **情绪优先级**：做完哪件事你会最轻松？

---

## 安装使用

### 方法一：放入项目级 Skills 目录

将需要的 Skill 文件夹复制到你项目的 `.claude/skills/` 目录下：

```bash
# 示例：安装 idea-forge
cp -r idea-forge /path/to/your-project/.claude/skills/idea-forge
```

### 方法二：放入全局 Skills 目录

复制到全局配置目录，所有项目都可使用：

```bash
# macOS / Linux
cp -r idea-forge ~/.claude/skills/idea-forge

# Windows
cp -r idea-forge "$APPDATA/claude/skills/idea-forge"
```

安装后在 Claude Code 对话中直接描述需求即可触发，也可以通过 `/skill-name` 手动调用。

---

## License

MIT
