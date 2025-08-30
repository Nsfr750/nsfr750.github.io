---
lang: zh
lang-niv: fonto
lang-ref: 017-jbk
layout: doc
order: 8
title: 'Nidec CommanderCDE 驱动器控制工具'
---

# Nidec CommanderCDE 驱动器控制工具

一个全面的Python GUI应用程序，用于通过Modbus RTU控制和监控Nidec Commander CDE驱动器。

## ✨ 功能特点

- **多语言支持**：完整的中英文界面，支持动态语言切换
- **多型号支持**：兼容CDE400、CDE550、CDE750和CDE1100S驱动器型号
- **驱动器控制**：
  - 通过RS-485/Modbus RTU连接Nidec Commander CDE驱动器
  - 控制电机速度和方向
  - 启动/停止驱动器
  - 实时监控驱动器状态和诊断信息
  - 故障检测和复位功能
  - 参数备份和恢复
- **用户界面**：
  - 现代化的标签式界面，直观易用
  - 包含实时指标的全面仪表板
  - 状态栏显示连接和驱动器状态
  - 响应式设计，支持深色/浅色主题
  - 可自定义的界面元素
- **数据管理**：
  - 实时监控和记录驱动器参数
  - 数据导出为CSV/Excel格式
  - 参数趋势图表可视化
  - 可配置的数据记录间隔
- **诊断功能**：
  - 全面的参数监控
  - 故障历史记录和日志
  - 系统状态指示器
  - 实时性能指标

## 🆕 v0.0.4 版本新功能

### 新增功能
- 添加了对多种Nidec驱动器型号的支持（CDE400、CDE550、CDE750、CDE1100S）
- 为所有UI元素添加了完整的意大利语翻译
- 增强了帮助系统，提供详细文档
- 为帮助部分添加了蓝色主题，提高可读性

### 改进
- 更新了用户界面，提升用户体验
- 改进了错误消息和日志记录
- 优化了实时监控性能
- 解决了PyQt6兼容性问题
- 修复了帮助对话框中的语言切换问题

## 🚀 系统要求

- Python 3.8或更高版本
- PyQt6 >= 6.6.1
- pyserial >= 3.5
- pymodbus >= 3.5.4
- PyQt6-QScintilla >= 2.14.1
- python-dotenv >= 1.0.0

## 🛠 安装与设置

1. 克隆仓库：

   ```bash
   git clone https://github.com/Nsfr750/nidec-commandercde.git
   cd nidec-commandercde
   ```

2. 创建并激活虚拟环境（推荐）：

   ```bash
   python -m venv venv
   # Windows系统：
   .\venv\Scripts\activate
   # Unix或MacOS系统：
   # source venv/bin/activate
   ```

3. 安装所需软件包：

   ```bash
   pip install -r requirements.txt
   ```

## 🚀 基本用法

1. 通过RS-485适配器将Nidec Commander CDE驱动器连接到计算机
2. 启动应用程序：

   ```bash
   python main.py
   ```

3. 选择适当的COM端口和波特率
4. 点击"连接"按钮与驱动器建立通信
5. 使用界面控制电机速度、方向和其他参数
6. 监控实时数据和系统状态

## 📊 主要功能区域

### 仪表板
- 显示关键参数和状态信息
- 实时更新驱动器数据
- 快速访问常用功能

### 参数设置
- 查看和修改驱动器参数
- 保存和加载参数配置文件
- 重置为默认设置

### 数据记录
- 配置数据记录设置
- 启动/停止数据记录
- 导出记录的数据进行分析

### 诊断
- 查看系统状态和错误代码
- 访问故障历史记录
- 执行系统诊断测试

## 🔧 故障排除

### 常见问题

- **无法连接到驱动器**：
  - 检查RS-485连接是否正确
  - 确认COM端口设置正确
  - 验证波特率与驱动器设置匹配

- **通信错误**：
  - 检查电缆连接是否牢固
  - 确认终端电阻设置正确
  - 验证Modbus地址设置

- **参数无法保存**：
  - 确保驱动器处于正确的操作模式
  - 检查参数是否可写
  - 验证用户权限级别

## 🤝 贡献

欢迎贡献代码、报告问题或提出功能请求。请访问我们的[GitHub仓库](https://github.com/Nsfr750/nidec-commandercde)。

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
