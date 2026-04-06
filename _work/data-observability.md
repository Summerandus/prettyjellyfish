---
title: "data observability"
title_zh: "数据可观测性"
desc: "data · systems · 2026"
desc_zh: "数据 · 系统 · 2026"
order: 1
coming_soon: false
image: /assets/images/data-observability.png
---

<div class="lang-en" markdown="1">

Every pipeline breaks eventually. The question is whether you find out before your stakeholders do.

This project is a monitoring dashboard built on top of dbt and BigQuery — tracking data freshness, row count anomalies, and schema drift across critical tables. It surfaces the invisible: the moment a upstream source went quiet, the table that grew by an order of magnitude overnight, the column that started arriving null.

## the problem

Data quality failures are usually discovered downstream — by an analyst whose numbers don't add up, or a dashboard that stops refreshing. By that point the damage is done. The pipeline failed silently, and trust erodes.

## the approach

Rather than bolting on a third-party tool, I built lightweight checks directly into the dbt DAG — tests that run on every model, thresholds that adapt to seasonal patterns, alerts that reach the right person before the wrong person notices.

> The goal wasn't to catch every anomaly. It was to make the normal state of the data legible, so that anything abnormal becomes obvious.

## outcome

Reduced mean time to detection from days to hours. More importantly: the team stopped treating data quality as someone else's problem.

</div>

<div class="lang-zh" markdown="1">

每条数据管道终究会出问题。问题在于——你是在利益相关方之前发现，还是之后。

这个项目是一个基于 dbt 和 BigQuery 构建的监控仪表盘，追踪关键数据表的数据新鲜度、行数异常和 schema 漂移。它让不可见的东西变得可见：某个上游数据源突然沉默的那一刻，某张表在一夜之间膨胀了一个数量级，某个字段开始以 null 值到达。

## 问题

数据质量故障通常在下游才被发现——某个分析师发现数字对不上，或者某个仪表盘停止刷新。到那时，损害已经造成。管道悄悄失败了，信任也在悄悄流失。

## 方法

我没有接入第三方工具，而是直接在 dbt DAG 中构建轻量级检查——每个模型都会运行的测试、能适应季节性规律的阈值、能在错误的人注意到之前通知到正确的人的告警。

> 目标不是捕捉每一个异常，而是让数据的正常状态变得清晰可读，这样任何异常都会变得显而易见。

## 结果

平均检测时间从数天缩短到数小时。更重要的是：团队不再把数据质量当作别人的问题。

</div>
