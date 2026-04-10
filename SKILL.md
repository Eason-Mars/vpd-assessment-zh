---
name: vpd-assessment-zh
description: 使用 Strategyzer VPD 框架诊断项目的价值主张质量和商业模式强度。触发词："这个产品有市场吗？"、"客户真的需要这个吗？"、顾问项目 DD/可行性评估、新项目 VP-Market Fit 风险评估。
---
# vpd-assessment — 价值主张诊断框架
版本：1.1.0
作者：Eason Zhang, Mars
基于：Strategyzer《价值主张设计》（Osterwalder, Pigneur, Bernarda, Smith）
模式：deep（深度）| medium（中等）| quick（快速）

## 本 Skill 做什么
使用 Strategyzer VPD 框架诊断项目的价值主张质量和商业模式强度。输出：结构化诊断报告，包含契合度评估、BM 质量评分及下一步实验建议。

**不是**填画布，而是回答：
- 这个产品是否在解决真实的、重要的客户问题？
- 价值主张是否针对了正确的 jobs/pains/gains？
- 商业模式是否足够支撑价值主张？
- 哪些假设需要优先验证？

## 何时使用
- Exploration 🌌：顾问项目 DD / 可行性评估 — 诊断客户的价值主张是否站得住脚
  - deep 模式：严肃顾问项目的完整 DD
  - medium 模式：初步项目评估、提案前诊断
- Spirit 🌟：新项目评估 — 快速 VP-Market Fit 风险评估（用 quick 模式）
- Mars 🔴：顾问群问答 — 3 分钟方向性诊断（用 quick 模式）
- 任何时候有人问："这个产品有市场吗？" / "客户真的需要这个吗？"

## 与 YC / Superpowers 框架的区别
- YC：投资人视角 — 这个值得押注吗？
- Superpowers：竞争战略 — 你的护城河是什么？
- VPD Assessment：产品-客户研究视角 — 你是否在为正确的客户解决正确的问题？
- 独特价值：机制层诊断 + 内置"下一步测什么"行动方案
- 使用顺序：VPD Assessment → Superpowers → YC（VPD 是基础层）

## 三种模式

### deep 模式（Exploration — 完整 5 步，顾问 DD）
预计时间：90-120 分钟分析

**Step 1：客户画像扫描**
读取：`{SKILL_DIR}/references/customer-jobs-trigger-questions.md`
读取：`{SKILL_DIR}/references/customer-pains-trigger-questions.md`
读取：`{SKILL_DIR}/references/customer-gains-trigger-questions.md`
- 用触发问题挖掘功能性 / 社会性 / 情感性 jobs
- 枚举 Pains（9 个触发问题）和 Gains（9 个触发问题）
- 按重要性排序 — 识别 Top 3 最未被满足的需求
- 区分：已验证事实 vs. 假设

**Step 2：价值地图分析**
读取：`{SKILL_DIR}/references/pain-relievers-trigger-questions.md`
读取：`{SKILL_DIR}/references/gain-creators-trigger-questions.md`
- 列出所有产品和服务
- 映射每个 Pain Reliever → 它解决了哪些 Pains？
- 映射每个 Gain Creator → 它创造了哪些 Gains？
- 覆盖率分析：Top Pains 和 Gains 是否被覆盖？缺口在哪里？

**Step 3：契合度诊断（3 个层次）**
- Problem-Solution Fit：这个 Pain 是真实的还是假设的？有什么证据？
- Product-Market Fit：产品在解决 Pain #1 还是 Pain #4？
- Business Model Fit：商业模式能支撑这个价值主张吗？

**Step 3b：竞品 VP 对比**
列出 2-3 个主要竞品，对每个竞品评估：
- Pain Coverage：他们的 VP 覆盖了哪些客户痛点？
- Gain Coverage：他们的 VP 创造了哪些收益？
- 差异化亮点：他们在哪里表现突出？

输出：对比矩阵（我方 vs 竞品A vs 竞品B），列：
| 维度 | 我方 VP | 竞品 A | 竞品 B |
| Pain Coverage | ... | ... | ... |
| Gain Coverage | ... | ... | ... |
| 差异化 | ... | ... | ... |

结论：
- 差异化优势：我方 VP 明显更强的地方
- 重叠风险：我方 VP 与竞品正面交锋、无差异化的地方

若无竞品信息：标注「数据不足 — 建议开展竞品研究」并跳过矩阵。

**Step 4：商业模式质量评分（7 个维度 × 0-10 分）**
读取：`{SKILL_DIR}/references/7-questions-bm-quality.md`
每个维度 0-10 分打分，识别最弱维度，提供具体改进建议。

**Step 5：下一步行动**
读取：`{SKILL_DIR}/references/six-ways-to-innovate.md`
- 推荐 1-2 个创新方向
- 识别最关键 + 最不确定的假设
- 设计 1-2 张 Test Card（假设 → 测试方法 → 成功标准）

输出格式：HTML 报告（Eason Consulting 品牌：主色 #8B3A2A，辅色 #C5963A，暖白背景）
输出模板：`{SKILL_DIR}/assets/output-template-deep.md`
QC 标准：`{SKILL_DIR}/references/10-characteristics-vp-checklist.md`（10 条全部覆盖）

---

### medium 模式（Exploration — Step 1-3 + BM 评分，初步项目评估）
预计时间：45-60 分钟分析
适用场景：初步项目评估、顾问提案前诊断

