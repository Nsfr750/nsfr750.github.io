---
lang: ar
lang-niv: fonto
lang-ref: 020-jbk
layout: doc
order: 11
title: 'PySnoop'
---

# PySnoop

[![الرخصة: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.7+](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![أسلوب الكود: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

تطبيق حديث يعمل بلغة Python لقراءة وكتابة وتحليل بيانات الشرائط الممغنطة للبطاقات. يمثل هذا المشروع استمرارًا لمشروع StripeSnoop الأصلي، مع إعادة بنائه باستخدام Python الحديثة وواجهة مستخدم سهلة الاستخدام.

## ✨ الميزات

- **قراءة البطاقات**: قراءة الشرائط الممغنطة للبطاقات باستخدام أجهزة قراءة متوافقة
- **إدارة قاعدة البيانات**: تخزين وإدارة بيانات البطاقات بشكل آمن
- **تنسيقات متعددة**: استيراد/تصدير بيانات البطاقات بتنسيقات مختلفة
- **واجهة مستخدم حديثة**: واجهة سهلة الاستخدام مع دعم السمات
- **متعدد المنصات**: يعمل على أنظمة Windows وmacOS وLinux
- **ملف تنفيذي مستقل**: تجميع التطبيق في ملف تنفيذي واحد لتوزيع سهل
- **إصدارات تصحيح الأخطاء**: تكوين خاص لتصحيح الأخطاء
- **الأمان**: تخزين آمن لبيانات البطاقات الحساسة
- **التحقق**: التحقق المدمج من أرقام البطاقات (C10/Luhn)
- **الوثائق**: وثائق شاملة وأمثلة

## 🚀 التثبيت

### المتطلبات الأساسية

- Python 3.7 أو أحدث
- pip (مدير حزم Python)
- Git (اختياري، للتطوير)

### البدء السريع

1. استنسخ المستودع:

   ```bash
   git clone https://github.com/Nsfr750/PySnoop.git
   cd PySnoop
   ```

2. أنشئ وقم بتفعيل بيئة افتراضية:

   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. قم بتثبيت التبعيات:

   ```bash
   pip install -r requirements.txt
   ```

## 🏗️ بناء التطبيق

يمكن تجميع PySnoop في ملف تنفيذي مستقل باستخدام Nuitka. نوفر سكريبتين للبناء:

### بناء التصحيح

```bash
.\snoop_debug.bat
```

ينشئ إصدار تصحيح من التطبيق مع تفعيل نافذة وحدة التحكم لاستكشاف الأخطاء وإصلاحها.

### بناء الإصدار النهائي

```bash
.\snoop.bat
```

ينشئ إصدارًا محسنًا من التطبيق.

### مخرجات البناء

- بناء التصحيح: `build\PySnoop_debug.exe`
- بناء الإصدار النهائي: `build\PySnoop.exe`

## 🛠️ التطوير
   ```bash
   pip install -r requirements.txt
   ```

## 💻 الاستخدام

### وضع الواجهة الرسومية (موصى به)

```bash
python pysnoop_gui.py
```

### واجهة سطر الأوامر

```bash
python pysnoop.py [خيارات]
```

### الخيارات المتاحة

```bash
-h, --help      إظهار رسالة المساعدة والخروج
-v, --verbose   تفعيل الإخراج المفصل
--version       إظهار معلومات الإصدار
```

## 🔌 الأجهزة المدعومة

- قارئ/كاتب البطاقات الممغنطة MSR605
- أجهزة قراءة بطاقات متوافقة مع HID (تجريبي)

## 📚 الوثائق

الوثائق التفصيلية، بما في ذلك مرجع API وأمثلة الاستخدام، متاحة في [الوثائق](https://nsfr750.github.io/PySnoop/ "PySnoop Documentation").

## 🤝 المساهمة

نرحب بالمساهمات! يرجى قراءة [إرشادات المساهمة](CONTRIBUTING.md) للبدء.

## 📄 الترخيص

هذا المشروع مرخص بموجب ترخيص GPLv3 - راجع ملف [LICENSE](LICENSE) للحصول على التفاصيل.

## 🙏 الدعم

إذا وجدت هذا المشروع مفيدًا، يرجى التفكير في دعم تطويره:

[![تبرع عبر PayPal](https://img.shields.io/badge/Donate-PayPal-blue.svg)](https://paypal.me/3dmega)
[![ادعمنا على Patreon](https://img.shields.io/badge/Support-Patreon-orange.svg)](https://www.patreon.com/Nsfr750)

## 📧 الاتصال

للأسئلة أو الدعم الفني، يرجى فتح issue أو الاتصال بـ [Nsfr750](mailto:nsfr750@yandex.com).

## الشكر والتقدير

- مبني على مشروع StripeSnoop الأصلي (http://stripesnoop.sourceforge.net)

## المساهمة

نرحب بالمساهمات! لا تتردد في إرسال Pull Request.
