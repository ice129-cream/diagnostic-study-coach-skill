# 更新记录

## [1.0.0] - 2026-11-19

三套机制融合的首个版本。不是文本拼接，而是按三层优先级重构成一个有机行为层。

### 融合来源

- **内核（不可让渡）**：第一性原理诊断式学习教练——十二问链、四层能力闭环、自检闸门、
  真题为母、不给答案不泄底、三张工作台。
- **调度 + 适配**：Universal Diagnostic Tutor——诊断自适应循环、学习状态卡、掌握状态词、
  跨学科迁移、可信资源、数学格式。
- **调度**：清华 OpenMAIC——确认闸门、配置驱动分支+意图覆盖例外、契约细节下沉、按需加载。

### 结构

- `skills/diagnostic-study-coach/SKILL.md`：主守则，含三层优先级、十二问链、诊断循环、
  四层闭环、三张工作台、确认闸门、自检闸门、通用适配、刻度盘、17 条红线。
- `references/`（13 份）：
  - 融合核心（新写）：`priority.md`（三层裁决+10 冲突实例）、`loop.md`（循环映射+动作决策表）、
    `confirmation.md`（确认闸门）、`universal.md`（跨学科+状态卡+资源+格式）、`mastery.md`（掌握状态词+就绪门）。
  - 继承内核（原版落地）：`constitution.md`、`ladder.md`、`grading.md`、`exploration.md`、
    `hints.md`、`sourcing.md`、`preflight.md`、`parameters.md`。
- `examples/dialogue.md`：行为样例。
- 项目文档：README / USER_GUIDE / COMMAND_SURFACE / INSTALL / EXAMPLES / EVALS /
  QUALITY_RUBRIC / LICENSE。

### 关键设计

三层裁决：内核决定"不能做什么"，调度决定"什么时候做"，适配决定"怎么表达"，下层不覆盖上层。
场景开关：数学/专升本场景内核全量生效；跨学科场景四层/真题/自检退场，但不泄底/停等/输出为王仍成立。

### 工程文件（v1.0.1 补齐）

对齐真实 skill 项目的完整形态：

- `platforms/` 多平台适配层（9 个平台）：DSH / generic-chat 两个主入口按"三套融合+三层裁决"重写，其余 7 个从数学导师版继承。
- `.gitignore`、`AGENTS.md`（仓库修改铁律）、`CONTRIBUTING.md`。
- `.github/workflows/validate.yml`：md 链接检查 + skill 结构检查 + frontmatter 检查。
- `scripts/check-links.sh`：纯 bash 无依赖的链接检查器（CI 在 Linux runner 上跑）。
- `evals/cases.json`：EVALS.md 的结构化版本（5 组）。

> 说明：UDT 项目 193 个路径里 174 个是 md，OpenMAIC 真正的 `skills/openmaic/` 也只有 SKILL.md + 8 个 md；两者核心 skill 本质都是 Markdown。OpenMAIC 仓库的 4475 个文件里 ts/tsx/png 等是平台 Next.js 应用代码，与 skill 无关。补齐的是工程配套文件（CI/配置/适配层），不是把平台代码搬进来。

### 验证

- 对抗压测：12 个三机制冲突场景 12/12 裁决正确，3 条真实台词抽查通过。
- 结构校验：35 个 md、11 个相对链接、0 断链；必备文件齐全；cases.json 合法（5 组）。
