---
lang: ja
lang-niv: fonto
lang-ref: 016-jbk
layout: page
title: 'NFC'
---

# 🚀 NFCリーダー/ライターアプリケーション

[![ライセンス: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![コードスタイル: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

PySide6ベースの強力なNFCタグリーダー/ライターアプリケーションで、高度な機能とユーザーフレンドリーなインターフェースを備えています。

## インストール

### 前提条件

- Python 3.9以上
- NFCリーダーハードウェア（ACR122U、ACR1252Uなど）

### クイックスタート

1. リポジトリをクローン:

   ```bash
   git clone https://github.com/Nsfr750/NFC.git
   cd NFC
   ```

2. 仮想環境を作成して有効化:

   ```bash
   python -m venv venv
   .\venv\Scripts\activate  # Windows
   source venv/bin/activate  # Linux/Mac
   ```

3. 依存関係をインストール:

   ```bash
   pip install -r requirements.txt
   ```

4. アプリケーションを実行:

   ```bash
   python main.py
   ```

詳細なインストール手順については、[PREREQUISITES.md](PREREQUISITES.md)を参照してください。

## 特徴

- **マルチタグサポート**: 以下の様々なNFCタグタイプを包括的にサポート:
  - NTAG（NTAG213、NTAG215、NTAG216）
  - MIFARE Classic（1K、4K）
  - MIFARE Ultralight
  - FeliCa（ソニー）
  - ISO 14443 Type A/Bカード

- **包括的なタグサポート**: すべてのタグタイプの[サポートされている操作](docs/supported_operations.md)を表示

- **NDEF操作**:
  - NDEFレコードの読み書き
  - 複数のNDEFレコードの作成と管理
  - 様々なNDEFレコードタイプのサポート（テキスト、URI、スマートポスターなど）
  - 生データ検査のための16進数ビュー

- **タグ管理**:
  - タグ情報の読み取り（UID、メモリレイアウト、機能）
  - 検証付きでのタグへのデータ書き込み
  - 不正な書き込みを防ぐためのタグのロック
  - NDEF使用のためのタグのフォーマット

- **ユーザーインターフェース**:
  - sphinx_rtd_themeを使用したモダンでレスポンシブなデザイン
  - ライト/ダーク/システムテーマサポート
  - リアルタイムのタグ検出とステータス更新
  - 詳細なタグ情報パネル
  - フィルタリングオプション付きログビューア
  - 英語とイタリア語の包括的なドキュメント

- **セキュリティ機能**:
  - 🔒 機密操作のためのパスワード保護
  - 🔑 PBKDF2を使用した安全なパスワードハッシュ化
  - 🔄 パスワード変更機能
  - ⚙️ パスワード保護の有効/無効切り替え
  - 🔐 タグツール、データベース、クローナーなどの保護された操作

- **高度な機能**:
  - タグエミュレーションモード（実験的）
  - 複数タグを処理するバッチ操作
  - カスタムコマンド実行
  - 複数の詳細レベルを持つロギングシステム
  - 開発者向けAPIドキュメント
  - 一般的な問題のトラブルシューティングガイド
  - オープンソースコラボレーションのための貢献ガイドライン

## 🚀 要件

- Python 3.8以上
- サポートされているNFCリーダー/ライターハードウェア:
  - ACR122U
  - PN532（USB/UART経由）
  - PC/SC互換リーダー
- PC/SCをサポートするWindows 10/11またはLinux
- 必要なPythonパッケージ（`requirements.txt`を参照）

## 📖 ドキュメント

英語とイタリア語で包括的なドキュメントが利用可能です：

- ユーザーガイド
- APIリファレンス
- トラブルシューティングガイド
- よくある質問
- 貢献ガイドライン

ドキュメントをローカルでビルドするには：

```bash
# ドキュメントの要件をインストール
pip install -r requirements-docs.txt

# 英語のドキュメントをビルド
cd docs/ENG
make html

# イタリア語のドキュメントをビルド
cd ../ITA
make html
```

ドキュメントは各言語フォルダの`_build/html`ディレクトリで利用可能です。

## 📦 インストール

1. リポジトリをクローン:

   ```bash
   git clone https://github.com/Nsfr750/NFC.git
   cd NFC
   ```

2. 仮想環境を作成して有効化（推奨）:

   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate

   # Linux/macOS
   python3 -m venv venv
   source venv/bin/activate
   ```

3. 必要なパッケージをインストール:

   ```bash
   pip install -r requirements.txt
   ```

4. （オプション）PC/SCドライバーがインストールされていない場合はインストール:
   - Windows: [CCIDドライバー](https://ccid.apdu.fr/)をインストール
   - Linux: `pcscd`と`libpcsclite-dev`パッケージをインストール

5. アプリケーションを実行:

   ```bash
   python main.py
   ```

## 🚀 使い方

### 基本操作

1. **NFCリーダーを接続**
   - アプリケーションがサポートされているデバイスを自動検出します
   - 接続状態はステータスバーに表示されます

2. **タグを読み取る**
   - NFCタグをリーダーに近づけます
   - タグ情報がメインウィンドウに表示されます
   - 16進エディタで詳細なメモリレイアウトを表示します

3. **タグに書き込む**
   - 「書き込み」タブに移動します
   - レコードタイプ（テキスト、URIなど）を選択します
   - コンテンツを入力して「タグに書き込み」をクリックします

4. **タグをロックする**
   - 「ロック」ボタンを使用してそれ以上の書き込みを防ぎます
   - 一部のタグは永続的なロックをサポートしています（注意して使用してください）

### 🛠️ 高度な機能

- **タグエミュレーション**: NFCタグをエミュレートします（実験的）
- **バッチ処理**: 複数のタグを連続して処理します
- **カスタムコマンド**: タグに直接コマンドを送信します
- **ログビューア**: 操作ログを表示およびフィルタリングします

## 🤝 貢献

貢献は大歓迎です！バグレポート、機能リクエスト、プルリクエストは歓迎します。

1. リポジトリをフォークします
2. 機能ブランチを作成します（`git checkout -b feature/AmazingFeature`）
3. 変更をコミットします（`git commit -m 'Add some AmazingFeature'`）
4. ブランチにプッシュします（`git push origin feature/AmazingFeature`）
5. プルリクエストを開きます

## 📄 ライセンス

このプロジェクトはGNU General Public License v3.0でライセンスされています。詳細は`LICENSE`ファイルを参照してください。

## 🙏 謝辞

- すべての貢献者の方々
- 素晴らしいオープンソースプロジェクトコミュニティ
- テストとフィードバックを提供してくれたユーザーの皆様
