# 📄 个人简历网站 / Personal Resume Website

> 一款基于原生前端技术构建的响应式个人简历网站，适配 PC 端和移动端，清晰展示个人背景、技能栈、项目经历与联系方式。

**在线演示：** [GitHub Pages](https://sinontime.github.io/Personal-Blog)

---

## 📋 目录

- [项目简介](#项目简介)
- [技术栈](#技术栈)
- [功能特性](#功能特性)
- [项目结构](#项目结构)
- [本地运行](#本地运行)
- [部署指南](#部署指南)
- [浏览器兼容](#浏览器兼容)
- [项目亮点](#项目亮点)
- [许可证](#许可证)

---

## 📖 项目简介

本项目是一个**个人简历展示型静态网站**，旨在通过网页形式系统化地展示个人的教育背景、技术能力、项目经历与联系方式。网站采用**响应式设计**，能够在桌面端、平板和手机端提供统一的优质浏览体验。

主要面向求职场景，可作为个人技术品牌展示页，也可作为 GitHub 主页的补充介绍。

---

## 🛠️ 技术栈

### 核心技术

| 技术 | 说明 |
|------|------|
| **HTML5** | 语义化标签（`<header>`、`<main>`、`<section>`、`<footer>`），结构化页面骨架 |
| **CSS3** | Flexbox 弹性布局、CSS Grid 网格布局、CSS 变量、过渡动画、媒体查询 |
| **JavaScript (ES6+)** | 原生 JS 实现 DOM 操作、事件监听、滚动监听、表单交互 |

### 辅助工具

| 工具 | 用途 |
|------|------|
| **Font Awesome 6** | 图标库（社交图标、联系方式图标、时间线图标） |
| **Google Fonts** | 字体优化（Segoe UI 字体系列） |
| **Git** | 版本控制 |
| **GitHub Pages** | 静态网站托管与自动部署 |

### 技术亮点

- **零框架依赖** — 纯原生 HTML5 + CSS3 + JavaScript 实现，无需 React/Vue 等框架即可运行
- **CSS 自定义属性** — 统一的主题色管理（`#66ccff` 主色调贯穿全局）
- **Intersection Observer-like 滚动检测** — 通过 `getBoundingClientRect()` 实现滚动到视口触发动画

---

## ✨ 功能特性

### 1. 🧭 固定导航栏 + 平滑滚动

- 导航栏固定顶部，滚动时呈现阴影效果
- 点击导航链接平滑滚动至对应锚点
- 导航项带有下划线悬停动画（`::after` 伪元素 + `transition`）

### 2. 📱 移动端汉堡菜单

- 屏幕宽度 ≤ 768px 时自动切换为汉堡菜单
- 点击展开/收起导航列表
- 汉堡图标三线条动画（旋转 + 消失变换）

### 3. ⏳ 时间线布局

- 个人经历采用左右交替时间线设计
- 鼠标悬停卡片上浮（`transform: translateY(-5px)`）
- 时间线竖线居中，带有圆形图标指示器

### 4. 📊 技能进度条动画

- 技能项采用网格布局展示
- 当页面滚动到技能区域时，进度条从 `0` 平滑展开至目标百分比
- 使用 `data-progress` 自定义属性存储进度值

### 5. 🖼️ 作品集悬停遮罩

- 作品卡片鼠标悬停时显示半透明遮罩层
- 遮罩包含项目标题、描述与查看按钮

### 6. 📬 联系表单

- 表单输入框聚焦时边框高亮
- 提交后显示成功通知浮层（3 秒自动消失）
- 表单数据打印至控制台（可扩展为后端 API 调用）

### 7. 🔗 社交链接

- 底部社交图标圆形按钮设计
- 悬停时上浮 + 背景色变化

### 8. 📢 通知浮层

- 全局通知组件，从右侧滑入
- 用于表单提交成功、作品链接点击等场景反馈

---

## 📁 项目结构

```
Personal-Blog/
├── index.html            # 主页面（语义化HTML5结构）
├── css/
│   └── style.css         # 全局样式表（响应式布局 + 动画）
├── js/
│   └── script.js         # JavaScript 交互逻辑
├── pic/
│   ├── profile.jpg       # 个人头像
│   └── resume-website.jpg # 作品集截图
├── .gitignore
└── README.md
```

### 文件职责

| 文件 | 职责描述 |
|------|----------|
| `index.html` | 页面结构骨架，包含导航、关于、经历、技能、作品集、联系方式、页脚七大区域 |
| `css/style.css` | 全局样式，涵盖布局（Flex/Grid）、组件样式、动画效果、5 个断点的响应式适配 |
| `js/script.js` | 交互逻辑：汉堡菜单、平滑滚动、技能条动画、表单提交、通知浮层 |

---

## 🚀 本地运行

由于本项目是纯静态网站，无需构建工具或依赖安装，直接使用浏览器打开即可：

### 方式一：直接打开

```bash
# 克隆仓库
git clone https://github.com/sinonTime/Personal-Blog.git

# 打开 index.html
cd Personal-Blog
start index.html          # Windows
open index.html           # macOS
```

### 方式二：使用 Live Server（推荐，支持热更新）

```bash
# 使用 VS Code Live Server 扩展
# 右键 index.html → Open with Live Server
```

```bash
# 或使用 Python 内置服务器
cd Personal-Blog
python3 -m http.server 8080
# 访问 http://localhost:8080
```

---

## 🌐 部署指南

### GitHub Pages 部署

1. 在 GitHub 仓库页面点击 **Settings** → **Pages**
2. **Source** 选择 `Deploy from a branch`
3. **Branch** 选择 `master`，目录选择 `/ (root)`
4. 点击 **Save**
5. 等待几分钟，访问 `https://sinontime.github.io/Personal-Blog`

### 自定义域名（可选）

1. 在 `Settings` → `Pages` 的 **Custom domain** 输入您的域名
2. 在 DNS 服务商添加 CNAME 记录指向 `sinontime.github.io`
3. 在项目根目录创建 `CNAME` 文件（内容为您的域名）

---

## 🌍 浏览器兼容

| 浏览器 | 支持情况 |
|--------|----------|
| Chrome 90+ | ✅ 完全支持 |
| Firefox 88+ | ✅ 完全支持 |
| Safari 14+ | ✅ 完全支持 |
| Edge 90+ | ✅ 完全支持 |
| IE 11 | ⚠️ 部分支持（CSS Grid / Flex 回退降级） |

### 响应式断点

| 断点 | 适配目标 |
|------|----------|
| > 1200px | 桌面大屏 |
| 992px - 1200px | 桌面标准 |
| 768px - 992px | 平板 |
| 576px - 768px | 大屏手机 |
| < 576px | 小屏手机 |

---

## ⭐ 项目亮点

### 1. 纯原生开发
无需任何前端框架或第三方库（除图标库外），展示扎实的 HTML/CSS/JavaScript 基本功。

### 2. 组件化 CSS 设计
样式按功能模块划分（导航栏、时间线、技能条、作品集、联系方式等），便于维护和复用。

### 3. 渐进式交互增强
JavaScript 仅用于增强体验（动画、平滑滚动、菜单切换），即使禁用 JS 页面仍可正常浏览。

### 4. 性能优化
- 无外部依赖加载（Font Awesome 通过 CDN 按需加载）
- 图片使用压缩格式
- CSS 选择器深度控制在 3 层以内

---

## 📄 许可证

本项目采用 **MIT License** 开源协议。

```
MIT License

Copyright (c) 2025 YUANMUMU

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

---

> **作者：** [YUANMUMU](https://github.com/sinonTime)
> 
> **技术反馈：** 如有问题或建议，欢迎提交 [Issue](https://github.com/sinonTime/Personal-Blog/issues)
