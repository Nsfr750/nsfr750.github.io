---
lang: ar
lang-niv: font
lang-ref: 012-jbk
layout: doc
order: 3
title: 'CDE550-Sim'
---

# محاكي Nidec Commander CDE 550

[![إصدار بايثون](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![الترخيص: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![الإصدار](https://img.shields.io/badge/version-0.0.2-green.svg)](CHANGELOG.md)

محاكي برمجي لعاكس Nidec Commander CDE 550 مع واجهة رسومية، مطور بلغة Python باستخدام PyQt6.

## ما الجديد في الإصدار 0.0.2

- **توطين كامل** لواجهة المستخدم إلى اللغة الإيطالية
- **تحسين معالجة التنبيهات** مع تقليل الإنذارات الكاذبة
- **تحسينات في الأداء** أثناء بدء التشغيل وتغيرات الحمل
- **تحديث الوثائق** مع سجل تغييرات مفصل

## الميزات

- محاكاة واقعية لسلوك عاكس Nidec Commander CDE 550
- واجهة رسومية بديهية مع PyQt6 مع توطين كامل للغة الإيطالية
- اتصال تسلسلي عبر pyserial
- دعم أوامر التحكم الرئيسية
- محاكاة الأعطال والتنبيهات مع إدارة متقدمة
- مراقبة المعلمات في الوقت الفعلي
- تسجيل الأحداث والأخطاء

## المتطلبات الأساسية

- بايثون 3.8 أو أحدث
- مدير حزم بايثون (Pip)
- بيئة افتراضية لبايثون (موصى بها)

## التثبيت

1. استنسخ المستودع:
   ```bash
   git clone https://github.com/Nsfr750/CDE550-sim.git
   cd CDE550-sim
   ```

2. أنشئ وقم بتفعيل بيئة افتراضية (موصى به):
   ```bash
   # في ويندوز
   python -m venv venv
   .\venv\Scripts\activate
   
   # في ماك/لينكس
   python3 -m venv venv
   source venv/bin/activate
   ```

3. قم بتثبيت التبعيات:
   ```bash
   pip install -r requirements.txt
   ```

## طريقة الاستخدام

1. ابدأ المحاكي:
   ```bash
   python main.py
   ```

2. ستظهر في الواجهة الرسومية:
   - حالة العاكس
   - معلمات التشغيل
   - سجل الأحداث
   - عناصر تحكم المحاكاة

3. للاتصال التسلسلي:
   - اذهب إلى اتصال -> اتصل
   - حدد منفذ COM المطلوب
   - عيّن سرعة الاتصال (باود)
   - انقر على "اتصال"

## أوامر الاتصال التسلسلي المدعومة

| الأمر | الوصف | مثال |
|---------|-------------|---------|
| `RUN` | تشغيل العاكس | `RUN` |
| `STOP` | إيقاف العاكس | `STOP` |
| `RST` | إعادة ضبط التنبيهات | `RST` |
| `FREQ <قيمة>` | تعيين التردد (هرتز) | `FREQ 50.0` |
| `DIR <1\|-1>` | تعيين الاتجاه | `DIR 1` (للأمام) |
| `STATUS` | عرض الحالة الكاملة | `STATUS` |
| `HELP` | عرض قائمة الأوامر | `HELP` |

## هيكل المشروع

```
CDE550-sim/
├── main.py              # نقطة دخول التطبيق
├── inverter_sim.py      # منطق محاكاة العاكس
├── serial_handler.py    # معالجة الاتصال التسلسلي
├── script/              # واجهة المستخدم وملفات المساعدة
│   ├── help.py          # نافذة المساعدة
│   ├── serial_dialog.py # نافذة الاتصال التسلسلي
│   └── version.py       # إدارة الإصدارات
├── requirements.txt     # تبعيات المشروع
├── README.md            # الوثائق الرئيسية
└── CHANGELOG.md         # سجل التغييرات
```

## المساهمة

نرحب بالمساهمات! لاقتراح تحسينات:

1. انسخ المشروع
2. أنشئ فرعًا للميزة الجديدة (`git checkout -b feature/AmazingFeature`)
3. احفظ التغييرات (`git commit -m 'إضافة ميزة رائعة'`)
4. ادفع التغييرات إلى الفرع (`git push origin feature/AmazingFeature`)
5. افتح طلب سحب

## الترخيص

مرخص بموجب رخصة GPL-3.0. راجع ملف `LICENSE` لمزيد من المعلومات.

## الاتصال

- المؤلف: Nsfr750
- البريد الإلكتروني: [nsfr750@yandex.com]
- المستودع: https://github.com/Nsfr750/CDE550-sim

---

<div align="center">
  <sub>طوره Nsfr750 بكل ❤️</sub>
</div>
