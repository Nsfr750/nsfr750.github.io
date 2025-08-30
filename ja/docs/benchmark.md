---
lang: ja
lang-niv: fonto
lang-ref: 023-jbk
layout: doc
order: 14 # オプション: メニュー内の順序
title: 'ベンチマーク'
---

[![ライセンス: GPL v3](https://img.shields.io/badge/ライセンス-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![コードスタイル: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

PySide6で構築されたモダンなPythonベンチマークツールで、Pystoneやその他のベンチマークテストを実行・分析するための使いやすいインターフェースを提供します。

## 📥 インストール

### 前提条件

- Python 3.9 以降
- Windows または Linux

### クイックスタート

1. リポジトリをクローン:

   ```bash
   git clone https://github.com/Nsfr750/benchmark.git
   cd benchmark
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

## ✨ 特徴

- **モダンなUI**: PySide6で構築されたクリーンで応答性の高いインターフェース
- **包括的なベンチマーク**:
  - カスタマイズ可能なテスト時間
  - リアルタイム進捗追跡
  - 統計付き詳細な結果
  - 過去データとの比較
- **ロギング**:
  - 詳細な操作ログ
  - レベル別ログフィルタリング
  - ログファイルのローテーション
- **多言語サポート**:
  - 英語 (en)
  - イタリア語 (it)
- **アクセシビリティ**:
  - キーボードショートカット
  - ハイコントラストモード
  - 調整可能なテキストサイズ

## ⌨️ キーボードショートカット

- `Ctrl+L`: アプリケーションログを表示
- `F1`: ヘルプを表示
- `Esc`: ダイアログを閉じる
- `Ctrl+Q`: アプリケーションを終了

## 📊 使い方

1. ベンチマークの反復回数を設定
2. 「ベンチマーク開始」をクリック
3. リアルタイムで進捗を確認
4. 詳細な結果と統計を表示
5. トラブルシューティングのためにログを確認

## 📂 プロジェクト構造

```
benchmark/
├── .github/                            # GitHub Actions
│   ├── workflows/                      # GitHub Actionsワークフロー
│   │   └── ci-cd.yml                   # CI/CDパイプライン
│   ├── issues/                         # GitHubイシュー
│   |   └── templates/                  # GitHubイシューテンプレート
│   └── FUNDING.yml                     # 資金調達ファイル
├── assets/                             # アセットファイル
├── config/                             # 設定ファイル
│   ├── config.json                     # 設定ファイル
│   └── updates.json                    # アップデートキャッシュ
├── docs/                               # ドキュメント
│   ├── images/                         # ドキュメント画像
│   ├── pdf/                            # PDFドキュメント
│   └── USER_GUIDE.md                   # ユーザーガイド
├── lang/                               # 言語ファイル
│   ├── en.json                         # 英語ファイル
│   └── it.json                         # イタリア語ファイル
├── logs/                               # ログファイル
├── script/                             # ソースコード
│   ├── __init__.py                     # パッケージ初期化
│   ├── about.py                        # バージョン情報ダイアログ
│   ├── benchmark_history.py            # ベンチマーク履歴
│   ├── benchmark_tests.py              # ベンチマークテスト
│   ├── CLI_pystone.py                  # コマンドラインPystoneベンチマーク
│   ├── config_manager.py               # 設定マネージャー
│   ├── export_results.py               # 結果のエクスポート
│   ├── hardware_monitor.py             # ハードウェアモニター
│   ├── help.py                         # ヘルプダイアログ
│   ├── history_dialog.py               # 履歴ダイアログ
│   ├── lang_mgr.py                     # 言語マネージャー
│   ├── logger.py                       # ロギング設定
│   ├── menu.py                         # メニューバー機能
│   ├── settings.py                     # 設定ダイアログ
│   ├── sponsor.py                      # スポンサーダイアログ
│   ├── system_info.py                  # システム情報
│   ├── test_menu.py                    # テストメニュー
│   ├── theme_manager.py                # テーママネージャー
│   ├── updates.py                      # アップデートシステム
│   ├── version.py                      # バージョンシステム
│   ├── view_log.py                     # ログビューアー
│   └── visualization.py                # ベンチマーク可視化
├── tests/                              # テストファイル
│   ├── test_benchmark.py               # ベンチマークテスト
│   ├── test_hardware_monitor.py        # ハードウェアモニターテスト
│   ├── test_monitor_manual.py          # マニュアルモニターテスト
│   ├── test_monitor.py                 # モニターテスト
│   └── TEST_README.md                  # テストのREADME
├── .gitignore                          # .gitignoreファイル
├── CHANGELOG.md                        # 変更履歴
├── CONTRIBUTING.md                     # コントリビューションガイドライン
├── LICENSE                             # GPLv3ライセンスファイル
├── main.py                             # メインアプリケーション
├── README.md                           # このファイル
├── requirements.txt                    # 依存関係ファイル
└── TO_DO.md                            # タスクリスト
```
