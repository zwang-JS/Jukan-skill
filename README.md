中文版 | [English](README_EN.md)

# semicon-sam

> 一个 Claude Code 技能，模拟 **@jukan05 (SemiconSam)** —— 一位以冷酷、严谨、数据驱动的视角审视芯片产业动态的半导体供应链分析师。

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-orange)](https://claude.ai/code)

---

## 这个技能能做什么

这是一个**人物技能（Character Skill）**——它编码的不是半导体的教科书知识，而是 @jukan05 的分析过滤器和表达 DNA。它让 Claude 以他独特的视角来思考问题：

- **瓶颈优先分析** —— 在讨论需求之前，先找出供给端的约束在哪里
- **机构研报三角验证** —— 交叉对比 Morgan Stanley、Citi、Deutsche Bank、JP Morgan、广发证券等机构的报告，找出共识与官方 PR 之间的落差
- **后道主导** —— 审计封装（CoWoS、EMIB、Hybrid Bonding），而不只看前道制程节点的发布会参数
- **供应链传导映射** —— 追踪短缺如何沿着 材料 → 设备 → 封装 → 测试 → 代工 → 系统 逐级放大

### 四大核心心智模型

| # | 模型 | 一句话概括 |
|---|---|---|
| 1 | **瓶颈传导与产能错配** | 需求再强也不如一次产能审计；固定成本型企业在扩产中获益最大 |
| 2 | **链式传导与持续短缺** | 短缺不会停在某个环节——它会沿着整条产业链逐级放大 |
| 3 | **机构共识差分过滤** | 分析优势来自跨区域、跨机构比较卖方报告，寻找共识与官宣之间的裂隙 |
| 4 | **后道工艺决定论** | 所有 AI 之路的尽头都是封装与 Die-to-Die 互连，而非前道光刻 |

---

## 安装方式

### 个人安装（跨项目始终可用）

```bash
# 克隆或复制技能文件夹
cp -r semicon-sam ~/.claude/skills/
```

### 项目级安装（团队共享）

```bash
# 放入任意 Claude Code 项目
cp -r semicon-sam your-project/.github/skills/
```

> **需要 Claude Code。** 本技能遵循 [agentskills.io](https://agentskills.io) 开放标准，兼容任何支持 skill-based agent routing 的平台。

---

## 使用方式

当你的提问中包含半导体供应链相关关键词时，技能会**自动隐式激活**，无需手动调用。

### 触发关键词

`半导体供应链`、`芯片短缺`、`HBM`、`CoWoS`、`先进封装`、`代工产能`、`三星半导体`、`SK 海力士`、`存储超级周期`、`设备交期`、`良率`、`MLCC`、`基板`、`PCB 材料`、`后道工艺`、`Chiplet`、`混合键合`、`晶圆制造`、`DRAM`、`NAND`、`EMIB`、`UCIe`

### 示例提问

```
> 你怎么看台积电 2027 年 CoWoS 产能扩张？能同时满足 NVIDIA Rubin 和 AMD MI455X 的需求吗？
```

```
> 考虑到 Intel 18A 良率的情况，三星代工的 2nm 竞争力与台积电 N2 相比如何？
```

```
> 汽车行业在预警「芯片短缺 2.0」。这是真实短缺，还是库存补库噪音？
```

### 预期输出风格

- 冷酷、结论先行。没有铺垫，没有 AI 味的过渡句
- 每一条判断都标注来源：`[Morgan Stanley]`、`[Citi]`、`[Channel Check]`、`[Rumor]`
- 结构化编号输出：瓶颈 → 传导 → 机构研报 → 后道检查 → 反面观点 → 受益方
- 中英混杂，信息密度高，句子短

---

## 来源与出处

本技能由三个独立的 AI 分别对 @jukan05 的 100+ 条公开推文（2024–2026 年 6 月）进行蒸馏，再交叉验证其 Substack 专栏（SemiconSam）后综合合成。三个来源蒸馏文档均保留在本仓库中：

- `grok's output.md` —— Grok 蒸馏（5 个心智模型 + 表达 DNA）
- `perplexity's output.md` —— Perplexity 蒸馏（4 个心智模型 + 写作模板）
- `gemini's output.md` —— Gemini 蒸馏（3 个心智模型 + 量化风格 + 测试用例）

整个合成过程（详见 `principle.md`）遵循 [agentskills.io](https://agentskills.io) 开放标准，包括渐进式披露、约束前置、工作流编号和已解决示例。

---

## 致谢与声明

**@jukan05 / SemiconSam** —— 本技能所模拟的原始分析师。技能捕捉的是其公开可见的分析模式和表达风格，不声称获取了其私密信息、个人身份或非公开观点。

**AI 合成** —— 三个独立的 LLM（Grok、Perplexity、Gemini）各产出一份蒸馏文档；最终的 SKILL.md 由 Claude Code 综合三份文档并遵循 `principle.md` 中的元准则合成。

**不构成投资建议。** 本技能提供的是分析视角，而非财务建议。请始终保持独立判断（DYODD）。

---

## 开源协议

[MIT](LICENSE) —— 可自由用于任何项目，个人或商业用途均可。
