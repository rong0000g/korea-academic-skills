---
name: thesis-defense-drill
description: Run a mock Korean thesis defense (학위논문 심사 / 디펜스) drill for graduate students, generating committee-style questions from the user's own thesis and coaching concise answers in Korean or Chinese. Use when the user is preparing for a proposal or final degree-thesis examination.
---

# 学位论文审查（학위논문 심사）模拟问答

开始前完整读取 [references/committee-questions.md](references/committee-questions.md)。

## 工作流程

1. 让用户提供论文（或摘要、目录、研究方法与主要结果），并说明是 프로포절 심사 还是 최종 심사、答辩语言（韩/英/中）、委员人数与背景（若知道）。
2. **只根据用户论文出题**：按参考文件的五个来源（主题必要性、对象与样本、方法与测量、结果解释、局限与启示）及“研究目的一句话/1分钟/5分钟”准备，生成 15–20 题。论文没有涉及的内容不要假设成事实。
3. **一次一题**，扮演심사위원（可按用户指定的语言提问），等用户回答后点评：结论是否先行、是否给出依据、是否主动承认局限（三段式），并给出更精炼的示范回答（示范只能使用论文中已有的信息）。
4. 记录答得薄弱的题，最后输出：薄弱点清单、需在论文中补强的位置、需提前标好页码的表/图/数字。
5. 可选：按 D-30 / D-14 / D-7 / D-3 / D-1 生成准备计划。

## 边界

- 委员会构成、审查形式和评分由各校规定（如人准纸签名人数），以学校通知为准。
- 不编造文献或数据来“救场”；不知道就练习如何诚实说明并提出后续计划。
