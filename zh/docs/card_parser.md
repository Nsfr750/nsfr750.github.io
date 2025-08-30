---
lang: zh
lang-niv: fonto
lang-ref: 011-jbk
layout: doc
order: 2
title: 'Credit Card Stripe Parser'
---

# 信用卡磁条解析器

**信用卡磁条解析器** 是一个 Python 库和命令行工具，用于解析和分析信用卡的磁条数据。它支持 ISO/IEC 7811-2 和 ISO/IEC 7813 标准中规定的 1 轨和 2 轨格式。

> **注意**
> 此工具仅用于教学和测试目的。请始终按照 PCI DSS 要求以及适用法律法规处理支付卡数据。

## 使用指南

本指南提供了如何使用信用卡磁条解析器库的示例。

### 基本用法

#### 解析完整轨迹数据

```python
from credit_card_stripe_parser import FullTrackParser

# 创建解析器实例
parser = FullTrackParser()

# 轨迹数据示例
t​​rack_data = "%B5168755544412233^PKMMV/UNEMBOXXXX ^1807111100000000000000111000000?;5168755544412233=18071111000011100000?

# 解析轨迹数据
result = parser.parse(track_data)

# 访问已解析数据
if result.is_track_one_valid and result.track_one:
print(f"持卡人: {result.track_one.card_holder_name.strip()}")
print(f"PAN: {result.track_one.pan}")
print(f"有效期: {result.track_one.expiration_date[:2]}/{result.track_one.expiration_date[2:]}")

if result.is_track_two_valid and result.track_two:
print(f"服务码: {result.track_two.service_code}")
```

### 解析单个轨迹

#### 轨迹 1 解析

```python
from credit_card_stripe_parser import FullTrackParser

parser = FullTrackParser()
track1_data = "%B5168755544412233^PKMMV/UNEMBOXXXX ^1807111100000000000000111000000？"

尝试：
track1 = parser.parse_track_one(track1_data)
print(f"轨道 1 数据：{track1}")
except Exception as e:
print(f"解析轨道 1 时出错：{e}")
```

#### 轨道 2 解析

```python
from credit_card_stripe_parser import FullTrackParser

parser = FullTrackParser()
track2_data = ";5168755544412233=18071111000011100000？"

尝试：
track2 = parser.parse_track_two(track2_data)
print(f"轨道 2 数据：{track2}")
except Exception as e:
print(f"解析轨道 2 时出错：{e}")
```

### 错误处理

该库针对不同的错误场景提供了特定的异常：

```python
from credit_card_stripe_parser import (
FullTrackParser,
InvalidTrackOneException,
InvalidTrackTwoException,
InvalidTrackDataException
)

parser = FullTrackParser()

尝试：
result = parser.parse(invalid_track_data)
except InvalidTrackOneException as e:
print(f"轨道 1 数据无效：{e}")
except InvalidTrackTwoException as e:
print(f"轨道 2 数据无效：{e}")
except InvalidTrackDataException as e:
print(f"轨道数据无效： {e}")
except Exception as e:
print(f"意外错误：{e}")
```

### 使用数据模型

该库提供了用于处理已解析跟踪数据的数据模型：

```python
from credit_card_stripe_parser.models import TrackOneModel, TrackTwoModel

# 创建 TrackOneModel 实例
track1 = TrackOneModel(
format_code='B',
pan='5168755544412233',
card_holder_name='JOHN DOE',
expiration_date='2512',
service_code='123',
discretionary_data='123456789012345678901',
source_string='%B5168755544412233^JOHN DOE^251212312345678901234567890?'
)

# 创建 TrackTwoModel 实例
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

## 高级用法

### 自定义验证

您可以实现自定义通过子类化解析器进行验证：

```python
from credit_card_stripe_parser import FullTrackParser

class CustomTrackParser(FullTrackParser):
def validate_track_one(self, track_data: str) -> bool:
# 针对 Track 1 的自定义验证逻辑
if not super().validate_track_one(track_data):
return False
# 在此处添加自定义验证
return True

def validate_track_two(self, track_data: str) -> bool:
# 针对 Track 2 的自定义验证逻辑
if not super().validate_track_two(track_data):
return False
# 在此处添加自定义验证
return True
```

### LRC 验证

启用 LRC（纵向冗余校验）验证：

```python
parser = FullTrackParser(validate_lrc=True)

# 如果 LRC 验证失败，将抛出异常
try:
result = parser.parse(track_data_with_lrc)
except Exception as e:
print(f"LRC 验证失败：{e}")
```
> **注意**
> LRC 验证要求轨道数据末尾包含 LRC 字符。

## 常见问题 (FAQ)

### 一般问题

#### 此库的用途是什么？
此库旨在解析和分析信用卡磁条数据，用于教育和测试目的。

#### 在生产环境中使用是否安全？
此工具的使用应符合 PCI DSS 要求和适用法律。始终确保适当的安全

