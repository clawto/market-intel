---
name: market-intel
description: "金融市场情报聚合系统：恐慌指数、指数行情、市场要闻、财经日历。Trigger on: 恐慌指数, 恐惧贪婪, fear greed, 行情, 指数, 大盘, 股价, 要闻, 快讯, 财经日历, 宏观事件, NFP, FOMC, CPI, PPI, PMI, LPR, 非农, 美联储, 欧央行"
version: 1.0.0
license: MIT
---

# Market Intel 📊

金融市场情报聚合系统 — 对标 investing.com 核心功能，全免费数据源。

## What it does

- **恐慌贪婪指数**: 美股(CNN) + 加密货币双市场实时情绪，含分化分析和策略建议
- **指数行情**: A股(上证/深证/沪深300/科创50/创业板) + 美股(纳斯达克/标普500/道琼斯)
- **市场要闻**: CNBC + MarketWatch RSS 实时快讯
- **财经日历**: 本周/下周重要宏观事件（FOMC、NFP、CPI、ECB等）

## Scripts

| Script | Trigger | Purpose |
|--------|---------|---------|
| `scripts/fear-greed.sh` | 恐慌指数/恐惧贪婪 | 双市场恐慌贪婪指数快照 |
| `scripts/quotes.sh` | 行情/指数/大盘 | A股+美股指数实时行情 |
| `scripts/news.sh` | 要闻/快讯 | CNBC+MarketWatch市场快讯 |
| `scripts/ecal.sh` | 财经日历/日历 | 本周/下周宏观事件安排 |

## Data Sources

| 来源 | 用途 | 费用 |
|------|------|------|
| Alternative.me | Crypto Fear & Greed | 免费 |
| CNN Dataviz API | 美股 Fear & Greed | 免费 |
| 东方财富 push2 API | A股+美股指数行情 | 免费 |
| CNBC RSS | 美股市场要闻 | 免费 |
| MarketWatch RSS | 美股市场头条 | 免费 |

## Output Style

- 纯 ASCII 标题 `===== 恐慌贪婪指数 =====`（手机安全不折行）
- 5颗星评级 `★★☆☆☆` 替代进度条（直观不错位）
- 简洁一行一条指数行情