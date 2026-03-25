# Trending News Aggregator

智能热点新闻聚合器 - 自动抓取多平台热点新闻，AI分析趋势，支持定时推送。

## 功能特点

- 🔥 **多平台聚合**: 自动抓取微博、知乎、百度等平台热点
- 🧠 **智能分类**: 自动分类为科技、财经、社会、国际、娱乐
- 📊 **热度评分**: 基于排名、频次、时效的加权算法
- 🆕 **增量检测**: 自动标记新增热点
- 📈 **AI趋势分析**: 一句话总结热点趋势
- ⏰ **定时推送**: 支持每天自动推送

## 快速开始

### 安装

```bash
clawdhub install trending-news-aggregator
```

### 使用

**手动获取热点**:
```
获取今日热点新闻
```

**设置定时推送**:
```
每天早上9点推送热点新闻
```

## 输出示例

```
===今日热点=== 2026-03-25 09:00
总新闻：32条 | 新增：8条

🔥高热度分类：
[1/5] 科技（12条）[热度分：95]
  1.[微博] 华为发布新芯片 [🔥98][🆕新增]
    链接：https://weibo.com/xxx
  2.[知乎] AI技术突破 [🔥92]
    链接：https://zhihu.com/xxx

📈 AI趋势分析：
今日科技板块热度最高，AI和芯片成为焦点。
```

## 配置

编辑 `config.yaml`:

```yaml
sources:
  weibo: true
  zhihu: true
  baidu: true

categories:
  tech:
    keywords: ["AI", "芯片", "华为"]
  finance:
    keywords: ["股市", "经济"]

push:
  enabled: true
  channels: ["weixin"]
  schedule: "09:00"
```

## 依赖

- OpenClaw >= 2026.3.22
- web_search tool

## License

MIT
