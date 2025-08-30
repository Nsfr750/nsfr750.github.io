---
lang: ja
lang-niv: fonto
lang-ref: 011-jbk
layout: page
title: 'クレジットカードストライプパーサー'
---

# クレジットカードストライプパーサー

**クレジットカードストライプパーサー**は、クレジットカードの磁気ストライプデータを解析・分析するためのPythonライブラリ兼コマンドラインツールです。ISO/IEC 7811-2およびISO/IEC 7813規格で規定されているトラック1とトラック2の両方のフォーマットをサポートしています。

> **注**
> このツールは教育およびテスト目的でのみ使用することを意図しています。支払いカードデータを扱う際は、常にPCI DSS要件および適用される法令を遵守してください。

## 使用ガイド

このガイドでは、クレジットカードストライプパーサーライブラリの使用方法について説明します。

### 基本的な使い方

#### フルトラックデータの解析

```python
from credit_card_stripe_parser import FullTrackParser

# パーサーインスタンスを作成
parser = FullTrackParser()

# トラックデータの例
track_data = "%B5168755544412233^PKMMV/UNEMBOXXXX          ^1807111100000000000000111000000?;5168755544412233=18071111000011100000?"

# トラックデータを解析
result = parser.parse(track_data)

# 解析データにアクセス
if result.is_track_one_valid and result.track_one:
    print(f"カード名義人: {result.track_one.card_holder_name.strip()}")
    print(f"PAN: {result.track_one.pan}")
    print(f"有効期限: {result.track_one.expiration_date[:2]}/{result.track_one.expiration_date[2:]}")

if result.is_track_two_valid and result.track_two:
    print(f"サービスコード: {result.track_two.service_code}")
```

### 個別トラックの解析

#### トラック1の解析

```python
from credit_card_stripe_parser import FullTrackParser

parser = FullTrackParser()
track1_data = "%B5168755544412233^PKMMV/UNEMBOXXXX          ^1807111100000000000000111000000?"

try:
    track1 = parser.parse_track_one(track1_data)
    print(f"トラック1データ: {track1}")
except Exception as e:
    print(f"トラック1の解析エラー: {e}")
```

#### トラック2の解析

```python
from credit_card_stripe_parser import FullTrackParser

parser = FullTrackParser()
track2_data = ";5168755544412233=18071111000011100000?"

try:
    track2 = parser.parse_track_two(track2_data)
    print(f"トラック2データ: {track2}")
except Exception as e:
    print(f"トラック2の解析エラー: {e}")
```

### エラーハンドリング

ライブラリは、さまざまなエラーシナリオに対応するための特定の例外を提供します：

```python
from credit_card_stripe_parser import (
    FullTrackParser,
    InvalidTrackOneException,
    InvalidTrackTwoException,
    InvalidTrackDataException
)

parser = FullTrackParser()

try:
    result = parser.parse(invalid_track_data)
except InvalidTrackOneException as e:
    print(f"無効なトラック1データ: {e}")
except InvalidTrackTwoException as e:
    print(f"無効なトラック2データ: {e}")
except InvalidTrackDataException as e:
    print(f"無効なトラックデータ: {e}")
except Exception as e:
    print(f"予期しないエラー: {e}")
```

### データモデルの使用

ライブラリは、解析されたトラックデータを操作するためのデータモデルを提供します：

```python
from credit_card_stripe_parser.models import TrackOneModel, TrackTwoModel

# TrackOneModelインスタンスを作成
track1 = TrackOneModel(
    format_code='B',
    pan='5168755544412233',
    card_holder_name='TANAKA TARO',
    expiration_date='2512',
    service_code='123',
    discretionary_data='123456789012345678901',
    source_string='%B5168755544412233^TANAKA TARO^251212312345678901234567890?'
)

# TrackTwoModelインスタンスを作成
track2 = TrackTwoModel(
    pan='5168755544412233',
    expiration_date='2512',
    service_code='123',
    pvki=None,
    pvv_or_cvv='1234',
    discretionary_data='123456789012345678901234567890',
    source_string=';5168755544412233=2512123123412345678901234567890?'
)
```

## 高度な使い方

### カスタムバリデーション

パーサーをサブクラス化してカスタムバリデーションを実装できます：

```python
from credit_card_stripe_parser import FullTrackParser

class CustomTrackParser(FullTrackParser):
    def validate_track_one(self, track_data: str) -> bool:
        # トラック1のカスタムバリデーションロジック
        if not super().validate_track_one(track_data):
            return False
        # カスタムバリデーションをここに追加
        return True

    def validate_track_two(self, track_data: str) -> bool:
        # トラック2のカスタムバリデーションロジック
        if not super().validate_track_two(track_data):
            return False
        # カスタムバリデーションをここに追加
        return True
```

### LRC検証

LRC（縦方向冗長検査）検証を有効にするには：

```python
parser = FullTrackParser(validate_lrc=True)

# LRC検証に失敗した場合は例外が発生します
try:
    result = parser.parse(track_data_with_lrc)
except Exception as e:
    print(f"LRC検証エラー: {e}")
```
> **注**
> LRC検証では、トラックデータの最後にLRC文字が含まれている必要があります。

## よくある質問（FAQ）

### 一般的な質問

#### このライブラリの目的は何ですか？
このライブラリは、教育およびテスト目的でクレジットカードの磁気ストライプデータを解析・分析するために設計されています。

#### 本番環境での使用は安全ですか？
このツールは、PCI DSS要件および適用される法令を遵守して使用する必要があります。支払いカードデータを扱う際は、適切なセキュリティ対策を講じてください。

### 技術的な質問

#### どのようなトラックフォーマットがサポートされていますか？
このライブラリは、ISO/IEC 7811-2およびISO/IEC 7813規格で規定されているトラック1とトラック2のフォーマットをサポートしています。

#### 解析中のエラーはどのように処理すればよいですか？
ライブラリは、さまざまなエラーシナリオに対応するための特定の例外を提供します。例については、エラーハンドリングのセクションを参照してください。

### セキュリティに関する考慮事項

#### 機密性の高いカードデータはどのように扱うべきですか？
支払いカードデータを扱う際は、常にPCI DSS要件に従ってください。このライブラリには、機密情報をマスキングするためのヘルパー関数が含まれています。

#### PANマスキングの例：

```python
from credit_card_stripe_parser.utils import mask_pan

pan = "5168755544412233"
masked_pan = mask_pan(pan)  # 例: "516875******2233"
print(f"マスクされたPAN: {masked_pan}")
```

#### セキュアなデータ処理のための推奨事項
- カードデータをログに記録しないでください
- メモリ上に保存する必要のないデータは、使用後すぐに消去してください
- 可能な限り、PANなどの機密データはマスキングまたはトークン化してください
- セキュアな通信チャネル（TLS/SSL）を使用してデータを転送してください

### トラブルシューティング

#### 無効なトラックデータエラーが発生します
- トラックデータのフォーマットが正しいことを確認してください
- 開始/終了センチネル文字（%、?、; など）が正しく設定されていることを確認してください
- トラックデータに不正な文字が含まれていないことを確認してください

#### 特定のカードが認識されません
- カードの磁気ストライプが損傷していないか確認してください
- カードリーダーが適切に動作していることを確認してください
- カードの規格がサポートされていることを確認してください（ISO/IEC 7811-2、ISO/IEC 7813）
