<img src="https://raw.githubusercontent.com/hubeiewuhan-creator/diagnostic-study-coach-skill/gh-pages/logo.svg" alt="logo" width="90" align="right">

# 诊断式学习教练 · diagnostic-study-coach

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![DSH skill](https://img.shields.io/badge/DSH-原生%20skill-2f6f4e.svg)](INSTALL.md)
![形态](https://img.shields.io/badge/形态-Markdown--only-blue.svg)
![来源](https://img.shields.io/badge/融合-三套机制-green.svg)
![内核](https://img.shields.io/badge/内核-十二问链%20·%20四层闭环-orange.svg)
![状态](https://img.shields.io/badge/状态-稳定-brightgreen.svg)

> 关联项目：[math-selfstudy-tutor-skill](https://github.com/hubeiewuhan-creator/math-selfstudy-tutor-skill) —— 本综合版的数学内核独立成包版本。

一个导师，没有功能菜单。**先诊断你卡在哪一层认知，再决定下一步做什么**——出题、追问、听你主讲、批改说理、放变式、建学习路径，还是查可信资源。目标是掌握，不是做完。

## 三套机制合成一个人格

这个 skill 把三套成熟机制融合成一个有机体，而不是把三份文本拼在一起：

| 来源 | 贡献的机制 | 在综合体里的位置 |
| --- | --- | --- |
| 第一性原理诊断式学习教练 | 十二问链、四层能力闭环、自检闸门、真题为母、不给答案不泄底 | **不可让渡内核** |
| Universal Diagnostic Tutor | 诊断自适应循环、学习状态卡、掌握状态词、跨学科适配、可信资源 | 统一调度层 + 通用适配层 |
| 清华 OpenMAIC | 确认闸门、配置驱动分支+意图覆盖例外、契约细节下沉、按需加载 | 统一调度层 |

**冲突时三层裁决**：内核决定"不能做什么"，调度决定"什么时候做"，适配决定"怎么表达"。下层不得覆盖上层。详见 [`priority.md`](skills/diagnostic-study-coach/references/priority.md)。

## 核心机制

- **十二问链**：学习→自学→归纳总结→自我输出→表达重构→理解→反思→迭代→聚焦深耕→抓本质→提问质疑→独立思考→**求真**（最高裁决）。
- **四层闭环**：独立做题→做懂→讲懂→举一反三讲清道理，层层以学生输出通关，是递进关卡不是可跳循环。
- **诊断循环**：澄清→诊断→干预→检查→决策→携带，只跑当前信号需要的阶段；参与式检查后停等学生。
- **三张工作台**：闭环台（默认）/ 核验台 / 探究台，彼此隔离，进场声明。
- **确认闸门**：改变状态前确认；学生已明确要求的发题不二次确认，但不免自检。
- **自检闸门**：主动出的改编题发出前六项验算，绝不发错题；学生自带真题不触发。

## 快速开始

1. 按 [`INSTALL.md`](INSTALL.md) 把 `skills/diagnostic-study-coach/` 软链到 DSH 的 skill 根目录。
2. 直接说人话：「这题不会」「我讲给你听」「批改我的推导」「给道变式」「换条件会怎样」「定理前提是什么」「给我学习路线」「继续上次」都会接住。
3. 默认：专升本高数 · 求真严格版 · Level 3 · 三项拓展全开 · 两项锁死生效。

> `/出题` `/讲题` `/批改` `/变式` `/自检` `/状态卡` 等斜杠文本只作意图信号静默识别，不当 shell 命令执行。

## 覆盖范围

- **主用场景**：专升本考纲内高数（极限连续、导数微分、中值定理、导数应用、不定积分、定积分及应用、多元微分、二重积分、微分方程、无穷级数）与线代（行列式、矩阵、矩阵运算、逆矩阵、伴随、向量组、线性相关、线性方程组、特征值特征向量、二次型）。
- **可迁移场景**：大学 STEM / AI-CS / 其他学科 / 通用学习问题——此时诊断循环与通用适配层升为主用，数学内核中"四层闭环/真题为母/自检闸门"退场，但"不泄底/停等/输出为王"仍成立。

## 文档导航

| 文档 | 用途 |
| --- | --- |
| [`skills/diagnostic-study-coach/SKILL.md`](skills/diagnostic-study-coach/SKILL.md) | 完整行为守则 |
| [`USER_GUIDE.md`](USER_GUIDE.md) | 上手教程 |
| [`COMMAND_SURFACE.md`](COMMAND_SURFACE.md) | 自然语言入口与斜杠信号 |
| [`INSTALL.md`](INSTALL.md) | 安装与更新 |
| [`EXAMPLES.md`](EXAMPLES.md) | 行为示例 |
| [`EVALS.md`](EVALS.md) | 行为评测用例 |
| [`QUALITY_RUBRIC.md`](QUALITY_RUBRIC.md) | 质量评分口径 |
| [`CHANGELOG.md`](CHANGELOG.md) | 更新记录 |

## 边界

Markdown-only，无代码依赖、无隐藏记忆、无数据库。学习状态卡可见、可复制、学生可控。不押题、不承诺分数、不伪造来源、不甩链接。数学场景坚持真题为母、不给答案不泄底。

## 许可

MIT。
