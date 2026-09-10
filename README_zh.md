# Manuscript Writing Kit

[![English](https://img.shields.io/badge/lang-English-0b57d0)](README.md)
[![简体中文](https://img.shields.io/badge/lang-%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87-c41e3a)](README_zh.md)

LaTeX + BibTeX 学术写作技能包与流程说明：环境、搭骨架、写作契约、分节多轮协作、润色、引用（可选 Zotero）、文献对比表核对。

**版本：** 1.1.2 · [CHANGELOG](CHANGELOG.md) · [许可](LICENSE) · Agent 入口：[SKILL.md](SKILL.md)

## 安装

```bash
git clone https://github.com/BAK262/manuscript-writing-kit.git
cd manuscript-writing-kit
```

按你使用的 Agent 产品，把本目录注册为技能包。目录名保持 `manuscript-writing-kit`，根目录保留 `SKILL.md`。

**Cursor 类个人 skills 目录 — Windows（PowerShell）：**

```powershell
$src = "C:\path\to\manuscript-writing-kit"   # 本地 clone 路径
$dst = "$env:USERPROFILE\.cursor\skills\manuscript-writing-kit"
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.cursor\skills" | Out-Null
cmd /c mklink /J "$dst" "$src"
```

**macOS / Linux：**

```bash
mkdir -p ~/.cursor/skills
ln -s /path/to/manuscript-writing-kit ~/.cursor/skills/manuscript-writing-kit
```

复制到 skills 目录同样可用。其他 Agent 产品按其技能 / 插件说明注册即可。

更新：

```bash
cd /path/to/manuscript-writing-kit
git pull
```

## 工作环境

| 层级 | 建议 |
|------|------|
| 编辑与编译 | IDE + 插件：**Visual Studio Code** 或其变体（如 **Cursor**）；LaTeX 编译/预览扩展；本机 TeX（`pdflatex` / `bibtex` 或项目指定引擎） |
| 对话改稿 | 能读写项目文件的 Agent；在会话中加载本包（如 `/manuscript-writing-kit`，或该产品的等价方式） |

模块内路径默认相对**项目根**；以契约 §0 为准。

## 开始使用

1. 在 Agent 会话中加载本包。  
2. 指向你的主 `.tex`。  
3. 从 [prompts/request-templates.md](prompts/request-templates.md) **任选一条**模板粘贴。

| 情况 | 模板 |
|------|------|
| 新开论文 | New paper bootstrap |
| 已有初稿、摘要仍为草稿 | 小范围 **Mode A**；先自行冻结摘要，再填契约 §1–§4 |
| 摘要已定稿，调整结构 | **Mode B**（先列修改 → 确认 → 再改） |
| 摘要已定稿，只改措辞 | **Mode A** |
| 处理引用 | Citation pass |
| 段内论证顺序需重理 | Logic-chain reset，再另发一条 Mode A |

开写前：IDE 能出 PDF；已有 `manuscript/WRITING_CONTRACT.md` 且 **§0** 已填。进入引用轮时再配置 Zotero（[modules/environment.md](modules/environment.md)）。

### 模式

| 模式 | 含义 | 默认 |
|------|------|------|
| **A** | 只改措辞；保留每段主旨 | 不确定时用这个 |
| **B** | 可调段序或合并；先列出修改并等待确认 | |
| **C** | 较大重写；改科学含义前需明确说明 | |

### 主路径

```text
环境 → 骨架 + 契约 §0 → 初稿
  → 冻结摘要 → 契约 §1–§4
  → 按节：Mode B（确认）→ Mode A → 引用 / 表核
  → 投稿前核对
```

细节：[modules/bootstrap.md](modules/bootstrap.md)、[modules/collaboration.md](modules/collaboration.md)。

### 术语

| 用语 | 含义 |
|------|------|
| 冻结摘要 | 由你定稿的 abstract；正文与图表跟它对齐 |
| 写作契约 | 本篇可主张什么、如何命名（`WRITING_CONTRACT.md`） |
| 文风锚点 | 润色时对齐的样本（常为已定稿 Introduction 与前文） |
| Mode A / B / C | 见上表 |
| 引用简报 | 正文中的 `【cite: …】` 及检索约束 |
| 叙事权威 | 以冻结后的摘要为准 |

### 请求示例

```text
Mode B，范围 @main.tex Related Work。
文风锚点：摘要 + Introduction。
先列出结构修改，确认后再改。
```

## 可选配套

| 需求 | 可另载技能 | 本包内做法 |
|------|------------|------------|
| Cover letter / 投稿信 | 如 `nature-writing` | 直接用 LaTeX 写信 |
| 更偏 Nature 腔的英文 | 如 `nature-polishing` | [modules/polish.md](modules/polish.md) |

## 目录

| 路径 | 作用 |
|------|------|
| `SKILL.md` | Agent 按意图加载模块 |
| `modules/` | 环境、bootstrap、协作、契约、润色、引用、Zotero、表核、venue |
| `examples/` | 合成填写示例 |
| `prompts/request-templates.md` | 请求骨架 |

## 论文项目中的文件

| 文件 | 常见位置 |
|------|----------|
| 主 `.tex` | `manuscript/`（或契约 §0） |
| 写作契约 | `manuscript/WRITING_CONTRACT.md` |
| 冻结摘要 | `\begin{abstract}...\end{abstract}` |

空白模板：[modules/contract/contract-template.md](modules/contract/contract-template.md)。  
填写示意：[examples/example-contract.md](examples/example-contract.md)（虚构名称与伦理编号）。
