# Claude Skills

A collection of reusable Claude Code skills. Project-agnostic, no private data.

Claude Code 自定义 Skill 集合。与项目代码隔离，不含任何隐私数据。

## Setup / 使用方法

Copy any `.md` file into your project's `.claude/commands/` directory. Done.

将需要的 `.md` 文件复制到目标项目的 `.claude/commands/` 目录下即可使用。

```bash
# Example: install the encouragement skill
cp encouragement.md /path/to/your-project/.claude/commands/
```

## Skills

### `/encouragement` — Session-End Encouragement / 走心鼓励

**What it does / 功能：**
Gives you a brief, genuine encouragement at the end of a session based on what you actually did — not generic praise.

每次 session 结束时，基于你本次实际做的事给出走心鼓励，不是泛泛的夸奖。

**Design principles / 设计原则：**

| Principle | 原则 |
|-----------|------|
| Be specific — every sentence ties to a real action | 每句话挂钩具体行动 |
| No sycophancy — one honest line beats five hollow ones | 不油腻 — 一句真话胜过五句空话 |
| Don't praise the wrong thing — read the room first | 不拍马腿 — 先读懂这次 session 的情绪 |
| Honest about setbacks — don't pretend everything was smooth | 有挫折就说 — 不假装一切顺利 |
| 3-5 sentences max — like a nod from a colleague, not a speech | 最多3-5句 — 像同事走过给你点个头 |

**Usage / 用法：**
```
/encouragement
```

Recommended: run at the end of every session, after wrapping up your work.

建议：每次 session 结束时使用。

---

### `/deep-research <topic>` — Deep Research / 深度调研

**What it does / 功能：**
Three-tier research (light / medium / paper-grade) with three anti-token-explosion locks and inter-phase review gates.

三级深度调研（轻量/中度/论文级）+ 三道防爆锁 + Phase 间审核门。

**Usage / 用法：**
```
/deep-research <your research topic>
```

The skill auto-detects scope and picks the appropriate depth. Each phase requires user approval before proceeding to the next.

自动判断范围选择深度。每个 Phase 完成后需用户确认才进入下一阶段。
