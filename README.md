# 🤖 AI News Summary Agent

> 基于 **Xiaomi MiMo-V2.5-Pro** 的每日 AI 行业资讯摘要 Agent，自动分析多个话题并生成结构化日报。

---

## ✨ 功能亮点

- 🔍 **多话题并行分析** — 同时覆盖 5 个 AI 行业核心话题
- 🧠 **AI Agent 驱动** — 使用 MiMo-V2.5-Pro 模型进行智能摘要与洞察提炼
- 📊 **结构化输出** — JSON 摘要 + Markdown 日报双格式
- 💾 **自动存档** — 每日报告以日期命名本地保存
- 🔌 **零依赖** — 仅使用 Python 标准库，无需 pip 安装

---

## 🚀 快速开始

### 1. 获取 MiMo API Key

前往 [Xiaomi MiMo 开放平台](https://platform.xiaomimimo.com) 注册并获取 API Key。

### 2. 配置 API Key

打开 `agent.py`，找到顶部配置区，将 API Key 填入：

```python
MIMO_API_KEY = "your-mimo-api-key-here"
```

### 3. 运行 Agent

```bash
python agent.py
```

---

## 📋 输出示例

```
==================================================
🤖 AI News Summary Agent 启动
📅 日期：2026-05-15
📌 话题数：5
==================================================

[1/5] 正在分析话题：大语言模型最新进展 ...
  ✅ 完成 — 重要性: 5/5, 趋势: 上升

[2/5] 正在分析话题：AI编程工具 ...
  ✅ 完成 — 重要性: 4/5, 趋势: 上升
...

📝 正在生成综合日报...
  ✅ 日报生成完成

💾 报告已保存：ai_report_20260515.md
```

生成的日报（`ai_report_YYYYMMDD.md`）示例：

```markdown
# 🤖 AI 行业每日简报 — 2026年05月15日

## 📋 各话题详细摘要

### 大语言模型最新进展  ⭐5/5  上升
- 多家头部厂商密集发布新模型
- 推理效率持续提升，成本大幅下降
- 开源与闭源模型差距持续缩小

> **总结：** LLM 进入精细化竞争阶段...

## 🗞️ 综合日报

📌 今日最重要的 3 条核心洞察
1. ...
```

---

## ⚙️ 自定义配置

在 `agent.py` 顶部的配置区可以修改：

```python
# 关注的话题列表（可随意增减）
TOPICS = [
    "大语言模型最新进展",
    "AI编程工具",
    "国内AI公司动态",
    "开源模型发布",
    "AI应用落地案例",
]
```

---

## 🏗️ 项目结构

```
ai-news-agent/
├── agent.py          # 主程序（Agent 核心逻辑）
├── README.md         # 项目说明
└── ai_report_*.md    # 自动生成的每日报告（运行后出现）
```

---

## 🔧 技术实现

| 组件 | 说明 |
|------|------|
| 模型 | Xiaomi MiMo-V2.5-Pro |
| 调用方式 | REST API（OpenAI 兼容格式） |
| 运行环境 | Python 3.8+ |
| 外部依赖 | 无（仅标准库） |

Agent 工作流程：

```
用户启动 → 遍历话题列表
    → [Agent] 生成结构化 JSON 摘要（每个话题）
    → [Agent] 整合所有摘要生成综合日报
    → 保存为 Markdown 文件
    → 终端预览
```

---

## 💡 申请 MiMo Token Plan 说明

本项目专为 [Xiaomi MiMo Orbit 百万亿 Token 创造者激励计划](https://100t.xiaomimimo.com) 设计。

- **使用模型**：MiMo-V2.5-Pro
- **典型 Token 消耗**：每次运行约 15,000 ~ 30,000 tokens
- **使用场景**：每日定时运行，积累 AI 行业资讯数据库

---

*由 AI News Agent powered by Xiaomi MiMo-V2.5-Pro 自动生成*
