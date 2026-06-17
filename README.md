# 脱水 · dehydrate

把注水的内容挤干，只留**一句话**、几个**关键点**、一句**「所以呢」**，以及一条可直接发出的**「可以这么回」**。

纯本地单文件工具：内容和 API key 都只存在浏览器本地（localStorage），不经过任何自己的服务器，只在调用模型时直连对应厂商接口。

## 用法

直接用浏览器打开 `index.html` 即可（双击，或拖进浏览器）。

首次使用：点右上角 ⚙ 翻到背面，选模型厂商、贴上自己的 API key、选回复语气，点「完成」。然后在正面粘贴文字 / 贴图 / 传文件，点「脱水」。

- 快捷键：在输入框里按 `⌘/Ctrl + Enter` 直接提交。
- 支持直接 `⌘/Ctrl + V` 粘贴图片。

## 支持的输入

文字（粘贴）、图片、PDF、docx、txt / md。
PDF 用 [pdf.js](https://mozilla.github.io/pdf.js/) 解析、docx 用 [mammoth](https://github.com/mwilliamson/mammoth.js) 解析，均走 CDN 加载，故运行时需联网。

## 支持的模型

| 厂商 | 看图 | 备注 |
| --- | --- | --- |
| 智谱 GLM（默认） | ✅ | GLM-4V-Flash 免费、国内直连 |
| 通义千问 Qwen | ✅ | 阿里云百炼 |
| DeepSeek | ❌ | 仅文字 |
| Moonshot Kimi | ✅ | |
| Google Gemini | ✅ | 免费 key，可能需代理 |
| OpenRouter | ✅ | 一个 key 通多家 |

> 注意：部分国产 API 不允许浏览器跨域（CORS）直连，浏览器里可能报「连不上」。遇到时可改用 OpenRouter，或把页面挂到能转发的环境。

## 文件

- `index.html` — 全部代码（HTML + CSS + JS 都在这一个文件里，无构建步骤）。
