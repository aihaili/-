# 卡片生成器

一个功能强大、易于使用的卡片生成工具，支持自定义封面、内容、样式和布局，可用于制作各种类型的知识卡片、宣传卡片等。

## 功能特性

### 🎨 丰富的视觉定制
- **多种配色方案**：内置多种预设配色方案，包括Pastel、Classic Blue、晨露花园、薰衣草田和信纸样式
- **自定义背景**：支持上传自定义背景图片，可调整透明度
- **字体选择**：支持多种中文字体，包括悠哉字体、霞鹜文楷、得意黑、思源黑体等（需手动下载）
- **图层管理**：支持图层的显示/隐藏、拖拽排序，方便管理卡片元素

### ✏️ 强大的编辑功能
- **文本编辑**：支持标题、副标题、内容文本的编辑，可调整字体大小、颜色、粗细、对齐方式等
- **图片支持**：支持上传图片，可拖拽调整位置、缩放大小、旋转角度
- **涂鸦工具**：内置画笔、圆形、椭圆、圆角矩形、三角形、五角星、波浪线等多种涂鸦工具
- **透明黑底**：支持自动抠除图片中的黑色部分，实现透明效果

### 📄 多页面支持
- **封面卡片**：用于展示主题和核心信息
- **内容卡片**：用于展示详细内容，支持多页内容
- **分页导航**：支持上下页切换和页码跳转

### 🤖 AI 助手
- **新闻解析**：支持粘贴新闻内容，自动生成卡片内容
- **多种API支持**：支持OpenAI、Anthropic、Google Gemini、DeepSeek等多种AI服务

### 💾 数据管理
- **配置导入导出**：支持保存和加载配置，方便重复使用
- **批量导出**：支持批量导出所有卡片为图片
- **文档导入**：支持从文本文件导入内容

## 快速开始

1. **下载项目**
   下载项目文件并解压

2. **下载字体**
   请参考「字体下载与安装」章节，下载并安装所需字体

3. **直接打开**
   双击 `index.html` 文件，在浏览器中打开

## 字体下载与安装

由于字体文件较大，无法直接上传到GitHub，您需要手动下载并安装所需字体。

### 推荐字体

1. **悠哉字体**
   - 下载地址：[https://www.maoken.com/freefonts/18043.html](https://www.maoken.com/freefonts/18043.html)
   - 文件名：悠哉字体-常规.ttf, 悠哉字体-细体.ttf

2. **霞鹜文楷**
   - 下载地址：[https://github.com/lxgw/LxgwWenKai/releases](https://github.com/lxgw/LxgwWenKai/releases)
   - 文件名：LXGWWenKai-Regular.ttf, LXGWWenKai-Light.ttf

3. **得意黑**
   - 下载地址：[https://github.com/atelier-anchor/smiley-sans/releases](https://github.com/atelier-anchor/smiley-sans/releases)
   - 文件名：SmileySans-Oblique.otf

4. **思源黑体**
   - 下载地址：[https://github.com/adobe-fonts/source-han-sans/releases](https://github.com/adobe-fonts/source-han-sans/releases)
   - 文件名：SourceHanSansSC-Regular.otf, SourceHanSansSC-Bold.otf, SourceHanSansSC-Light.otf

5. **小赖字体**
   - 下载地址：[https://www.maoken.com/freefonts/13044.html](https://www.maoken.com/freefonts/13044.html)
   - 文件名：小赖字体.ttf

### 安装方法

1. **创建fonts目录**
   在项目根目录下创建一个名为 `fonts` 的目录

2. **复制字体文件**
   将下载的字体文件复制到 `fonts` 目录中

3. **验证安装**
   打开应用后，在字体选择下拉菜单中应该能看到已安装的字体

## 如何使用

### 1. 基本操作

1. **切换卡片类型**：点击「封面卡片」或「内容卡片」按钮切换编辑模式
2. **编辑文本**：在左侧控制面板中输入文本内容，调整文本样式
3. **上传图片**：点击「选择图片」按钮上传图片，然后在预览区拖拽调整位置
4. **调整样式**：在右侧设置面板中选择配色方案，调整背景图片
5. **保存卡片**：点击「保存当前卡片」按钮下载当前卡片为图片

### 2. 高级功能

1. **图层管理**
   - 在左侧「图层管理」区域，点击图层前的眼睛图标可显示/隐藏图层
   - 拖拽图层可调整图层顺序

2. **涂鸦工具**
   - 在图层管理中选择「涂鸦层」
   - 在「涂鸦工具设置」中选择工具类型、调整画笔大小、颜色等
   - 在预览区直接绘制

3. **AI 助手**
   - 在左侧「AI助手设置」区域，选择API提供商并输入API Key
   - 粘贴新闻内容到「新闻内容」文本框
   - 点击「生成卡片」按钮，等待AI生成内容

4. **批量导出**
   - 编辑好所有卡片后，点击「批量保存」按钮
   - 选择是否仅导出文字，然后等待所有卡片导出完成

## 项目结构

```
card-generator/
├── fonts/              # 字体文件（需手动创建并添加字体）
├── js/                 # 第三方库
│   ├── FileSaver.min.js
│   ├── html2canvas.min.js
│   └── jszip.min.js
├── icon.svg            # 图标
├── index.html          # 主页面
├── script-complete.js  # 完整功能脚本
├── script-simple.js    # 简化版脚本
├── script.js           # 基础脚本
├── script.js.new       # 新脚本
├── server.py           # 本地服务器
└── styles.css          # 样式文件
```

> **注意**：fonts目录需要手动创建，并添加下载的字体文件。详见「字体下载与安装」章节。

## 技术栈

- **前端**：HTML5, CSS3, JavaScript (ES6+)
- **第三方库**：
  - html2canvas - 用于将HTML元素转换为图片
  - FileSaver.js - 用于客户端文件保存
  - JSZip - 用于创建和管理ZIP文件
- **字体**：
  - 悠哉字体
  - 霞鹜文楷
  - 得意黑
  - 思源黑体
  - 小赖字体

## 浏览器兼容性

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## 贡献指南

欢迎贡献代码、报告问题或提出建议！

1. **Fork 项目**
2. **创建分支** (`git checkout -b feature/AmazingFeature`)
3. **提交更改** (`git commit -m 'Add some AmazingFeature'`)
4. **推送到分支** (`git push origin feature/AmazingFeature`)
5. **打开 Pull Request**

## 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件

## 致谢

- 感谢所有开源字体的作者
- 感谢所有第三方库的开发者
- 感谢用户的使用和反馈

## 联系方式

- 作者：乂海狸
- GitHub：https://github.com/aihaili
- 小红书：4212737469
- 哔哩哔哩：乂海狸

---

**享受制作卡片的乐趣！** 🎉
