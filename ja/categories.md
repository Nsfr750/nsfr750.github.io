---
lang: ja
lang-niv: fonto
lang-ref: 003-jbk
layout: page
title: 'カテゴリ'
---

# ブログカテゴリ

興味のあるコンテンツを見つけるために、カテゴリ別に記事を閲覧できます。

## メインカテゴリ

- [ブログ](/category/blog/) - 一般的な更新情報や考え
- [プロジェクト](/category/projects) - 私の作品集
- [チュートリアル](/category/tutorials) - ステップバイステップガイド
- [テクノロジー](/category/technology) - 技術的な洞察とレビュー
- [開発](/category/development) - プログラミングとコーディングのトピック

## 最新の投稿

{% for post in site.posts limit:5 %}

### [{{ post.title }}]({{ post.url }})

{{ post.date | date: "%Y年%-m月%-d日" }} | {{ post.categories | join: '、' }}

{{ post.excerpt | strip_html | truncatewords: 30 }}

[続きを読む...]({{ post.url }})

{% endfor %}

[すべての投稿を見る](/archive) | [RSSで購読する](/feed.xml)

---

最終更新日: {{ site.time | date: "%Y年%-m月%-d日" }}
