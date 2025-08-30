---
lang: zh
lang-niv: fonto
lang-ref: 014-jbk
layout: doc
order: 5
title: '图片去重工具'
---

# 图片去重工具

图片去重工具是一个强大的Python应用程序，专为高效管理和删除重复图片而设计。该工具利用Wand库（ImageMagick）进行图像处理，提供先进的视觉比较技术，以高精度识别和管理重复图片。

## 主要功能

- **高级图像处理**：基于Wand/ImageMagick，提供卓越的图像格式支持
- **视觉重复检测**：使用感知哈希算法识别视觉上相似的图片
- **全面格式支持**：支持所有主流图片格式，包括JPEG、PNG、WEBP、PSD等
- **直观界面**：用户友好的图形界面，支持深色/浅色主题
- **多语言支持**：内置英语和意大利语国际化支持
- **批量处理**：高效处理数千张图片
- **预览与比较**：在操作前并排比较图片
- **安全操作**：移至回收站而非永久删除
- **详细日志**：全面的操作日志，便于追踪

## 系统要求

- **Python**：3.8或更高版本（推荐3.10+）
- **ImageMagick**：Wand图像处理所需
  - Windows：从[ImageMagick Windows](https://imagemagick.org/script/download.php#windows)安装
  - macOS：`brew install imagemagick`
  - Linux：`sudo apt-get install libmagickwand-dev`
- **内存**：最低4GB，处理大型图片集推荐8GB以上
- **存储空间**：足够的空间用于处理图片和临时文件
- **操作系统**：
  - Windows 10/11
  - macOS 10.15+
  - 支持X11/Wayland的Linux

## 为什么选择Wand/ImageMagick？

图片去重工具使用Wand（ImageMagick的Python绑定）具有以下优势：

- 更广泛的格式支持，包括PSD、GIF和BMP
- 更好的大图内存管理
- 跨平台行为更一致
- 高级图像处理能力
- 积极的维护和安全更新

## 使用方法

### 主界面

应用程序具有现代化的用户友好界面，包含以下关键组件：

1. **菜单栏**：访问所有应用程序功能和设置
2. **工具栏**：快速访问常用功能
3. **文件夹浏览器**：导航和选择要扫描的目录
4. **预览窗格**：并排查看和比较图片
5. **结果面板**：显示找到的重复项及相似度分数
6. **状态栏**：显示操作进度和系统信息

### 基本工作流程

1. **选择源文件夹**
   - 点击"打开文件夹"按钮或使用`文件 > 打开文件夹`
   - 应用程序将扫描支持的图片格式
   - 支持格式：JPEG、PNG、WEBP、PSD、BMP、GIF等（通过Wand/ImageMagick）

2. **配置扫描设置**
   - 调整相似度阈值（默认：90%）
   - 设置考虑的最小图片大小
   - 选择要比较的图片属性（大小、日期、内容哈希）

3. **开始扫描**
   - 点击"开始扫描"开始重复检测
   - 状态栏显示进度
   - 可随时暂停或停止扫描

4. **查看结果**
   - 显示重复组及预览
   - 按文件大小、日期或相似度分数排序
   - 使用并排比较工具进行验证

5. **管理重复项**
   - 选择要保留或删除的图片
   - 将重复项移至回收站（可恢复）或永久删除
   - 将结果导出为CSV/JSON格式供参考

### 高级功能

#### 批量处理

- 按顺序处理多个文件夹
- 保存和加载扫描配置
- 安排自动扫描

#### 智能选择

- 根据条件自动选择图片（最旧、最小等）
- 保留最高分辨率版本
- 保留最佳质量图片

### 性能优化

- 使用多线程加速扫描
- 智能缓存机制减少重复计算
- 增量扫描仅处理新文件
- 可调整的CPU/内存使用率

## 安装指南

### 从PyPI安装（推荐）

```bash
pip install images-deduplicator
```

### 从源代码安装

1. 克隆仓库：
   ```bash
   git clone https://github.com/Nsfr750/Images-Deduplicator.git
   cd Images-Deduplicator
   ```

2. 安装依赖：
   ```bash
   pip install -r requirements.txt
   ```

3. 运行应用程序：
   ```bash
   python -m images_deduplicator
   ```

## 故障排除

### 常见问题

- **ImageMagick未找到**：确保已正确安装ImageMagick并添加到系统PATH
- **内存不足**：尝试减少同时处理的图片数量
- **处理速度慢**：增加最小文件大小以跳过缩略图
- **大集合处理**：在非高峰时段安排扫描

### 内存管理

- 调整`--max-workers`参数控制并行处理数量
- 使用`--cache-size`限制缓存大小
- 启用`--low-memory`模式减少内存使用

## 贡献指南

欢迎贡献代码、报告问题或提出改进建议。请遵循以下步骤：

1. Fork仓库
2. 创建功能分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 打开拉取请求

## 许可证

本项目采用GNU通用公共许可证v3.0 - 详情请参阅[LICENSE](LICENSE)文件。

## 致谢

- 所有贡献者
- [Wand](https://github.com/emcconville/wand) 和 [ImageMagick](https://imagemagick.org/) 团队
- 测试人员和错误报告者

## 支持

如果您觉得这个项目有用，请考虑支持我的工作：

[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://paypal.me/3dmega)
[![Support](https://img.shields.io/badge/Support-Patreon-ff69b4.svg)](https://www.patreon.com/Nsfr750)

## 联系方式

- 邮箱: nsfr750@yandex.com
- GitHub: [Nsfr750](https://github.com/Nsfr750)
- Discord: [加入](https://discord.gg/ryqNeuRYjD)
