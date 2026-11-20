# 贡献指南

欢迎改进这个 skill。它是一个 Markdown-only 项目，改的都是文本规则，所以"写注释"和"写规则"是同一件事——措辞的精确性就是质量。

## 开始之前

先读三份，缺一不可：

1. `skills/diagnostic-study-coach/SKILL.md` —— 行为守则主体。
2. `skills/diagnostic-study-coach/references/priority.md` —— 三层优先级，融合的关键。
3. `AGENTS.md` —— 本仓库的修改铁律。

## 改什么

| 改动类型 | 落到哪里 |
| --- | --- |
| 核心行为规则 | `skills/diagnostic-study-coach/SKILL.md` |
| 某机制的细节展开 | 对应 `references/*.md`（别堆回主文件） |
| 冲突裁决新案例 | `references/priority.md` |
| 触发入口/斜杠信号 | `COMMAND_SURFACE.md` |
| 评测用例 | `EVALS.md` + `evals/cases.json` |
| 平台打包 | `platforms/*`（Lite 可省细节，核心不可省） |

## 硬性检查

提交前逐条过：

- [ ] 不违反三层优先级：内核 > 调度 > 适配，下层不覆盖上层。
- [ ] 场景开关没写死：数学场景内核全量，跨学科场景四层/真题/自检退场但底线仍在。
- [ ] 改了核心规则就在 `EVALS.md` 加对应用例，并按 A–E 组回归。
- [ ] 内核红线（SKILL.md 第十一节）一条没破。
- [ ] markdown 内部链接无断链（CI 会查）。
- [ ] `CHANGELOG.md` 记了本次改动。
- [ ] 平台 prompt 同步了新规则（如果改动影响核心）。

##  Philosophy

规则不是越多越好。每加一条，先问：它解决的是真实出现的跑偏，还是假想的边界？能被现有规则 + 链尾"求真"裁掉的，就不要新增。主文件保持精简，细节进分册。
