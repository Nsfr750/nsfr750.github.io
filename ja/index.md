---
lang: ja
lang-niv: fonto
lang-ref: 000-jbk
layout: index
title: 'ホーム'
---

# プロジェクトハブへようこそ

こんにちは！Nsfr750と申します。情熱的な開発者でオープンソース愛好家です。ここでは私のプロジェクトや考え方、発見を世界と共有しています。

## 最新のブログ記事

{% for post in site.posts limit:3 %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | strip_html | truncatewords: 30 }}

[続きを読む...]({{ post.url }})

{% endfor %}

[すべての記事を見る](blog) | [カテゴリ別に表示](categories)

## 注目のプロジェクト

人気のオープンソースプロジェクトをいくつかご紹介します：

- [3D フィラメントマネージャー](https://github.com/Nsfr750/3D_Filament_Manager) - 3Dプリント用フィラメントを簡単に管理
- [CDE550 シミュレーター](https://github.com/Nsfr750/CDE550-sim) - 日本電産CDE550モーターコントローラー用シミュレーター
- [メール重複クリーナー](https://github.com/Nsfr750/EmailDuplicateCleaner) - 重複メールを効率的に整理

[すべてのプロジェクトを見る](projects)

## お問い合わせ

- [プロフィール](about) - 私の仕事や興味について
- [ドキュメント](docs) - プロジェクトの詳細ガイド
- [サポート](support) - 私の活動を応援する
- [お問い合わせ](contact) - コラボレーションや質問はこちら

---

最終更新日: {{ site.time | date: "%Y年%-m月%-d日" }}
