# 大数据与人工智能课程作业 · 个人学习仓库

本仓库用于存放《大数据与人工智能》课程的作业与个人学习资料。它既是一个**可公开访问、可继续迭代的个人学习仓库**，也是本课程作业一（用 AI 构建个人概念学习资料生成 Skill）的提交物。

## 基本信息

- 课程：大数据与人工智能
- 作者：xiaoyao-mo
- 邮箱：3435409877@qq.com
- 仓库：https://github.com/xiaoyao-mo/bigdata-ai-course

## 仓库结构

```
bigdata-ai-course/
├── .workbuddy/
│   └── skills/
│       └── concept-explainer/     # 项目级 Skill（作业一核心交付物）
│           └── SKILL.md
├── learning-materials/            # 作业一：concept-explainer 生成的概念学习资料
│   ├── agent.html                 #   概念 1：Agent（智能体）
│   ├── llm-context.html           #   概念 2：大模型的上下文（LLM Context）
│   ├── skill.html                 #   概念 3：Skill（技能包）
│   └── concept-relationship.html  #   三个概念的关系说明（含闭环示意图）
├── agent-skills/                  # 早期探索资料（Agent Skills 专题，2026-09-03）
│   └── agent-skills-学习资料.html
├── README.md
└── .gitignore
```

说明：早期资料 `agent-skills/` 为本人首次尝试用 HTML 整理学习资料的产出，作为探索过程保留；作业一要求的三份概念资料与关系说明位于 `learning-materials/`。

## 作业一核心交付物：concept-explainer Skill

- **存放路径**：项目级 Skill，位于 `.workbuddy/skills/concept-explainer/SKILL.md`（仓库根目录下的 `.workbuddy/skills/`，随 Git 版本管理，团队成员打开本仓库即可共享）。
- **它是什么**：一个"概念学习资料生成器"。SKILL.md 顶部含 YAML 元数据（`name`、`description`），正文写明了适用场景、输入要求、生成步骤、输出结构模板、资料来源要求与自检清单。
- **可复用性**：不绑定本作业的三个概念；任何新概念（如 RAG、Transformer、决策树……）都可以作为输入，按同一流程产出结构化学习资料。

### 如何在 WorkBuddy 中调用它

1. 在 WorkBuddy 中**打开本仓库目录**作为工作区（项目级 Skill 随仓库加载）；
2. 在对话中直接说明意图，例如：
   - "用 concept-explainer 学习一下『向量数据库』，输出 HTML"
   - "帮我生成『K 近邻』的概念学习资料"
   - 也可让助手对已有资料做概念辨析或补充自测题；
3. Skill 会根据 description 自动匹配触发，或按要求显式调用，按"生成步骤"产出文件到 `learning-materials/`。

（Skill 的调用说明同样写在 SKILL.md 内，方便任何协作者阅读。）

## 已生成的学习资料清单（作业一）

| 文件 | 内容 | 结构 |
|---|---|---|
| `learning-materials/agent.html` | 概念 1：Agent | 速览卡 / 学习目标 / 核心问题 / 我的理解 / 机制与组成（含 Agentic Loop 图）/ 应用场景 / 易混淆与边界 / 自测 8 题 / 参考资料 |
| `learning-materials/llm-context.html` | 概念 2：大模型的上下文 | 同上（含上下文窗口构成图、Lost in the Middle U 型曲线图）|
| `learning-materials/skill.html` | 概念 3：Skill | 同上（含 SKILL.md 结构与渐进式披露图）|
| `learning-materials/concept-relationship.html` | 三概念关系 | 定位对比表、上下文如何驱动 Agent、Skill 如何沉淀经验、三者闭环图、个人判断 |
| `agent-skills/agent-skills-学习资料.html` | 早期探索：Agent Skills 专题 | 8 章知识 + 分级测试题 15 道 |

三份概念资料均包含：个人解释、核心机制/组成、一个具体应用场景、易混淆问题与使用边界、可核查的资料来源链接。

## 作业提交记录

| 作业 | 内容 | 状态 |
|---|---|---|
| 作业一 | 项目级 Skill + 三份概念学习资料 + 关系说明 + README | 已完成（本提交） |

## AI 使用与人工核查说明

本作业按课程要求使用 AI 辅助设计与编写，并对产出进行了人工核查，过程如下：

1. **Skill 设计**：先在 AI 协助下明确 Skill 应"接收任意概念、输出固定结构"，再逐节编写 SKILL.md（适用场景 / 输入 / 步骤 / 输出结构 / 资料来源要求 / 自检清单），并通读确认其可复用性。
2. **资料生成**：调用 concept-explainer 的流程生成三份概念资料与关系说明；撰写"我的理解"部分时未整段照搬 AI 或来源原文。
3. **来源核查（重要）**：三份资料引用的全部外部链接（Anthropic 官方文章与文档、arXiv 论文、WorkBuddy 官方文档）均于 **2026-09-06** 通过独立网络检索逐一核实可访问，且文中关键论断（如 Workflow vs Agent 的控制权划分、Lost in the Middle 的 U 型曲线、SKILL.md 的 frontmatter 与渐进式披露）与原始出处比对一致；**未编造任何来源**。每份资料的"参考资料"小节都注明了检索日期。
4. **待本人复核点**（提交前建议再通读一遍）：
   - [ ] 概念口径与课堂讲授是否一致（尤其 Agent 的定义侧重）；
   - [ ] "我的理解"与个人体会是否补充了自己的例子；
   - [ ] 若课程使用不同模型的 Skill 路径约定，以官方文档为准。
5. **安全与隐私**：未上传任何 API Key、密码或个人隐私信息；`.gitignore` 已排除 `.env`、`*.key` 等敏感文件类型。本仓库内容均适合公开访问。

## 运行环境

- 本仓库内容为 Skill 定义文件与 HTML 学习资料，无需安装依赖；HTML 用浏览器直接打开即可阅读。
- 若后续课程涉及 Python 作业：Python 3.x + pandas、numpy、scikit-learn、matplotlib 等按需补充。
