---
lang: zh
lang-niv: fonto
lang-ref: 019-jbk
layout: doc
order: 10
title: 'PDF 重复文件查找器'
---

# PDF 重复文件查找器

[![许可证: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![代码风格: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

一个强大的工具，用于在计算机上查找和管理重复的PDF文件。PDF重复文件查找器帮助您识别和删除重复的PDF文档，节省磁盘空间并更有效地组织文件。

## ✨ 功能特点

- 🔍 **智能PDF比较**：基于内容而不仅仅是文件名或大小查找重复的PDF文件
- 📝 **基于文本的比较**：使用高级文本分析识别即使有轻微视觉差异的重复文件
- 👁 **内置PDF查看器**：直接在应用程序中预览PDF文件
- 📋 **双视图界面**：在单独的标签页中查看文件列表和重复组
- 🎯 **高级筛选**：按文件大小、修改日期和名称模式进行筛选
- 🚀 **快速扫描**：优化的算法可快速扫描大量PDF文件集合
- 🎨 **直观的用户界面**：简洁友好的界面，支持浅色/深色主题
- 🔄 **批量处理**：一次性处理多个文件或整个文件夹
- 📊 **详细分析**：查看文件详情、预览和比较结果
- 🛠 **高级工具**：多选模式、筛选和排序选项
- 🌍 **多语言支持**：支持多种语言
- 📊 **进度跟踪**：实时显示文件处理进度条
- ⏱ **最近文件**：通过上下文菜单快速访问最近打开的文件

## 📦 安装

### 先决条件

- Python 3.8 或更高版本
- pip (Python包管理器)
- 可选的PDF渲染后端（自动安全回退）：
  - PyMuPDF (fitz) — 默认并通过requirements安装
  - Ghostscript (用于Wand) — 安装Ghostscript并在设置中设置其可执行路径

请参阅[PREREQUISITES.md](PREREQUISITES.md)获取特定于平台的设置说明。

### 从源代码安装

1. 克隆仓库：

   ```bash
   git clone https://github.com/Nsfr750/PDF_finder.git
   cd PDF_finder
   ```

2. 创建并激活虚拟环境（推荐）：

   ```bash
   python -m venv venv
   .\venv\Scripts\activate  # Windows
   source venv/bin/activate  # Linux/Mac
   ```

3. 安装所需的依赖项：

   ```bash
   pip install -r requirements.txt
   ```

## 使用方法

1. 启动应用程序：

   ```bash
   python main.py
   ```

2. 点击"扫描文件夹"选择要扫描重复PDF文件的目录。

3. 在主窗口中查看结果。扫描完成后，文件列表将自动填充扫描到的PDF文件和重复组。

4. 使用工具管理重复文件：
   - 标记要保留的文件
   - 删除不需要的重复文件
   - 在操作前预览文件

## 主要功能详情

### 智能PDF比较

- 使用高级哈希算法比较PDF内容
- 即使文件名或元数据不同也能检测到相似文档
- 可配置的相似度阈值，以获得更精确的结果

### 性能优化

- 多线程扫描，处理速度更快
- 高效处理大型PDF文件的内存使用
- 进度跟踪和取消支持

### 用户体验

- 直观的界面，清晰的视觉反馈
- 可自定义的视图和布局选项
- 详细的文件信息和元数据显示

### 高级功能

- 批量重命名和移动文件
- 导出扫描结果和报告
- 自定义扫描配置文件和预设

## 故障排除

### 常见问题

- **扫描速度慢**：
  - 尝试增加扫描线程数
  - 排除大型或系统文件夹
  - 确保有足够的可用内存

- **PDF渲染问题**：
  - 确保已安装所有必需的PDF渲染后端
  - 检查文件权限和路径中的特殊字符

- **内存不足**：
  - 减少同时处理的文件数量
  - 增加系统虚拟内存
  - 关闭其他内存密集型应用程序

## 贡献

欢迎贡献代码、报告问题或提出功能请求。请访问我们的[GitHub仓库](https://github.com/Nsfr750/PDF_finder)。

## 许可证

本项目采用GNU通用公共许可证v3.0 - 详情请参阅[LICENSE](LICENSE)文件。

## 支持

如果您觉得这个项目有用，请考虑支持我的工作：

[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://paypal.me/3dmega)
[![Support](https://img.shields.io/badge/Support-Patreon-ff69b4.svg)](https://www.patreon.com/Nsfr750)

## 联系方式

- 邮箱: nsfr750@yandex.com
- GitHub: [Nsfr750](https://github.com/Nsfr750)
- Discord: [加入](https://discord.gg/ryqNeuRYjD)
