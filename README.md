# skill-oil-brief 🛢️

原油简报生成工具 — Crude Oil Briefing Skill for Claude Code

生成结构化原油日报，覆盖 **当前趋势、技术分析、关键支撑/阻力位、消息面分析、研报观点、市场情绪、交易计划、价格预测、风险提示、AI 总结** 十一大维度。

## 数据源

| 数据 | 来源 |
|------|------|
| Brent 原油 | Yahoo Finance `BZ=F` |
| WTI 原油 | Yahoo Finance `CL=F` |
| 上海原油期货 (SC) | Pandadata 期货接口 |
| 美国原油库存 | EIA Open API |
| 实时新闻 | Google News RSS |

## 快速开始

```bash
# 安装依赖
pip install -r requirements.txt

# 配置 Pandadata 凭证
cp .env.template .env
# 编辑 .env 填入你的 Pandadata 账号和 EIA API Key

# 生成原油简报（默认分析 Brent）
python -m oil_brief --output 原油简报.md

# 分析其他品种
python -m oil_brief --variety WTI --output 原油简报_WTI.md
python -m oil_brief --variety SC --output 原油简报_SC.md
```

## 输出示例

```
# 📊 原油日报 — Brent 原油

| 品种 | 最新价 | 日涨跌幅 |
|------|--------|----------|
| Brent 原油 | 93.43 美元/桶 | +2.66% |
| WTI 原油 | 86.61 美元/桶 | +2.01% |
| 上海原油期货 (SC) | 531.00 元/桶 | -3.17% |
```

完整 11 章中文 Markdown 报告。

## 许可证

GPL-3.0

## 作者

- **xixihaha-dzh** — 作者与维护者
