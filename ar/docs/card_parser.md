---
lang: ar
lang-niv: fonto
lang-ref: 011-jbk
layout: doc
order: 2
title: 'أداة تحليل الشرائط الممغنطة للبطاقات الائتمانية'
---

# أداة تحليل الشرائط الممغنطة للبطاقات الائتمانية

**Credit Card Stripe Parser** هي مكتبة بايثون وأداة سطر أوامر لتحليل بيانات الشرائط الممغنطة للبطاقات الائتمانية. تدعم تنسيقات المسار الأول والثاني كما هو محدد في معايير ISO/IEC 7811-2 و ISO/IEC 7813.

> **ملاحظة**
> هذه الأداة مخصصة للأغراض التعليمية والاختبارية فقط. يرجى التعامل مع بيانات البطاقات الائتمانية دائمًا وفقًا لمتطلبات معايير أمان صناعة بطاقات الدفع (PCI DSS) والقوانين واللوائح المعمول بها.

## دليل الاستخدام

يقدم هذا الدليل أمثلة حول كيفية استخدام مكتبة Credit Card Stripe Parser.

### الاستخدام الأساسي

#### تحليل بيانات المسار الكامل

```python
from credit_card_stripe_parser import FullTrackParser

# إنشاء كائن المحلل اللغوي
parser = FullTrackParser()

# مثال على بيانات المسار
track_data = "%B5168755544412233^PKMMV/UNEMBOXXXX          ^1807111100000000000000111000000?;5168755544412233=18071111000011100000?"

# تحليل بيانات المسار
result = parser.parse(track_data)

# الوصول إلى البيانات المحللة
if result.is_track_one_valid and result.track_one:
    print(f"حامل البطاقة: {result.track_one.card_holder_name.strip()}")
    print(f"الرقم الأساسي للبطاقة (PAN): {result.track_one.pan}")
    print(f"تاريخ الانتهاء: {result.track_one.expiration_date[:2]}/{result.track_one.expiration_date[2:]}")

if result.is_track_two_valid and result.track_two:
    print(f"رمز الخدمة: {result.track_two.service_code}")
```

### تحليل المسارات الفردية

#### تحليل المسار الأول

```python
from credit_card_stripe_parser import FullTrackParser

parser = FullTrackParser()
track1_data = "%B5168755544412233^PKMMV/UNEMBOXXXX          ^1807111100000000000000111000000?"

try:
    track1 = parser.parse_track_one(track1_data)
    print(f"بيانات المسار الأول: {track1}")
except Exception as e:
    print(f"خطأ في تحليل المسار الأول: {e}")
```

#### تحليل المسار الثاني

```python
from credit_card_stripe_parser import FullTrackParser

parser = FullTrackParser()
track2_data = ";5168755544412233=18071111000011100000?"

try:
    track2 = parser.parse_track_two(track2_data)
    print(f"بيانات المسار الثاني: {track2}")
except Exception as e:
    print(f"خطأ في تحليل المسار الثاني: {e}")
```

### معالجة الأخطاء

توفر المكتبة استثناءات محددة لسيناريوهات الأخطاء المختلفة:

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
    print(f"بيانات المسار الأول غير صالحة: {e}")
except InvalidTrackTwoException as e:
    print(f"بيانات المسار الثاني غير صالحة: {e}")
except InvalidTrackDataException as e:
    print(f"بيانات المسار غير صالحة: {e}")
except Exception as e:
    print(f"خطأ غير متوقع: {e}")
```

### استخدام نماذج البيانات

توفر المكتبة نماذج بيانات للعمل مع بيانات المسار المحللة:

```python
from credit_card_stripe_parser.models import TrackOneModel, TrackTwoModel

# إنشاء كائن TrackOneModel
track1 = TrackOneModel(
    format_code='B',
    pan='5168755544412233',
    card_holder_name='أحمد محمد',
    expiration_date='2512',
    service_code='123',
    discretionary_data='123456789012345678901',
    source_string='%B5168755544412233^أحمد محمد^251212312345678901234567890?'
)

# إنشاء كائن TrackTwoModel
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

## استخدام متقدم

### التحقق المخصص

يمكنك تنفيذ التحقق المخصص من خلال إنشاء فئة فرعية من المحلل:

```python
from credit_card_stripe_parser import FullTrackParser

class CustomTrackParser(FullTrackParser):
    def validate_track_one(self, track_data: str) -> bool:
        # منطق التحقق المخصص للمسار الأول
        if not super().validate_track_one(track_data):
            return False
        # أضف منطق التحقق المخصص هنا
        return True

    def validate_track_two(self, track_data: str) -> bool:
        # منطق التحقق المخصص للمسار الثاني
        if not super().validate_track_two(track_data):
            return False
        # أضف منطق التحقق المخصص هنا
        return True
```

### التحقق من LRC

لتفعيل التحقق من المجموع الاختباري الطولي (Longitudinal Redundancy Check):

```python
parser = FullTrackParser(validate_lrc=True)

# سيثير استثناءً في حالة فشل التحقق من LRC
try:
    result = parser.parse(track_data_with_lrc)
except Exception as e:
    print(f"فشل التحقق من LRC: {e}")
```
> **ملاحظة**
> يتطلب التحقق من LRC تضمين حرف LRC في نهاية بيانات المسار.

## الأسئلة الشائعة (FAQ)

### أسئلة عامة

#### ما هو الغرض من هذه المكتبة؟
تم تصميم هذه المكتبة لتحليل بيانات الشرائط الممغنطة للبطاقات الائتمانية للأغراض التعليمية والاختبارية.

#### هل هي آمنة للاستخدام في بيئة الإنتاج؟
يجب استخدام هذه الأداة وفقًا لمتطلبات معايير أمان صناعة بطاقات الدفع (PCI DSS) والقوانين المعمول بها. تأكد دائمًا من وجود إجراءات أمان مناسبة عند التعامل مع بيانات البطاقات الائتمانية.

### أسئلة تقنية

#### ما هي تنسيقات المسارات المدعومة؟
تدعم المكتبة تنسيقي المسار الأول والثاني كما هو محدد في معايير ISO/IEC 7811-2 و ISO/IEC 7813.

#### كيف يمكنني التعامل مع الأخطاء أثناء التحليل؟
توفر المكتبة استثناءات محددة لسيناريوهات الأخطاء المختلفة. انظر قسم "معالجة الأخطاء" للأمثلة.

### اعتبارات الأمان

#### كيف يجب التعامل مع بيانات البطاقات الحساسة؟
اتبع دائمًا متطلبات معايير أمان صناعة بطاقات الدفع (PCI DSS) عند التعامل مع بيانات البطاقات الائتمانية. تتضمن المكتبة وظائف مساعدة لإخفاء المعلومات الحساسة.

#### مثال على إخفاء رقم البطاقة:

```python
def mask_pan(pan: str) -> str:
    if len(pan) < 10:
        return pan
    return pan[:6] + '*' * (len(pan) - 10) + pan[-4:]

print(mask_pan("5168755544412233"))  # الناتج: 516875******2233
```
