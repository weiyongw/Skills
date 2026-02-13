# Claude Code Skills by 唯庸

一组为 [Claude Code](https://docs.anthropic.com/en/docs/claude-code) 设计的中文技能包，专注于思维辅助和写作场景。

## 技能列表

| 技能 | 说明 | 适用场景 |
|------|------|----------|
| **quick-start** | 启动助手 | 有很多事要做但一直拖延、不知道从哪开始 |
| **brainstorm** | 头脑风暴助手 | 需要发散思维、深挖想法 |
| **evergreen-writing** | 长青写作助手 | 想写出经得起时间考验的文章 |

## 安装方法

1. 下载本仓库
2. 将技能文件夹复制到 Claude Code 的 skills 目录：
   - macOS/Linux: `~/.claude/skills/`
   - Windows: `%USERPROFILE%\.claude\skills\`

例如：
```bash
# 克隆仓库
git clone https://github.com/your-username/claude-code-skills.git

# 复制技能（macOS/Linux）
cp -r claude-code-skills/quick-start ~/.claude/skills/
cp -r claude-code-skills/brainstorm ~/.claude/skills/
cp -r claude-code-skills/evergreen-writing ~/.claude/skills/
```

## 技能详情

### quick-start（启动助手）

**解决的问题**：有很多事情要做，但就是不敢开始。

**核心理念**：你不是懒，你是"不敢开始"。一旦开始，你会进入心流。

**工作方式**：
1. 倾听你脑子里在转的所有事情
2. 帮你找到"今天的那一件事"
3. 把任务拆解到"不可能失败"的第一步（2分钟内能完成）
4. 消除启动障碍
5. 让你立刻开始

**触发词**：
- "我有很多事要做"
- "不知道从哪开始"
- "一直在拖"
- "帮我理一下"

---

### brainstorm（头脑风暴助手）

**解决的问题**：想法太散，需要有人帮忙梳理和扩展。

**两种模式**：
- **发散**：横向扩展，打开思路（还有什么例子？反过来呢？极端情况？）
- **深挖**：纵向追问，找到根本（为什么？背后的假设是什么？再往下一层？）

**交互方式**：
- 你说一个想法
- 助手判断适合发散还是深挖，然后问一个问题
- 周期性帮你总结已经聊到的点

**关键原则**：一次只问一个问题，保持好奇，不急着给结论。

---

### evergreen-writing（长青写作助手）

**解决的问题**：写的东西过几个月就没人看了，想写出能持续产生价值的内容。

**什么是长青内容**：
- 讲原理而非工具（工具会变，原理不变）
- 基于人性和底层逻辑（人性千年不变）
- 十年后读依然有价值

**工作流程**：

```
用户提出想法
    ↓
[诊断] 评估观点清晰度 + 长青度
    ↓
[思维挖掘] 挖掘底层洞察（如需要）
    ↓
[选题确定] 锁定长青选题
    ↓
[框架讨论] 组织结构
    ↓
[内容产出] 写出文章
```

**长青度评估维度**：
1. 时间检验：十年后还有人想读吗？
2. 抽象层次：讲工具还是原理？
3. 人性根基：是否基于不变的人性？
4. 可迁移性：能应用到其他领域吗？
5. 独特视角：只有你能讲吗？

**触发词**：
- "我想写..."
- "帮我梳理选题"
- "怎么形成框架"

## 文件结构

```
Skills/
├── README.md
├── quick-start/
│   └── skill.md
├── brainstorm/
│   └── SKILL.md
└── evergreen-writing/
    ├── SKILL.md
    └── stages/
        ├── 00-diagnosis.md
        ├── 01-mining.md
        ├── 02-topic.md
        ├── 03-framework.md
        └── 04-writing.md
```

## 作者

**唯庸**

## License

MIT
