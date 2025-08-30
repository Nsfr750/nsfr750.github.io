---
lang: ja
lang-niv: font
lang-ref: 012-jbk
layout: page
title: 'CDE550シミュレーター'
---

# ナイデック コマンダー CDE 550 シミュレーター

[![Python バージョン](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![ライセンス: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![バージョン](https://img.shields.io/badge/version-0.0.2-green.svg)](CHANGELOG.md)

PyQt6を使用してPythonで開発された、グラフィカルインターフェースを備えたNidec Commander CDE 550インバーターのソフトウェアシミュレーターです。

## バージョン0.0.2の新機能

- ユーザーインターフェースの完全な**日本語ローカライズ**
- 誤検出を減らした**改善されたアラーム処理**
- 起動時と負荷変動時の**パフォーマンス最適化**
- 詳細なCHANGELOGを含む**更新されたドキュメント**

## 特徴

- Nidec Commander CDE 550インバーターのリアルな動作シミュレーション
- 完全に日本語化されたPyQt6による直感的なグラフィカルインターフェース
- pyserialを使用したシリアル通信
- 主要な制御コマンドのサポート
- 高度な管理を備えた障害・アラームシミュレーション
- パラメータのリアルタイム監視
- イベントとエラーのログ記録

## 前提条件

- Python 3.8以上
- Pip（Pythonパッケージマネージャー）
- Python仮想環境（推奨）

## インストール

1. リポジトリをクローン:
   ```bash
   git clone https://github.com/Nsfr750/CDE550-sim.git
   cd CDE550-sim
   ```

2. 仮想環境を作成して有効化（任意ですが推奨）:
   ```bash
   # Windowsの場合
   python -m venv venv
   .\venv\Scripts\activate
   
   # macOS/Linuxの場合
   python3 -m venv venv
   source venv/bin/activate
   ```

3. 依存関係をインストール:
   ```bash
   pip install -r requirements.txt
   ```

## 使い方

1. シミュレーターを起動:
   ```bash
   python main.py
   ```

2. グラフィカルインターフェースに以下が表示されます:
   - インバーターの状態
   - 動作パラメータ
   - イベントログ
   - シミュレーションコントロール

3. シリアル接続の場合:
   - 接続 -> 接続 に移動
   - 使用するCOMポートを選択
   - 通信速度（ボーレート）を設定
   - 「接続」をクリック

## サポートされているシリアルコマンド

| コマンド | 説明 | 例 |
|---------|-------------|---------|
| `RUN` | インバーターを起動 | `RUN` |
| `STOP` | インバーターを停止 | `STOP` |
| `RST` | アラームをリセット | `RST` |
| `FREQ <値>` | 周波数を設定（Hz） | `FREQ 50.0` |
| `DIR <1\|-1>` | 回転方向を設定 | `DIR 1`（正転）|
| `STATUS` | 完全な状態を表示 | `STATUS` |
| `HELP` | コマンドリストを表示 | `HELP` |

## プロジェクト構造

```
CDE550-sim/
├── main.py              # アプリケーションのエントリーポイント
├── inverter_sim.py      # インバーターシミュレーションロジック
├── serial_handler.py    # シリアル通信処理
├── script/              # ユーザーインターフェースとヘルプファイル
│   ├── help.py          # ヘルプウィンドウ
│   ├── serial_dialog.py # シリアル接続ウィンドウ
│   └── version.py       # バージョン管理
├── requirements.txt     # プロジェクトの依存関係
├── README.md            # メインのドキュメント
└── CHANGELOG.md         # 変更履歴
```

## 貢献について

改善案を歓迎します！提案手順は以下の通りです：

1. プロジェクトをフォーク
2. 機能ブランチを作成（`git checkout -b feature/素晴らしい機能`）
3. 変更をコミット（`git commit -m '素晴らしい機能を追加'`）
4. ブランチにプッシュ（`git push origin feature/素晴らしい機能`）
5. プルリクエストを開く

## ライセンス

GPL-3.0ライセンスの下で配布されています。詳細は`LICENSE`ファイルをご覧ください。

## 連絡先

- 作者: Nsfr750
- メール: [nsfr750@yandex.com]
- リポジトリ: https://github.com/Nsfr750/CDE550-sim

---

<div align="center">
  <sub>❤️ によって開発されました Nsfr750</sub>
</div>
