---
lang: zh
lang-niv: fonto
lang-ref: 016-jbk
layout: doc
order: 7
title: 'NFC读写工具'
---

# 🚀 NFC读写器应用程序

[![许可证: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![代码风格: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

一个基于PySide6的强大应用程序，用于读取和写入各种类型的NFC标签，具有高级功能和用户友好的界面。

## 安装

### 先决条件

- Python 3.9或更高版本
- NFC读卡器硬件（ACR122U、ACR1252U等）

### 快速开始

1. 克隆仓库：

   ```bash
   git clone https://github.com/Nsfr750/NFC.git
   cd NFC
   ```

2. 创建并激活虚拟环境：

   ```bash
   python -m venv venv
   .\venv\Scripts\activate  # Windows
   source venv/bin/activate  # Linux/Mac
   ```

3. 安装依赖：

   ```bash
   pip install -r requirements.txt
   ```

4. 运行应用程序：

   ```bash
   python main.py
   ```

详细安装说明请参见[PREREQUISITES.md](PREREQUISITES.md)。

## 功能特点

- **多标签支持**：全面支持各种NFC标签类型，包括：
  - NTAG (NTAG213, NTAG215, NTAG216)
  - MIFARE Classic (1K, 4K)
  - MIFARE Ultralight
  - FeliCa (Sony)
  - ISO 14443 A/B型卡

- **全面的标签支持**：[查看支持的操作](docs/supported_operations.md)了解所有标签类型

- **NDEF操作**：
  - 读写NDEF记录
  - 创建和管理多个NDEF记录
  - 支持多种NDEF记录类型（文本、URI、智能海报等）
  - 十六进制视图用于原始数据检查

- **标签管理**：
  - 读取标签信息（UID、内存布局、功能）
  - 将数据写入标签并进行验证
  - 锁定标签以防止未经授权的写入
  - 格式化标签以用于NDEF

- **用户界面**：
  - 现代化响应式设计，采用sphinx_rtd_theme
  - 支持浅色/深色/系统主题
  - 实时标签检测和状态更新
  - 详细的标签信息面板
  - 带过滤选项的日志查看器
  - 提供英文和意大利文的全面文档

- **安全特性**：
  - 🔒 敏感操作密码保护
  - 🔑 使用PBKDF2进行安全密码哈希
  - 🔄 密码更改功能
  - ⚙️ 启用/禁用密码保护的切换
  - 🔐 受保护的操作包括标签工具、数据库和克隆器

- **高级功能**：
  - 标签模拟模式（实验性）
  - 批量处理多个标签
  - 自定义命令执行
  - 具有多个详细级别的日志系统
  - 开发人员API文档
  - 常见问题故障排除指南
  - 开源协作的贡献指南

## 使用指南

### 基本操作

1. **连接读卡器**：
   - 将NFC读卡器连接到计算机
   - 应用程序将自动检测并连接

2. **读取标签**：
   - 将NFC标签放在读卡器上
   - 点击"读取"按钮
   - 标签信息将显示在主界面

3. **写入标签**：
   - 选择要写入的数据类型（文本、URL等）
   - 输入数据
   - 点击"写入"按钮

### 高级功能

- **标签模拟**：模拟NFC标签（实验性）
- **自定义命令**：向标签发送原始APDU命令
- **内存视图**：检查和编辑标签原始内存
- **批量操作**：处理多个标签
- **数据库集成**：存储和检索标签数据

## 故障排除

### 常见问题

- **读卡器未检测到**：
  - 检查USB连接
  - 确保已安装正确的驱动程序
  - 尝试不同的USB端口

- **无法读取标签**：
  - 确保标签类型受支持
  - 检查标签是否损坏
  - 尝试重新放置标签

- **写入失败**：
  - 检查标签是否可写
  - 确保有足够的存储空间
  - 验证数据格式是否正确

## 支持与贡献

如果您遇到任何问题或有功能建议，请：
1. 查看[问题跟踪器](https://github.com/Nsfr750/NFC/issues)
2. 提交新的问题或功能请求

欢迎贡献代码！请阅读我们的[贡献指南](CONTRIBUTING.md)以开始。

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
