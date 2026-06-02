# ✨ 图个明白

> 右键图片，一键生成中英双语 AI 绘图提示词

<p align="center">
  <img src="https://raw.githubusercontent.com/LillltaChen/tuge-mingbai/main/assets/cover.png" width="200" alt="图个明白">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Chrome-Extension-4285F4?logo=googlechrome&logoColor=white" alt="Chrome Extension">
  <img src="https://img.shields.io/badge/Manifest-V3-green" alt="Manifest V3">
  <img src="https://img.shields.io/badge/License-MIT-blue" alt="License">
</p>

---

## 这是什么？

「图个明白」是一款 Chrome 浏览器扩展。当你在浏览网页时看到一张喜欢的图片，右键点击它，AI 会在 3-8 秒内分析图片内容，生成结构化的中英双语提示词 —— 直接复制到 Midjourney、GPT Image 2、Nano Banana、即梦 等 AI 生成平台即可复现类似风格。

**核心口号：让每一张图片，都被读懂。**

---

## 🎬 演示视频

![演示：右键图片生成 AI 提示词](https://raw.githubusercontent.com/LillltaChen/tuge-mingbai/main/assets/demo.gif)

> 在任意网页右键点击图片，3-8 秒内获得结构化提示词。

## ✨ 功能特性

| 功能 | 说明 |
|------|------|
| 🖱️ **右键即用** | 在任意网页右键点击图片，无需离开当前页面 |
| 🌐 **中英双语** | 同时输出英文 Prompt + 中文提示词，支持实时编辑互译 |
| 🏷️ **风格标签** | 自动提取 4-6 个关键词（主题、风格、光线、色彩、情绪）|
| ⚡ **本地缓存** | LRU 缓存最近 20 条结果，重复图片秒出 |
| 📦 **批量分析** | 支持多张图片队列分析，带进度面板 |
| 🎨 **精美浮窗** | 毛玻璃效果、可拖拽缩放、明暗主题切换 |
| 🔒 **隐私优先** | API Key 与历史记录仅存储在本地浏览器 |

---

## 📦 安装方法

1. 下载或克隆本仓库
2. 打开 Chrome，进入 `chrome://extensions/`
3. 开启右上角「开发者模式」
4. 点击「加载已解压的扩展程序」，选择本项目文件夹
5. 点击扩展图标，配置 API Key 即可使用

### 配置说明

| 配置项 | 说明 | 默认值 |
|--------|------|--------|
| API Key | OpenAI / Gemini / Claude 密钥 | — |
| Base URL | API 服务地址 | `https://api.openai.com` |
| 模型 | 需支持 Vision 能力 | `gpt-4o` |

> 💡 兼容任意 OpenAI 格式接口，包括中转 API。

---

## 🚀 使用方法

1. 在任意网页上 **右键点击图片**
2. 选择「✨ 图个明白：生成 AI 提示词」
3. 等待分析完成，结果以浮窗形式展示
4. 点击「复制」一键复制提示词
5. 点击关键词标签可单独复制

---

## 🛠 技术栈

- **Chrome Extension Manifest V3**
- **Vanilla JavaScript** — 零框架依赖，体积 < 100KB
- **OpenAI Chat Completions API（Vision）**
- **chrome.storage.local** — 本地持久化

---

## 📁 项目结构

```
.
├── manifest.json          # 扩展配置入口
├── background.js          # Service Worker：菜单 / API / 缓存
├── content.js             # 内容脚本：浮窗 UI / 交互 / 主题
├── popup.html / popup.js  # 扩展弹窗
├── options.html / options.js  # 设置页面
├── icons/                 # 扩展图标（16/32/48/128px）
└── README.md              # 本文件
```

---

## 🎯 设计哲学

- **隐形的工具** — 没有常驻 UI，只在右键菜单中静静等待
- **愉悦的细节** — 扫描动画、复制涟漪、拖拽弹性、主题切换
- **尊重隐私** — 数据不出本地

---

## 👤 开发者

基于 AI 技术，由 **CHEN** 设计开发

- GitHub: [@LillltaChen](https://github.com/LillltaChen)
- 项目主页: 本仓库

---

## 📄 License

MIT License
