---
lang: zh
lang-niv: fonto
lang-ref: 020-jbk
layout: page
title: 'PySnoop 磁卡读写工具'
---

# PySnoop

[![许可证: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.7+](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![代码风格: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

一个基于Python的现代应用程序，用于读取、写入和分析磁条卡数据。本项目是原始StripeSnoop项目的延续，使用现代Python和用户友好界面重建。

## ✨ 功能特点

- **卡片读取**：使用兼容读卡器读取磁条卡
- **数据库管理**：安全存储和管理卡片数据
- **多格式支持**：以多种格式导入/导出卡片数据
- **现代化GUI**：支持主题的用户友好界面
- **跨平台**：支持Windows、macOS和Linux
- **独立可执行文件**：可构建为单个可执行文件，便于分发
- **调试版本**：专门用于故障排除的调试配置
- **安全性**：敏感卡片数据的安全存储
- **验证**：内置卡号验证（C10/Luhn算法）
- **文档**：全面的文档和示例

## 🚀 安装

### 先决条件

- Python 3.7或更高版本
- pip (Python包管理器)
- Git (可选，用于开发)

### 快速开始

1. 克隆仓库：

   ```bash
   git clone https://github.com/Nsfr750/PySnoop.git
   cd PySnoop
   ```

2. 创建并激活虚拟环境：

   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. 安装依赖：

   ```bash
   pip install -r requirements.txt
   ```

## 🏗️ 构建应用程序

PySnoop可以使用Nuitka构建为独立可执行文件。我们提供两个构建脚本：

### 调试版本

```bash
.\snoop_debug.bat
```

这将创建一个调试版本的应用，启用控制台窗口以便故障排除。

### 发布版本

```bash
.\snoop.bat
```

这将创建一个优化过的发布版本应用。

### 构建输出

- 调试版本：`build\PySnoop_debug.exe`
- 发布版本：`build\PySnoop.exe`

## 🛠️ 开发

### 设置开发环境

1. 克隆仓库并创建虚拟环境（如上述"快速开始"部分）
2. 安装开发依赖：

   ```bash
   pip install -r requirements-dev.txt
   ```

### 运行测试

```bash
pytest
```

## 💻 使用方法

### GUI模式（推荐）

```bash
python pysnoop_gui.py
```

### 命令行模式

```bash
python pysnoop_cli.py [options]
```

#### 命令行选项

- `-r, --read`：从读卡器读取卡片
- `-w, --write`：写入卡片
- `-f, --file`：指定输入/输出文件
- `-d, --database`：使用数据库存储/检索卡片
- `-v, --verbose`：详细输出
- `--version`：显示版本信息

## 📦 功能详情

### 卡片操作

- **读取**：从磁条卡读取数据
- **写入**：将数据写入磁条卡
- **验证**：验证卡号（C10/Luhn算法）
- **擦除**：安全擦除卡片数据

### 数据管理

- **数据库**：本地SQLite数据库存储卡片信息
- **导入/导出**：支持多种格式（CSV、JSON、XML）
- **搜索**：按各种标准搜索卡片
- **批量处理**：一次处理多张卡片

### 安全功能

- **加密存储**：敏感数据加密存储
- **访问控制**：可选的密码保护
- **审计日志**：记录所有关键操作

## 📚 文档

完整的文档可在[docs](docs/)目录中找到，包括：

- 用户指南
- 开发者文档
- API参考
- 示例代码

## 🤝 贡献

欢迎贡献代码、报告问题或提出功能请求。请访问我们的[GitHub仓库](https://github.com/Nsfr750/PySnoop)。

## 📄 许可证

本项目采用GNU通用公共许可证v3.0 - 详情请参阅[LICENSE](LICENSE)文件。

## 🙏 支持

如果您觉得这个项目有用，请考虑支持我的工作：

[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://paypal.me/3dmega)
[![Support](https://img.shields.io/badge/Support-Patreon-ff69b4.svg)](https://www.patreon.com/Nsfr750)

## 📧 联系方式

- 邮箱: nsfr750@yandex.com
- GitHub: [Nsfr750](https://github.com/Nsfr750)
- Discord: [加入](https://discord.gg/ryqNeuRYjD)
