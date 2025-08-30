---
lang: ja
lang-niv: fonto
lang-ref: 013-jbk
layout: page
title: 'メール重複クリーナー'
---

# 📧 メール重複クリーナー

複数のメールクライアント間で重複メールをスキャン・識別・削除するための包括的なPythonツールです。Web、デスクトップ、コマンドラインインターフェースを備えています。

## 🚀 バージョン

**現在のバージョン:**
[![GitHub リリース](https://img.shields.io/badge/release-v2.5.2-green)](https://github.com/Nsfr750/EmailDuplicateCleaner)
[![ドキュメント](https://img.shields.io/badge/docs-利用可能-brightgreen)](https://github.com/Nsfr750/EmailDuplicateCleaner/blob/master/README.md)
[![Python バージョン](https://img.shields.io/badge/python-3.8%20|%203.9%20|%203.10%20|%203.11%20|%203.12-blue)](https://www.python.org/)
[![ライセンス: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![PyPI](https://img.shields.io/pypi/v/email-duplicate-cleaner)](https://pypi.org/project/email-duplicate-cleaner/)
[![寄付](https://img.shields.io/badge/寄付-PayPal-green.svg)](https://paypal.me/3dmega)
[![サポート](https://img.shields.io/badge/サポート-Patreon-ff69b4.svg)](https://www.patreon.com/Nsfr750)

## ✨ バージョン2.5.2の新機能

- 🚀 バージョン2.5.2に更新
- 🐛 バージョン番号の表示を修正
- 📚 最新の変更を反映するためにドキュメントを更新

## ✨ バージョン2.5.1の新機能

- 🐛 PySide6 GUIのQActionインポートエラーを修正
- 🌐 完全な英語の翻訳を追加
- 📄 GPL-3.0ライセンスファイルを含むように
- 🔄 GUI初期化時のエラーハンドリングを改善
- ⬆️ 安定性向上のため依存関係を更新

## ✨ 特徴

### 🔍 重複検出

複数の検出基準:
- 厳密: 包括的な比較
- コンテンツのみ: メッセージ本文の分析
- ヘッダー: メタデータベースのマッチング
- 件名+送信者: 焦点を絞った識別

### 📊 メール分析

高度なメール分析:
- 送信者分析: 上位の送信者とドメインを特定
- タイムライン分析: 時間経過に伴うメールパターンの可視化
- 添付ファイル分析: ファイルタイプ、サイズ、頻度
- スレッド分析: 会話スレッドの表示と管理
- 重複分析: 詳細な重複検出の洞察
- 複数形式（テキスト、HTML、JSON）でのレポート出力

### 🖥️ マルチインターフェースサポート

- **Webインターフェース** - ダーク/ライトモード対応のモダンでレスポンシブなデザイン
- **デスクトップGUI** - PySide6を使用したネイティブなデスクトップ体験
- **コマンドラインインターフェース** - 強力な自動化とスクリプトサポート

### 🌓 強化されたユーザーエクスペリエンス

- ダーク/ライトモード対応のモダンなWebインターフェース
- リアルタイム更新付きインタラクティブプレビュー
- 包括的なヘルプシステム
- 詳細なログ記録を備えたデバッグモード
- テストと学習のためのデモモード

### 🔒 メールクライアント互換性

対応クライアント:
- Mozilla Thunderbird
- Apple Mail
- Microsoft Outlook
- 汎用mbox/maildir形式

### 🏗️ 技術的特徴

- Flaskで構築されたモダンなWebインターフェース
- データベース管理のためのSQLAlchemy
- 動的コンテンツを備えた包括的なヘルプシステム
- 関心の分離が明確なモジュール型アーキテクチャ
- クロスプラットフォーム互換性
- 広範なエラーハンドリングとロギング

## 🛠️ 前提条件

- Python 3.8以上
- pip
- サポートOS: Windows、macOS、Linux

## 🚀 クイックスタート

### 💰 プロジェクトをサポート

このツールが役立った場合は、開発をサポートしてください：

- [![寄付](https://img.shields.io/badge/寄付-PayPal-green.svg)](https://paypal.me/3dmega) PayPalでサポート
- [![サポート](https://img.shields.io/badge/サポート-Patreon-ff69b4.svg)](https://www.patreon.com/Nsfr750) パトロンになる
- :money_with_wings: **Monero (XMR)**: 
  ```
  47Jc6MC47WJVFhiQFYwHyBNQP5BEsjUPG6tc8R37FwcTY8K5Y3LvFzveSXoGiaDQSxDrnCUBJ5WBj6Fgmsfix8VPD4w3gXF
  ```

## 📦 インストール

1. リポジトリをクローン:

    ```bash
    git clone https://github.com/Nsfr750/EmailDuplicateCleaner.git
    cd EmailDuplicateCleaner
    ```

2. 依存関係をインストール:

    ```bash
    pip install -r requirements.txt
    ```

### アプリケーションの実行

#### Webインターフェース

```bash
python app.py
```

`http://localhost:5000` でアクセス

#### デスクトップGUI

```bash
python email_cleaner_gui.py
```

#### コマンドラインデモ

```bash
python email_duplicate_cleaner.py --demo
```

## 🤝 貢献

貢献に興味がありますか？[貢献ガイドライン](CONTRIBUTING.md)を確認してください！

## 📄 ライセンス

このプロジェクトはMITライセンスの下でライセンスされています。

## 🐛 問題

バグを見つけましたか？[問題を報告](https://github.com/Nsfr750/EmailDuplicateCleaner/issues)

## 📊 検出方法

- `strict`: メッセージID + 日付 + 差出人 + 件名 + 内容
- `content`: 内容のみ
- `headers`: メッセージID + 日付 + 差出人 + 件名
- `subject-sender`: 件名 + 差出人フィールドのみ

## 安全機能

- 常に各メールの少なくとも1つのコピーを保持
- デフォルトで最も古いメールを保持
- 元のメールはゴミ箱から復元可能
- 安全なテストのためのデモモード

## プロジェクト構造

- `email_cleaner_web.py`: Webインターフェース
- `email_cleaner_gui.py`: デスクトップGUI
- `email_duplicate_cleaner.py`: コア機能とCLI
- `static/`: Webアセット（CSS、JS）
- `templates/`: HTMLテンプレート

## ワークフロー

- デモモード: テストメールで実行
- ヘルプ: 使用情報を表示
- GUIモード: デスクトップインターフェースを起動
- Webモード: Webサーバーを起動

## GUI構造

- **GUI (`email_cleaner_gui.py`)**：Tkinterで構築されたユーザーフレンドリーなグラフィカルインターフェース。メールクライアントの選択、フォルダのスキャン、重複の管理を直感的に行えます。
- **CLI (`email_cleaner_cli.py`)**：ターミナルでの作業を好むユーザーのためのコマンドラインインターフェース。
- **Web (`app.py`)**：Flaskで構築されたWebベースのインターフェースで、任意のブラウザからアクセス可能。

### 補助モジュール (`struttura/`)

`struttura/` ディレクトリには、ダイアログウィンドウやメニューなど、GUIをサポートするすべての補助モジュールが含まれています。

- **`menu.py`**：メインメニューバーの作成と機能を管理し、メインのGUIファイルをクリーンに保ち、そのコアレイアウトに集中できるようにします。
- **`about.py`**、**`help.py`**、**`sponsor.py`**：`About`、`Help`、`Sponsor` ダイアログウィンドウを定義し、それぞれが独自のクラスにカプセル化されています。
- **`log_viewer.py`**：アプリケーションログを表示するシンプルなログビューア。
