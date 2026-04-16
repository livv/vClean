# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

vClean 是一个 macOS 应用程序的官方网站，该应用是专为 Xcode 开发者设计的编译目录清理工具。网站包含以下页面：

- **index.html** - 主页面，展示应用功能特色、截图和下载信息
- **privacypolicy.html** - 隐私政策页面，详细说明应用的隐私保护承诺

## 项目结构

```
vClean_pages/
├── index.html              # 主页面
├── privacypolicy.html      # 隐私政策页面
├── README.md              # 项目说明
├── vClean_sample.png      # 应用截图
└── CLAUDE.md              # 本文件
```

## 开发说明

### 技术栈
- **前端**: 纯 HTML5 + CSS3 + JavaScript (无框架)
- **样式**: 内联 CSS，响应式设计
- **脚本**: 原生 JavaScript，主要用于平滑滚动和导航栏效果
- **兼容性**: 适配 macOS 15.6+ 系统

### 主要功能
1. **响应式导航栏** - 滚动时背景透明度变化
2. **平滑滚动** - 锚点链接平滑滚动到对应区域
3. **功能展示** - 6 个功能卡片展示应用特色
4. **截图展示** - 应用界面截图展示
5. **下载区域** - Mac App Store 下载入口
6. **隐私保护声明** - 强调本地数据处理承诺

### 代码约定
- 所有文本内容使用中文
- CSS 采用 BEM-like 命名风格（如 `.nav-container`, `.hero-content`）
- JavaScript 使用原生 API，无依赖
- 媒体查询处理移动端适配（最大宽度 768px）

## 常用操作

### 本地预览
由于是静态网站，可以直接在浏览器中打开 `index.html` 进行预览。

### 编辑内容
1. **修改文本内容** - 直接编辑对应 HTML 文件中的文本节点
2. **更新样式** - 在 `<style>` 标签内修改 CSS
3. **更新截图** - 替换 `vClean_sample.png` 文件
4. **更新版本信息** - 修改 `index.html` 中 `.version-info` 的内容

### 测试验证
- 在桌面浏览器中测试响应式布局
- 在移动设备模拟器中测试移动端显示
- 验证所有链接和锚点跳转正常工作

## 部署说明
网站可直接部署到任何静态网站托管服务（如 GitHub Pages、Netlify、Vercel 等），无需构建步骤。

## 注意事项
- 隐私政策强调应用不收集任何个人数据，所有操作都在本地完成
- 下载按钮目前使用 JavaScript alert 提示用户在 Mac App Store 中下载
- 如需添加新的功能卡片，需在 `index.html` 中 `.features` 网格内添加新的 `.feature-card` 元素