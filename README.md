<div align="center">

# korea-academic-skills 韩国学术生存 Skill 包

**给在韩中国研究生的 Claude Code / Codex Skill：KCI 选刊、中译韩学术润色、学位论文审查模拟问答、论文格式与查重检查。**

*Agent skills for Chinese graduate students in Korea — KCI/SSCI journal selection, Chinese→Korean academic translation, thesis-defense drills and thesis format & plagiarism-check prep.*

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skills-d97757)](#安装)
[![Codex](https://img.shields.io/badge/Codex-Skills-black)](#安装)
[![GitHub stars](https://img.shields.io/github/stars/rong0000g/korea-academic-skills?style=social)](https://github.com/rong0000g/korea-academic-skills/stargazers)

[中文](#中文) · [English](#english)

</div>

---

## 中文

### 为什么做这个

在韩国读研，难点往往不在研究本身，而在“韩国特有的规则”：KCI 등재지和등재후보지有什么区别？我们学科毕业到底要发几篇？论文要写成地道的韩语学术体，答辩委员会问什么，学校的작성 지침和카피킬러怎么过？这些信息分散在各校公告和 PDF 里。

这个仓库把**公开来源**整理成 4 个可直接调用的 AI Skill。所有规则都附有出处链接；凡是各校不同的地方，Skill 会明确提示你“以本校规定为准”，而不是编一个答案。

### 包含的 Skill

| Skill | 用途 | 依据 |
| --- | --- | --- |
| [`kci-journal-selection`](kci-journal-selection/) | 拆解本校毕业发表要求，核验 KCI 등재구분 / SSCI，建立冲刺—匹配—保底选刊梯队 | 韩国研究财团《학술지 등재제도 관리지침》、多校시행세칙示例 |
| [`zh-ko-academic-translation`](zh-ko-academic-translation/) | 中文→韩文学术翻译与润色，输出“原文/修改/理由”三栏 | 137 篇中国学习者韩语学位论文的错误研究等 |
| [`thesis-defense-drill`](thesis-defense-drill/) | 基于你的论文出 15–20 道심사委员式问题，一问一答并点评 | 学位论文审查问答整理、McGill 答辩指南 |
| [`thesis-format-check`](thesis-format-check/) | 按작성 지침检查结构、版式、页码、인준지，并准备 KCI 문헌유사도검사/카피킬러 | 多校작성 지침与查重说明 |

### 安装

#### Claude Code

```bash
git clone https://github.com/rong0000g/korea-academic-skills.git /tmp/kas && mkdir -p ~/.claude/skills && cp -r /tmp/kas/*/ ~/.claude/skills/
```

#### Codex

```bash
git clone https://github.com/rong0000g/korea-academic-skills.git /tmp/kas && mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills" && cp -r /tmp/kas/*/ "${CODEX_HOME:-$HOME/.codex}/skills/"
```

每个 Skill 是一个独立文件夹（`SKILL.md` + `references/`），也可以只复制你需要的那个。请保留 `references/` 目录，否则规则不会加载。

### 使用示例

- “用 `kci-journal-selection`：我是고려대 경제학 박사，帮我列出毕业发表要求要核对的条件。”
- “用 `zh-ko-academic-translation` 把这段中文摘要翻成韩语국문초록，不要改内容。”
- “用 `thesis-defense-drill` 根据我的论文模拟최종 심사，一次问一题。”
- “用 `thesis-format-check` 按我们学校的작성 지침检查这份论文。”

### 输出示例（仅为格式示意，非真实稿件）

```text
| 原文 | 修改后 | 理由 |
| 이 연구는 ~에 대해 좀 알아봤다. | 본 연구는 ~을/를 분석하였다. | 口语表达（좀）→ 书面学术体；人称/主语规范 |
| 그것은 중요하다. | 이러한 결과는 ~ 측면에서 중요하다. | 指代对象不明确 |
待确认：术语「○○」的韩文译法（候选 A / B）
```

### 设计原则

- **只写有来源的事实**，每个 `references/*.md` 末尾都有链接；规则因校而异时明确说明。
- 不编造期刊、审稿周期或数据；不承诺录用；不提供规避查重/AI 检测的改写。
- 本仓库不是任何学校的官方解释，最终以本校最新规定为准。

### 相关项目

- [paper-forge](https://github.com/rong0000g/paper-forge)：证据优先的通用学术写作 Skill（文献卡片、模拟审稿、投稿前检查、选刊），可与本仓库搭配使用。

### 在韩留学生服务

> 维护者可在此填写联系方式与服务说明（如：咨询、校对等）。
>
> - 联系方式：`待填写`

### 参与贡献

欢迎 PR：补充你学校/学科的公开规定（请附官方链接和入学年度）、修正错误、完善 Skill。觉得有用请点 ⭐。

---

## English

Four portable agent skills for international (especially Chinese) graduate students in Korea:

- **kci-journal-selection** – break down your department's publication requirement (KCI 우수등재/등재/등재후보, SSCI/SCIE, authorship, points) and verify journal status on kci.go.kr.
- **zh-ko-academic-translation** – Chinese→Korean academic translation and polishing, targeting the most frequent errors found in Korean theses by Chinese-speaking students.
- **thesis-defense-drill** – committee-style mock Q&A generated from your own thesis.
- **thesis-format-check** – check against your school's thesis guideline and prepare the KCI similarity check / CopyKiller step.

Install: clone the repo and copy the skill folders into `~/.claude/skills/` (Claude Code) or `$CODEX_HOME/skills/` (Codex). Every rule cites a public source; requirements differ by university, department and admission year, so always confirm with your own school. MIT licensed.