**Step 1：客户画像扫描**
读取：`{SKILL_DIR}/references/customer-jobs-trigger-questions.md`
读取：`{SKILL_DIR}/references/customer-pains-trigger-questions.md`
读取：`{SKILL_DIR}/references/customer-gains-trigger-questions.md`
- 用触发问题挖掘功能性 / 社会性 / 情感性 jobs
- 枚举 Pains（9 个触发问题）和 Gains（9 个触发问题）
- 按重要性排序 — 识别 Top 3 最未被满足的需求
- 区分：已验证事实 vs. 假设

**Step 2：价值地图分析**
读取：`{SKILL_DIR}/references/pain-relievers-trigger-questions.md`
读取：`{SKILL_DIR}/references/gain-creators-trigger-questions.md`
- 列出所有产品和服务
- 映射每个 Pain Reliever → 它解决了哪些 Pains？
- 映射每个 Gain Creator → 它创造了哪些 Gains？
- 覆盖率分析：Top Pains 和 Gains 是否被覆盖？缺口在哪里？

**Step 3：契合度诊断（3 个层次）**
- Problem-Solution Fit：这个 Pain 是真实的还是假设的？有什么证据？
- Product-Market Fit：产品在解决 Pain #1 还是 Pain #4？
- Business Model Fit：商业模式能支撑这个价值主张吗？

**Step 3b：竞品 VP 对比**
列出 2-3 个主要竞品，对每个竞品评估：
- Pain Coverage：他们的 VP 覆盖了哪些客户痛点？
- Gain Coverage：他们的 VP 创造了哪些收益？
- 差异化亮点：他们在哪里表现突出？

输出：对比矩阵（我方 vs 竞品A vs 竞品B），列：
| 维度 | 我方 VP | 竞品 A | 竞品 B |
| Pain Coverage | ... | ... | ... |
| Gain Coverage | ... | ... | ... |
| 差异化 | ... | ... | ... |

结论：
- 差异化优势：我方 VP 明显更强的地方
- 重叠风险：我方 VP 与竞品正面交锋、无差异化的地方

若无竞品信息：标注「数据不足 — 建议开展竞品研究」并跳过矩阵。

**Step 4：商业模式质量评分（7 个维度 × 0-10 分）**
读取：`{SKILL_DIR}/references/7-questions-bm-quality.md`
每个维度 0-10 分打分，识别最弱维度，提供具体改进建议。

_（medium 模式不包含 Step 5 创新方向 — 如需完整创新方向分析请使用 deep 模式）_

输出格式：Markdown 报告（500 字以内），含 BM Score 表格
输出模板：`{SKILL_DIR}/assets/output-template-quick.md`（medium 模式适配：扩展至 500 字，含 BM Score 表格）

---

### quick 模式（Spirit — Step 1-3 + 结论，约 30 分钟）

**Step 1：客户画像（压缩版）**
- 仅 Top 3 Jobs / Top 3 Pains / Top 3 Gains
- 来源：同样的触发问题，但每类只取 Top 3

**Step 2：价值地图（粗粒度）**
- 覆盖率评级：Pain Relief 和 Gain Creation 各为 高 / 中 / 低

**Step 3：契合度诊断**
- Problem-Solution Fit：🟢 绿色 / 🟡 黄色 / 🔴 红色 + 一句话原因
- Product-Market Fit：🟢 / 🟡 / 🔴 + 一句话原因
- Business Model Fit：🟢 / 🟡 / 🔴 + 一句话原因

输出：
- 1 段核心发现（最多 100 字）
- Top 3 风险
- 1 个优先验证的假设

输出格式：
- 默认：Markdown（最多 300 字）
- 若需客户交付版：HTML（Eason Consulting 品牌：主色 #8B3A2A，辅色 #C5963A）

输出模板：`{SKILL_DIR}/assets/output-template-quick.md`

## 质量标准
- 所有诊断结论必须基于所提供的信息 — 不得杜撰
- 契合度结论必须区分「已验证事实」和「未经验证的假设」
- deep 模式强制使用 10 Characteristics 清单做 QC
- 若信息不足以评估某一维度，明确标注「数据不足」

## 参考资料索引
- `references/customer-jobs-trigger-questions.md` — 客户 jobs 的 9 个触发问题
- `references/customer-pains-trigger-questions.md` — 客户 pains 的 9 个触发问题
- `references/customer-gains-trigger-questions.md` — 客户 gains 的 9 个触发问题
- `references/pain-relievers-trigger-questions.md` — pain relievers 的 9 个触发问题
- `references/gain-creators-trigger-questions.md` — gain creators 的 9 个触发问题
- `references/7-questions-bm-quality.md` — 7 维度商业模式质量评分框架
- `references/10-characteristics-vp-checklist.md` — 优秀价值主张的 10 个特征
- `references/six-ways-to-innovate.md` — 基于客户画像的 6 种创新方向

## 资产索引
- `assets/output-template-deep.md` — deep 模式报告结构（HTML，完整 5 步）
- `assets/output-template-quick.md` — quick 模式报告结构（Markdown，也是 medium 模式的基础模板）
- medium 模式：以 `assets/output-template-quick.md` 为基础，扩展至 500 字并含 BM Score 表格

## Skill 联动
- **前置条件**：无（VPD 是基础层）
- **VPD deep 之后**：→ `company-financial-analysis`（完整 DD = VP 诊断 + 财务分析）
- **VPD quick/medium 之后**：→ `consulting-report`（将发现打包成客户可交付报告）
- **并行使用**：`venture-dd`（投资人视角与 VPD 的产品-客户视角互补）
- **使用顺序**：VPD Assessment → Superpowers → YC（基础 → 战略 → 投融资）
