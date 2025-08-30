---
lang: zh
lang-niv: fonto
lang-ref: 018-jbk
layout: page
title: 'OpenPGP 图形界面应用'
---

# OpenPGP 图形界面应用文档

欢迎阅读**OpenPGP 图形界面应用**的官方文档。

## 概述
本应用提供了一个现代化的用户友好界面，用于OpenPGP密钥管理、加密、解密、消息签名、验证以及SSL证书生成。所有加密操作均在本地执行，确保最高级别的隐私保护。

# 功能特点

- 采用ttkbootstrap的现代化UI（超级英雄主题）
- 生成、加载和导出OpenPGP密钥对
- 设置密钥名称、邮箱、密码短语，并查看指纹
- 加密和解密消息
- 签名和验证消息（分离式签名）
- 以ASCII-armor格式（.asc）导出公钥
- 可视化密钥指纹以进行安全检查
- 使用自定义CN生成SSL证书
- 一键清除/重置所有字段
- **集中式日志系统**（信息、警告、错误、未捕获的异常）
- **带实时过滤功能的日志查看器**（全部、信息、警告、错误）
- 使用`log_info`、`log_warning`、`log_error`记录自定义日志条目
- 自动捕获回溯信息并在日志查看器中显示
- 动态菜单栏，包含关于、帮助、日志查看器、赞助、版本对话框
- 语义化版本控制和版本信息
- 模块化结构（`struttura`、`gui`等）
- 易于扩展和主题定制（通过ttkbootstrap）

# 快速开始

## 系统要求
- Python 3.9或更高版本
- PySide6（包含在requirements中）
- pgpy（包含在requirements中）
- cryptography（包含在requirements中）
- pyperclip（包含在requirements中）

> **注意**：本应用已从Tkinter/ttkbootstrap迁移到PySide6，以获得更现代化和可维护的UI。

## 安装
1. 克隆或下载此仓库。
2. （可选）创建虚拟环境：
   ```
   python -m venv venv
   venv\Scripts\activate
   ```
3. 安装依赖：
   ```
   pip install -r requirements.txt
   ```

## 运行应用
从项目根目录运行：
```
python main.py
```

如果遇到导入错误，请确保从根目录运行，而不是在子文件夹内。

# 用户指南

## 主窗口概览
- 输入您的姓名、邮箱和密码短语以生成密钥。
- 选择算法（当前支持RSA；更多算法即将推出）。
- 使用按钮生成、加载或导出密钥。
- 显示已加载/生成的密钥指纹以供验证。
- 使用文本区域输入要加密、解密、签名或验证的消息。
- 导出公钥以安全共享。
- 从图形界面生成SSL证书。
- 使用"清除"按钮重置所有字段。

## 菜单栏
- **文件**：导出公钥、退出
- **日志**：查看日志（可筛选全部、信息、警告、错误）
- **帮助**：帮助、关于、赞助

## 日志和日志查看器
- 自动记录所有信息、警告、错误和未捕获的异常。
- 在脚本中使用`log_info(msg)`、`log_warning(msg)`、`log_error(msg)`进行自定义日志记录。
- 日志查看器（日志 > 查看日志）允许按级别筛选和查看日志。
- 如果日志文件丢失，将显示上次运行时的回溯信息（如果有）。

## 提示
- 所有加密操作均在本地完成（无云服务）。
- 为获得最佳效果，请使用强密码短语。
- 日志窗口提供反馈和错误详情。

# 高级用法

## 导出公钥
- 使用"导出公钥"按钮或菜单项以ASCII-armor格式（.asc）保存公钥。

## 生成SSL证书
1. 在"SSL证书"部分输入通用名称（CN）
2. 点击"生成证书"按钮
3. 证书和密钥将显示在文本区域中
4. 使用"保存证书"和"保存私钥"按钮保存文件

## 故障排除

### 常见问题
- **导入错误**：确保所有依赖项已正确安装。
- **密钥生成失败**：检查输入字段是否有效。
- **日志文件过大**：定期清理日志文件或调整日志级别。

### 日志位置
- Windows: `%APPDATA%\OpenPGP_GUI\logs\app.log`
- Linux/macOS: `~/.openpgp_gui/logs/app.log`

## 开发

### 项目结构
```
openpgp_gui/
├── gui/           # 图形用户界面组件
├── core/          # 核心功能（加密、解密等）
├── utils/         # 工具函数和辅助模块
├── resources/     # 图标和其他资源
└── tests/         # 单元测试
```

### 依赖项
- **PySide6** — 图形用户界面
- **pgpy** — OpenPGP加密
- **cryptography** — SSL证书生成
- **Pillow** — （可选）用于图标

## 如何贡献
1. Fork仓库
2. 创建功能分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 打开拉取请求

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
