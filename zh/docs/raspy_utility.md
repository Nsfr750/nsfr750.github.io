---
lang: zh
lang-niv: font
lang-ref: 021-jbk
layout: page
title: 'RasPY 实用工具'
---

# RasPY 实用工具

<div align="center">
  <img src="../images/logo.png" alt="RasPY 实用工具标志" width="50%">
</div>

## 欢迎使用 RasPY 实用工具文档

RasPY 实用工具是一个综合应用程序，通过直观的图形界面或REST API控制和监控树莓派GPIO引脚。

## 目录

### 介绍
- [安装](installazione.md)
- [指南](guida.md)

### 开发
- [开发](sviluppo.md)
- [API](api.md)
- [图形界面](gui.md)
- [示例](esempi.md)

### 其他资源
- [更新日志](changelog.md)
- [常见问题](faq.md)

### 社区
- [贡献](contribuire.md)
- [致谢](ringraziamenti.md)

## 主要功能

### ✅ **现代化图形界面**
- 深色/浅色主题
- 多语言支持
- 实时引脚状态可视化
- 系统托盘集成

### 🔌 **完整的GPIO支持**
- 数字输入/输出引脚控制
- 内置模拟器用于开发
- 自动硬件检测
- 远程GPIO支持

### 🌐 **网页界面**
- 内置网页服务器
- 响应式设计，适配移动/桌面设备
- 实时更新
- 集成的API文档

## 快速开始

1. [安装](installazione.md) - 如何安装和配置RasPY实用工具
2. [指南](guida.md) - 应用程序使用指南
3. [API](api.md) - 开发者API文档
4. [开发](sviluppo.md) - 开发和贡献指南

## 用户指南

### 图形界面

RasPY 4 实用工具的图形界面设计直观易用。

#### 主菜单

- **文件**：应用程序通用控制
- **GPIO**：GPIO引脚和模拟器管理
- **视图**：界面自定义
- **帮助**：文档和信息

#### GPIO控制

1. 从菜单打开GPIO控制窗口
2. 选择要控制的引脚
3. 使用按钮切换引脚状态
4. 实时监控状态

#### GPIO模拟器
模拟器允许您在没有物理硬件的情况下测试代码：

1. 从GPIO菜单启动模拟器
2. 使用界面模拟输入/输出
3. 更改会实时反映

### 日志记录和调试
应用程序在`logs/app.log`文件中记录重要事件。使用内置的日志查看器可以：

- 按级别（信息、警告、错误）筛选消息
- 搜索特定消息
- 导出日志进行分析

### 键盘快捷键

- `Ctrl+O`：打开项目
- `Ctrl+S`：保存项目
- `F1`：显示帮助
- `F5`：刷新GPIO状态

## 高级功能

### 远程访问

RasPY实用工具包含一个内置的Web服务器，允许从网络上的任何设备进行远程访问：

1. 在设置中启用Web服务器
2. 配置端口和访问凭据
3. 从任何浏览器连接到树莓派的IP地址和端口

### 自动化脚本

使用Python脚本自动化任务：

```python
from raspy_utility import GPIO

# 初始化GPIO
GPIO.setmode(GPIO.BCM)

# 设置引脚14为输出
GPIO.setup(14, GPIO.OUT)

# 切换引脚状态
GPIO.output(14, not GPIO.input(14))
```

### 插件系统

通过插件扩展功能：

1. 将插件文件放在`plugins/`目录中
2. 从设置中启用/禁用插件
3. 自定义插件行为

## 故障排除

### 常见问题

- **无法检测到GPIO**：
  - 确保已安装正确的Python库
  - 检查用户权限（通常需要`gpio`组）
  - 验证硬件连接

- **Web界面无法访问**：
  - 检查防火墙设置
  - 验证Web服务器是否正在运行
  - 检查端口冲突

- **性能问题**：
  - 减少轮询间隔
  - 禁用未使用的功能
  - 检查系统资源使用情况

## 贡献

欢迎贡献代码、报告问题或提出功能请求。请访问我们的[GitHub仓库](https://github.com/Nsfr750/raspy_utility)。

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
