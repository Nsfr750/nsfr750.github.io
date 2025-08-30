---
lang: ja
lang-niv: fonto
lang-ref: 010-jbk
layout: page
title: '3Dフィラメントマネージャー'
---

# 3Dフィラメントマネージャー

![3Dフィラメントマネージャー](assets/logo.png)

3Dプリント用フィラメントの在庫管理を行うデスクトップアプリケーションです。材料、色、使用量、コスト、スライサー設定を一箇所で管理できます。

## ✨ 特徴

* **🌐 多言語サポート**: 英語とイタリア語に対応
* **🎨 モダンなUI**: 絵文字アイコンとテーマサポート（ライト/ダークモード）を備えたクリーンなインターフェース
* **📊 包括的なフィラメント管理**:
  * 詳細なフィラメント情報の保存（ブランド、素材、色、直径など）
  * フィラメントの使用量と残量の追跡
  * 材料コストの計算
  * 価格の追跡と履歴
  * 視覚化による価格分析
  * ベンダーごとの価格比較
* **⚙️ スライサー連携**:
  * スライサープロファイルの保存と管理（Cura、PrusaSlicer、eQuidiSlicer）
  * プリンターごとのカスタムプリントプロファイル
* **🔍 高度な検索とフィルタリング**:
  * 任意のフィラメントプロパティで検索
  * 任意の列でソート
  * 素材タイプ、色、またはカスタムタグでフィルタリング
* **📂 インポート/エクスポート**:
  * フィラメントライブラリのバックアップと復元
  * プロファイルの共有
  * 一括インポート/エクスポートのサポート
* **🔒 データセキュリティ**:
  * 設定は`config/`ディレクトリに保存
  * インターネット接続不要
  * ローカルデータストレージ

## 🚀 システム要件

* Python 3.8以上
* 必要なパッケージ（自動的にインストールされます）:
  * `lxml` - 高速なXML処理
  * `pillow` - アイコンの画像処理
  * `matplotlib` - 価格分析のためのデータ可視化

## 🛠️ インストール

### 前提条件

* Python 3.8以上
* Git（開発用、オプション）

### インストール手順

1. **リポジトリをクローン**（またはZIPでダウンロード）:

   ```bash
   git clone https://github.com/Nsfr750/3D_Filament_Manager.git
   cd 3D_Filament_Manager
   ```

2. **仮想環境を作成して有効化**（推奨）:

   ```bash
   # Windowsの場合
   python -m venv venv
   .\venv\Scripts\activate
   
   # macOS/Linuxの場合
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **依存関係をインストール**:

   ```bash
   pip install -r requirements.txt
   ```

4. **アプリケーションを実行**:

   ```bash
   python main.py
   ```

### データストレージ

* フィラメントプロファイルは`fdm/`ディレクトリに保存されます
* アプリケーション設定は`config/`ディレクトリに保存されます
* ログは`logs/`ディレクトリに書き込まれます

## 🤝 貢献について

皆様の貢献をお待ちしています！以下の方法で協力いただけます：

* [issue](https://github.com/Nsfr750/3D_Filament_Manager/issues)を開いてバグを報告
* 新機能や改善点の提案
* コード変更のプルリクエストの提出
* ドキュメントの改善
* 新しい言語への翻訳

### 開発環境のセットアップ

1. リポジトリをフォーク
2. 機能ブランチを作成（`git checkout -b feature/amazing-feature`）
3. 変更をコミット（`git commit -m '素晴らしい機能を追加'`）
4. ブランチにプッシュ（`git push origin feature/amazing-feature`）
5. プルリクエストを開く

### コーディングスタイル

* [PEP 8](https://www.python.org/dev/peps/pep-0008/)ガイドラインに従ってください
* コードの明確さのために型ヒントを使用してください
* すべてのパブリック関数とクラスにドキュストリングを記述してください

## 📜 ライセンス

このプロジェクトは**GNU General Public License v3.0**の下でライセンスされています。詳細は[LICENSE](LICENSE)ファイルをご覧ください。

## 🙏 サポート

このプロジェクトが役に立った場合は、開発をサポートしていただけると幸いです：

* ⭐ リポジトリをスターする
* 🐛 問題を報告する
* 💡 新機能を提案する
* 💰 [GitHubでプロジェクトをスポンサーする](https://github.com/sponsors/Nsfr750)

## 📞 連絡先

* GitHub: [@Nsfr750](https://github.com/Nsfr750)
* メール: nsfr750@yandex.com

---

### 開発者をサポートする

このアプリケーションが役に立った場合は、開発者をサポートしてください：

* **PayPal**: [https://paypal.me/3dmega](https://paypal.me/3dmega)
* **GitHub**: [https://github.com/Nsfr750](https://github.com/Nsfr750)
