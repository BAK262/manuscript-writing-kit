# Manuscript Writing Kit（中文说明）

面向人读的入口。机器路由见 [SKILL.md](SKILL.md)。English: [README.en.md](README.en.md) · 总入口: [README.md](README.md)

**版本：** 1.1.1 · [CHANGELOG](CHANGELOG.md)

## 这是什么

一套可复用的「人 + Agent」学术写作流程说明与可加载技能包，覆盖：

- 写作环境与编译约定  
- 从搭骨架到人定摘要、再写写作契约（writing contract）  
- 分章节、多轮协作（结构整理 / 语言润色 / 引用与表格核对）  
- 可选的本地文献库（Zotero）检索约定  

适用于 LaTeX + BibTeX 文稿。论文故事写在**你自己项目里**的 `WRITING_CONTRACT.md`；本仓库提供框架、模板与合成示例。

## 推荐工作方式

| 层级 | 建议 |
|------|------|
| 编辑与编译 | **IDE + 插件**：Visual Studio Code，或其变体（如 **Cursor**）；安装 LaTeX 编译/预览类扩展；本机有 TeX 发行版 |
| 对话改稿 | 任意能读改仓库文件的 **Agent 工具**；在会话中**加载本技能包**（或按该产品的方式引用 `SKILL.md` / 模块） |
| 技能安装位置 | 视 Agent 产品而定；若使用 Cursor 等兼容「个人 skills 目录」的宿主，见下方安装 |

流程不绑定单一聊天产品；模块文案里出现的路径示例，以「项目根相对路径 + 你的 contract §0」为准。

## 安装（推荐 Fork）

**建议先 Fork 再克隆**：便于 `git pull` 上游更新，也便于在自己的分支里沉淀实验室习惯。

1. 在 GitHub Fork：https://github.com/BAK262/manuscript-writing-kit  
2. 克隆你的 Fork：

```bash
git clone https://github.com/<你的用户名>/manuscript-writing-kit.git
cd manuscript-writing-kit
git remote add upstream https://github.com/BAK262/manuscript-writing-kit.git
```

3. 拉取上游更新（需要时）：

```bash
git fetch upstream
git merge upstream/main   # 或 rebase，按你的习惯
```

4. 让 Agent 宿主能发现本包（目录名保持 `manuscript-writing-kit`，根目录保留 `SKILL.md`）：

**Cursor 等使用 `~/.cursor/skills/` 的宿主 — Windows PowerShell 联接：**

```powershell
$src = "C:\path\to\your\fork\manuscript-writing-kit"
$dst = "$env:USERPROFILE\.cursor\skills\manuscript-writing-kit"
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.cursor\skills" | Out-Null
cmd /c mklink /J "$dst" "$src"
```

**macOS / Linux 符号链接：**

```bash
mkdir -p ~/.cursor/skills
ln -s /path/to/your/fork/manuscript-writing-kit ~/.cursor/skills/manuscript-writing-kit
```

也可直接把仓库复制到对应 skills 目录。其他 Agent 产品：按其「技能 / 插件 / 提示词包」文档注册本文件夹。

## 开始使用

1. 在 Agent 会话中加载本包（例如 Cursor 中使用 `/manuscript-writing-kit`，或其他产品中的等价操作）。  
2. 引用（@）你的主 `.tex`。  
3. 从 [prompts/request-templates.md](prompts/request-templates.md) **只选一条**模板粘贴。

| 你的情况 | 使用模板 |
|----------|----------|
| 新开论文 | New paper bootstrap |
| 已有初稿、摘要尚未由你定稿 | 小范围 **Mode A**；先由你冻结摘要，再填契约 §1–§4 |
| 摘要已定稿，要调段落结构 | **Mode B**（先列修改点 → 你确认 → 再改） |
| 摘要已定稿，只改措辞 | **Mode A** |
| 补全 / 核对引用 | Citation pass |
| 论证顺序不对 | Logic-chain reset，然后**另发一条** Mode A |

**开写前最低配置：** IDE 能编译出 PDF；项目里有 `manuscript/WRITING_CONTRACT.md` 且 **§0** 已填。Zotero 等文献库接口在进入「引用轮」再配置即可（见 [modules/environment.md](modules/environment.md)）。

### 模式（三行）

| 模式 | 含义 | 不确定时 |
|------|------|----------|
| **A** | 只改措辞；保留每段主旨 | **先选这个** |
| **B** | 可调段序/合并；**必须先列出修改并等你确认** | |
| **C** | 较大重写；改科学含义需你明确要求 | |

### 主路径

```text
环境就绪 → 搭骨架 + 契约 §0 → 初稿
  → 你冻结摘要 → 契约 §1–§4
  → 按节：Mode B（确认）→ Mode A → 引用 / 表核
  → 投稿前核对
```

细节：[modules/bootstrap.md](modules/bootstrap.md)、[modules/collaboration.md](modules/collaboration.md)。

### 术语

| 用语 | 含义 |
|------|------|
| 冻结摘要 | 由你定稿的 abstract；之后正文与图表跟它对齐 |
| 写作契约 | 本篇可主张什么、如何命名（`WRITING_CONTRACT.md`） |
| 文风锚点 | 润色时对齐的样本（常为已定稿 Introduction + 前文） |
| Mode A/B/C | 见上表 |
| 引用简报 | 正文 `【cite: …】`，作者给出的检索约束 |
| 叙事权威 | 冻结后的摘要优先 |

### 请求示例

```text
较弱：把 Related Work 改好看一点（结构和用词一起改）。
较强：Mode B，范围 @main.tex Related Work。
      文风锚点：摘要 + Introduction。先列出结构修改，等我确认后再改。
```

## 可选配套技能

| 需求 | 可加载的技能名 | 仅用本包时 |
|------|----------------|------------|
| Cover letter / 投稿信 | `nature-writing` 等 | 用普通 LaTeX 写信 |
| 更偏 Nature 腔英文 | `nature-polishing` | 使用本包 `modules/polish.md` |

## 目录结构

| 路径 | 作用 |
|------|------|
| `SKILL.md` | Agent 路由（按意图加载模块） |
| `modules/` | 环境、bootstrap、协作、契约、润色、引用、Zotero、表核、venue |
| `examples/` | 合成填写示例 |
| `prompts/request-templates.md` | 可复制请求骨架 |

## 每篇论文侧文件

| 文件 | 常见位置 |
|------|----------|
| 主 `.tex` | `manuscript/`（或契约 §0） |
| 写作契约 | `manuscript/WRITING_CONTRACT.md` |
| 冻结摘要 | 主 tex 中 `\begin{abstract}...\end{abstract}` |

模板：`modules/contract/contract-template.md`。

## 隐私与再分发

- 核心模块使用可发现路径与配置占位。  
- `examples/example-contract.md` 为虚构数据集与伦理编号。  
- 个人 MCP 安装路径保留在本机；仓库内仅使用占位符示例。

## 许可

MIT — [LICENSE](LICENSE)
