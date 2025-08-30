---
lang: zh
lang-niv: fonto
lang-ref: 013-jbk
layout: doc
order: 4
title: '邮件重复清理工具'
---

# 📧 邮件重复清理工具

一个全面的Python工具，用于扫描、识别和删除多个邮件客户端中的重复邮件。提供网页、桌面和命令行界面。

## 🚀 版本

**当前版本:**
[![GitHub release](https://img.shields.io/badge/release-v2.5.2-green)](https://github.com/Nsfr750/EmailDuplicateCleaner)
[![Documentation](https://img.shields.io/badge/docs-available-brightgreen)](https://github.com/Nsfr750/EmailDuplicateCleaner/blob/master/README.md)
[![Python Versions](https://img.shields.io/badge/python-3.8%20|%203.9%20|%203.10%20|%203.11%20|%203.12-blue)](https://www.python.org/)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![PyPI](https://img.shields.io/pypi/v/email-duplicate-cleaner)](https://pypi.org/project/email-duplicate-cleaner/)
[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://paypal.me/3dmega)
[![Support](https://img.shields.io/badge/Support-Patreon-ff69b4.svg)](https://www.patreon.com/Nsfr750)

## ✨ 2.5.2 版本更新

- 🚀 更新至2.5.2版本
- 🐛 修复了关于对话框中版本号显示的问题
- 📚 更新了文档以反映最新更改

## ✨ 2.5.1 版本更新

- 🐛 修复了PySide6 GUI中的QAction导入错误
- 🌐 添加了完整的英文翻译
- 📄 包含了GPL-3.0许可证文件
- 🔄 改进了GUI初始化中的错误处理
- ⬆️ 更新了依赖项以提高稳定性

## ✨ 功能特点

### 🔍 重复检测

- 多种检测标准：
  - 严格模式：全面比较
  - 仅内容：分析邮件正文
  - 头部：基于元数据匹配
  - 主题+发件人：针对性识别

### 📊 邮件分析

- 高级邮件分析：
  - 发件人分析：识别主要发件人和域名
  - 时间线分析：可视化邮件时间模式
  - 附件分析：文件类型、大小和频率
  - 会话分析：查看和管理邮件线程
  - 重复分析：详细的重复检测分析
  - 支持多种格式导出报告（文本、HTML、JSON）

### 🖥️ 多界面支持

- **网页界面** - 现代化响应式设计，支持深色/浅色模式
- **桌面GUI** - 使用PySide6的原生桌面体验
- **命令行界面** - 强大的自动化和脚本支持

### 🌓 增强用户体验

- 支持深色/浅色模式的现代化网页界面
- 实时更新的交互式预览
- 全面的帮助系统
- 带有详细日志的调试模式
- 用于测试和学习的演示模式

### 🔒 邮件客户端兼容性

支持：

- Mozilla Thunderbird
- Apple Mail
- Microsoft Outlook
- 通用mbox/maildir格式

### 🏗️ 技术亮点

- 使用Flask构建的现代化网页界面
- 使用SQLAlchemy进行数据库管理
- 包含动态内容的全面帮助系统
- 关注点分离的模块化架构
- 跨平台兼容性
- 全面的错误处理和日志记录

## 🛠️ 系统要求

- Python 3.8+
- pip
- 支持的操作系统：Windows、macOS、Linux

## 🚀 快速开始

### 安装

```bash
pip install email-duplicate-cleaner
```

### 网页界面

```bash
email-duplicate-cleaner-web
```

### 桌面GUI

```bash
email-duplicate-cleaner-gui
```

### 命令行界面

```bash
email-duplicate-cleaner --help
```

## 📂 项目结构

- `email_cleaner_web.py`: 网页界面
- `email_cleaner_gui.py`: 桌面GUI
- `email_duplicate_cleaner.py`: 核心功能和CLI
- `static/`: 网页资源（CSS、JS）
- `templates/`: HTML模板
- `docs/`: 文档
- `tests/`: 测试文件

## 🤝 贡献

欢迎提交问题和拉取请求！

## 📄 许可证

GNU General Public License v3.0

## 🙏 支持

如果您觉得这个项目有用，请考虑支持我的工作：

[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://paypal.me/3dmega)
[![Support](https://img.shields.io/badge/Support-Patreon-ff69b4.svg)](https://www.patreon.com/Nsfr750)

## 📧 联系方式

- 邮箱: nsfr750@yandex.com
- GitHub: [Nsfr750](https://github.com/Nsfr750)
- Discord: [Join](https://discord.gg/ryqNeuRYjD)
