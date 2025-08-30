---
lang: ar
lang-niv: fonto
lang-ref: 023-jbk
layout: doc
order: 14 # اختياري: للترتيب في القائمة
title: 'الاختبار المعياري'
---

[![الترخيص: GPL v3](https://img.shields.io/badge/الترخيص-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![بايثون 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![نمط الكود: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

أداة حديثة للاختبار المعياري بلغة بايثون مبنية باستخدام PySide6، توفر واجهة مستخدم سهلة الاستخدام لتشغيل وتحليل اختبارات Pystone واختبارات معيارية أخرى.

## 📥 التثبيت

### المتطلبات الأساسية

- بايثون 3.9 أو أحدث
- ويندوز أو لينكس

### البدء السريع

1. استنسخ المستودع:

   ```bash
   git clone https://github.com/Nsfr750/benchmark.git
   cd benchmark
   ```

2. أنشئ ونشط بيئة افتراضية:

   ```bash
   python -m venv venv
   .\venv\Scripts\activate  # ويندوز
   source venv/bin/activate  # لينكس/ماك
   ```

3. قم بتثبيت التبعيات:

   ```bash
   pip install -r requirements.txt
   ```

4. شغل التطبيق:

   ```bash
   python main.py
   ```

## ✨ الميزات

- **واجهة مستخدم عصرية**: واجهة نظيفة وسريعة الاستجابة مبنية باستخدام PySide6
- **اختبار معياري شامل**:
  - مدة اختبار قابلة للتخصيص
  - تتبع التقدم في الوقت الفعلي
  - نتائج مفصلة مع إحصائيات
  - مقارنة بالبيانات التاريخية
- **التسجيل**:
  - سجلات تشغيل مفصلة
  - تصفية السجلات حسب المستوى
  - تدوير ملفات السجل
- **دعم متعدد اللغات**:
  - الإنجليزية (en)
  - الإيطالية (it)
- **إمكانية الوصول**:
  - اختصارات لوحة المفاتيح
  - وضع التباين العالي
  - حجم خط قابل للتعديل

## ⌨️ اختصارات لوحة المفاتيح

- `Ctrl+L`: عرض سجلات التطبيق
- `F1`: عرض المساعدة
- `Esc`: إغلاق النوافذ المنبثقة
- `Ctrl+Q`: إغلاق التطبيق

## 📊 طريقة الاستخدام

1. عيّن عدد التكرارات للاختبار المعياري
2. انقر على "بدء الاختبار المعياري" للبدء
3. راقب التقدم في الوقت الفعلي
4. اعرض النتائج التفصيلية والإحصائيات
5. الوصول إلى السجلات لاستكشاف الأخطاء وإصلاحها

## 📂 هيكل المشروع

```
benchmark/
├── .github/                            # إجراءات GitHub
│   ├── workflows/                      # سير عمل GitHub Actions
│   │   └── ci-cd.yml                   # خط أنابيب CI/CD
│   ├── issues/                         # مشكلات GitHub
│   |   └── templates/                  # قوالب المشكلات
│   └── FUNDING.yml                     # ملف التمويل
├── assets/                             # ملفات الأصول
├── config/                             # ملفات التكوين
│   ├── config.json                     # ملف التكوين
│   └── updates.json                    # ذاكرة التخزين المؤقت للتحديثات
├── docs/                               # الوثائق
│   ├── images/                         # صور الوثائق
│   ├── pdf/                            # وثائق PDF
│   └── USER_GUIDE.md                   # دليل المستخدم
├── lang/                               # ملفات اللغة
│   ├── en.json                         # ملف اللغة الإنجليزية
│   └── it.json                         # ملف اللغة الإيطالية
├── logs/                               # ملفات السجل
├── script/                             # الكود المصدري
│   ├── __init__.py                     # تهيئة الحزمة
│   ├── about.py                        # مربع حوار "حول"
│   ├── benchmark_history.py            # سجل الاختبارات المعيارية
│   ├── benchmark_tests.py              # اختبارات معيارية
│   ├── CLI_pystone.py                  # اختبار Pystone المعياري من سطر الأوامر
│   ├── config_manager.py               # مدير التكوين
│   ├── export_results.py               # تصدير النتائج
│   ├── hardware_monitor.py             # مراقب الأجهزة
│   ├── help.py                         # مربع حوار المساعدة
│   ├── history_dialog.py               # مربع حوار السجل
│   ├── lang_mgr.py                     # مدير اللغة
│   ├── logger.py                       # تكوين التسجيل
│   ├── menu.py                         # وظائف شريط القوائم
│   ├── settings.py                     # مربع حوار الإعدادات
│   ├── sponsor.py                      # مربع حوار الرعاة
│   ├── system_info.py                  # معلومات النظام
│   ├── test_menu.py                    # قائمة الاختبار
│   ├── theme_manager.py                # مدير السمة
│   ├── updates.py                      # نظام التحديثات
│   ├── version.py                      # نظام الإصدار
│   ├── view_log.py                     # عارض السجلات
│   └── visualization.py                # تصور الاختبارات المعيارية
├── tests/                              # ملفات الاختبار
│   ├── test_benchmark.py               # اختبار معياري
│   ├── test_hardware_monitor.py        # اختبار مراقب الأجهزة
│   ├── test_monitor_manual.py          # اختبار يدوي للمراقب
│   ├── test_monitor.py                 # اختبار المراقب
│   └── TEST_README.md                  # ملف README للاختبارات
├── .gitignore                          # ملف .gitignore
├── CHANGELOG.md                        # سجل التغييرات
├── CONTRIBUTING.md                     # إرشادات المساهمة
├── LICENSE                             # ملف الترخيص GPLv3
├── main.py                             # التطبيق الرئيسي
├── README.md                           # هذا الملف
├── requirements.txt                    # ملف المتطلبات
└── TO_DO.md                            # قائمة المهام
```
