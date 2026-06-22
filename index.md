---
layout: default
title: Latest Summary
---

{% assign zh_posts = site.posts | where: "lang", "zh" %}
{% assign latest_zh = zh_posts.first %}
{% assign en_posts = site.posts | where: "lang", "en" %}
{% assign latest_en = en_posts.first %}

{% if latest_zh %}
<meta http-equiv="refresh" content="0; url={{ latest_zh.url | relative_url }}">
<script>
  window.location.replace("{{ latest_zh.url | relative_url }}");
</script>
{% endif %}

# Horizon Daily

{% if latest_zh %}
正在打开最新中文日报：

[查看 {{ latest_zh.date | date: "%Y-%m-%d" }} 中文日报]({{ latest_zh.url | relative_url }})
{% else %}
暂时还没有生成中文日报。
{% endif %}

## 快速入口

- [中文归档]({{ '/feed-zh.xml' | relative_url }})
- [配置指南](configuration)
- [信息源采集器](scrapers)
- [评分系统](scoring)
- [GitHub 仓库](https://github.com/jackzhang42/Horizon)

{% if latest_en %}
## English

[Open the latest English digest: {{ latest_en.date | date: "%Y-%m-%d" }}]({{ latest_en.url | relative_url }})
{% endif %}
