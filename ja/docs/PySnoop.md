---
lang: ja
lang-niv: fonto
lang-ref: 020-jbk
layout: doc
order: 11
title: 'PySnoop'
---

# PySnoop

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.7+](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

磁気ストライプカードの読み取り、書き込み、分析を行うためのモダンなPythonベースのアプリケーションです。このプロジェクトは、元のStripeSnoopプロジェクトを継承し、モダンなPythonとユーザーフレンドリーなインターフェースで再構築されました。

## ✨ 特徴

- **カード読み取り**: 互換性のあるリーダーで磁気ストライプカードを読み取り
- **データベース管理**: カードデータを安全に保存・管理
- **複数フォーマット対応**: 様々な形式でカードデータをエクスポート/インポート
- **モダンなGUI**: テーマ対応の使いやすいインターフェース
- **クロスプラットフォーム**: Windows、macOS、Linuxで動作
- **スタンドアローン実行ファイル**: 配布が容易な単一の実行ファイルにビルド可能
- **デバッグビルド**: トラブルシューティングのための特別なデバッグ構成
- **セキュリティ**: 機密性の高いカードデータを安全に保存
- **検証**: 組み込みのカード番号検証（C10/ルーンチェックサム）
- **ドキュメント**: 包括的なドキュメントと例

## 🚀 インストール

### 前提条件

- Python 3.7 以上
- pip（Pythonパッケージマネージャー）
- Git（オプション、開発用）

### クイックスタート

1. リポジトリをクローン:

   ```bash
   git clone https://github.com/Nsfr750/PySnoop.git
   cd PySnoop
   ```

2. 仮想環境を作成して有効化:

   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. 依存関係をインストール:

   ```bash
   pip install -r requirements.txt
   ```

## 🏗️ アプリケーションのビルド

PySnoopはNuitkaを使用してスタンドアローン実行ファイルにビルドできます。2つのビルドスクリプトを用意しています：

### デバッグビルド

```bash
.\snoop_debug.bat
```

これは、トラブルシューティング用にコンソールウィンドウが有効なデバッグバージョンのアプリケーションを作成します。

### リリースビルド

```bash
.\snoop.bat
```

これは最適化されたリリースバージョンのアプリケーションを作成します。

### ビルド出力

- デバッグビルド: `build\PySnoop_debug.exe`
- リリースビルド: `build\PySnoop.exe`

## 🛠️ 開発
   ```bash
   pip install -r requirements.txt
   ```

## 💻 使い方

### GUIモード（推奨）

```bash
python pysnoop_gui.py
```

### コマンドラインインターフェース

```bash
python pysnoop.py [オプション]
```

### 利用可能なオプション

```bash
-h, --help      ヘルプメッセージを表示して終了
-v, --verbose   詳細な出力を有効化
--version       バージョン情報を表示
```

## 🔌 対応デバイス

- MSR605 磁気ストライプカードリーダー/ライター
- その他のHID互換カードリーダー（実験的）

## 📚 ドキュメント

詳細なドキュメント、APIリファレンス、使用例については、[ドキュメント](https://nsfr750.github.io/PySnoop/ "PySnoop ドキュメント")をご覧ください。

## 🤝 貢献

貢献は大歓迎です！[貢献ガイドライン](CONTRIBUTING.md)をお読みの上、ご参加ください。

## 📄 ライセンス

このプロジェクトはGPLv3ライセンスの下で公開されています。詳細は[LICENSE](LICENSE)ファイルをご覧ください。

## 🙏 サポート

このプロジェクトがお役に立てば、開発のサポートをご検討ください：

[![PayPalで寄付](https://img.shields.io/badge/寄付-PayPal-blue.svg)](https://paypal.me/3dmega)
[![Patreonでサポート](https://img.shields.io/badge/サポート-Patreon-orange.svg)](https://www.patreon.com/Nsfr750)

## 📧 お問い合わせ

ご質問やサポートが必要な場合は、イシューを開くか、[Nsfr750](mailto:nsfr750@yandex.com)までご連絡ください。

## クレジット

- オリジナルのStripeSnoopプロジェクト (http://stripesnoop.sourceforge.net) を基にしています

## 貢献

貢献は大歓迎です！プルリクエストをお気軽に送信してください。
