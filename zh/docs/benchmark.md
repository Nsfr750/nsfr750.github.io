---
lang: zh
lang-niv: fonto
lang-ref: 023-jbk
layout: doc
order: 14 # 可选：菜单排序
title: '性能测试工具'
---

[![许可证: GPL v3](https://img.shields.io/badge/许可证-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![代码风格: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

基于PySide6构建的现代Python性能测试工具，提供用户友好的界面来运行和分析Pystone及其他基准测试。

## 📥 安装

### 先决条件

- Python 3.9 或更高版本
- Windows 或 Linux

### 快速开始

1. 克隆仓库：

   ```bash
   git clone https://github.com/Nsfr750/benchmark.git
   cd benchmark
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

4. 运行应用：

   ```bash
   python main.py
   ```

## ✨ 功能特点

- **现代化界面**：基于PySide6构建的简洁响应式界面
- **全面的基准测试**：
  - 可定制的测试时长
  - 实时进度跟踪
  - 详细的统计结果
  - 历史数据对比
- **日志记录**：
  - 详细的操作日志
  - 按级别过滤日志
  - 日志文件轮转
- **多语言支持**：
  - 英语 (en)
  - 意大利语 (it)
- **可访问性**：
  - 键盘快捷键
  - 高对比度模式
  - 可调节文字大小

## ⌨️ 键盘快捷键

- `Ctrl+L`：查看应用日志
- `F1`：显示帮助
- `Esc`：关闭对话框
- `Ctrl+Q`：退出应用

## 📊 使用说明

1. 设置基准测试的迭代次数
2. 点击"开始测试"按钮
3. 实时监控进度
4. 查看详细结果和统计数据
5. 访问日志进行故障排除

## 📂 项目结构

```
benchmark/
├── .github/                            # GitHub Actions
│   ├── workflows/                      # GitHub Actions工作流
│   │   └── ci-cd.yml                   # CI/CD流水线
│   ├── issues/                         # GitHub问题
│   |   └── templates/                  # 问题模板
│   └── FUNDING.yml                     # 赞助文件
├── assets/                             # 资源文件
├── config/                             # 配置文件
│   ├── config.json                     # 配置文件
│   └── updates.json                    # 更新缓存
├── docs/                               # 文档
│   ├── images/                         # 文档图片
│   ├── pdf/                            # PDF文档
│   └── USER_GUIDE.md                   # 用户指南
├── lang/                               # 语言文件
│   ├── en.json                         # 英文语言文件
│   └── it.json                         # 意大利语语言文件
├── logs/                               # 日志文件
├── script/                             # 源代码
│   ├── __init__.py                     # 包初始化
│   ├── about.py                        # 关于对话框
│   ├── benchmark_history.py            # 测试历史记录
│   ├── benchmark_tests.py              # 基准测试
│   ├── CLI_pystone.py                  # 命令行Pystone测试
│   ├── config_manager.py               # 配置管理器
│   ├── export_results.py               # 结果导出
│   ├── hardware_monitor.py             # 硬件监控
│   ├── help.py                         # 帮助对话框
│   ├── history_dialog.py               # 历史记录对话框
│   ├── lang_mgr.py                     # 语言管理器
│   ├── logger.py                       # 日志配置
│   ├── menu.py                         # 菜单栏功能
│   ├── settings.py                     # 设置对话框
│   ├── sponsor.py                      # 赞助对话框
│   ├── system_info.py                  # 系统信息
│   ├── test_menu.py                    # 测试菜单
│   ├── theme_manager.py                # 主题管理器
│   ├── updates.py                      # 更新系统
│   ├── version.py                      # 版本系统
│   ├── view_log.py                     # 日志查看器
│   └── visualization.py                # 测试可视化
├── tests/                              # 测试文件
│   ├── test_benchmark.py               # 基准测试
│   ├── test_hardware_monitor.py        # 硬件监控测试
│   ├── test_monitor_manual.py          # 手动监控测试
│   ├── test_monitor.py                 # 监控测试
│   └── TEST_README.md                  # 测试说明
├── .gitignore                          # Git忽略文件
├── CHANGELOG.md                        # 更新日志
├── CONTRIBUTING.md                     # 贡献指南
├── LICENSE                             # GPLv3许可证
├── main.py                             # 主程序
├── README.md                           # 本文件
├── requirements.txt                    # 依赖文件
└── TO_DO.md                            # 待办事项
```
