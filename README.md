# WeChat Markdown Formatter - Zeabur 部署模板

> Version: 1.0.0 | Last Updated: 2025-12-11

<p align="center">
  <strong>微信公众号 Markdown 排版工具</strong>
</p>

<p align="center">
  将标准 Markdown 转换为适配微信公众号的富文本 HTML<br>
  支持代码高亮、多种主题、脚注引用等特性
</p>

<p align="center">
  🌐 <a href="https://xiangyugongzuoliu.com/">官网</a> |
  📦 <a href="https://github.com/xiangyugongzuoliu/wechat-markdown-formatter-template">GitHub 仓库</a> |
  🐳 <a href="https://hub.docker.com/r/xiangyugongzuoliu/wechat-markdown-formatter">Docker Hub</a>
</p>

---

## 🚀 一键部署

[![Deploy on Zeabur](https://zeabur.com/button.svg)](https://zeabur.com/templates/TFH99L?referralCode=xiangyugongzuoliu)

点击上方按钮，一键部署到 Zeabur。

> **注意：** 部署后请务必修改 `API_TOKEN` 环境变量为自定义值！

---

## ⚙️ 环境变量配置

部署时可配置以下环境变量：

| 变量名 | 说明 | 默认值 | 必填 |
|--------|------|--------|------|
| `API_TOKEN` | API 认证令牌（建议自定义） | `xiangyugongzuoliu` | ✅ |
| `PORT` | 服务端口 | `8081` | ❌ |
| `NODE_ENV` | 运行环境 | `production` | ❌ |

**安全提示：** 部署后请务必修改 `API_TOKEN` 为自定义值，保护你的 API 安全。

---

## 📖 使用说明

### API 端点

```
POST /api/wechat-format
```

### 请求示例

```bash
curl -X POST https://your-domain.zeabur.app/api/wechat-format \
  -H "Authorization: Bearer YOUR_API_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "markdown": "# 你好，微信\n\n这是一段**重要**的文本",
    "theme": "jikehei",
    "font": "cx"
  }'
```

### 请求参数

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `markdown` | string | ✅ | Markdown 文本内容 |
| `theme` | string | ❌ | 主题样式（默认：wechat） |
| `font` | string | ❌ | 字体设置（cx 或 no-cx） |

### 可用主题

`wechat` `chengxin` `jikehei` `kejilan` `qianduan` `quanzhanlan` `mohei` `chazi` `hongfei` `lanqing` `lanying` `lvyi` `menglv` `nenqing` `qiangweizi` `shanchui` `jian`

---

## ✨ 核心功能

- ✅ 完整 Markdown 语法支持（标题、列表、代码块、表格、图片等）
- ✅ 17+ 种精美主题
- ✅ 代码语法高亮（基于 Prettify.js）
- ✅ 智能脚注引用（外部链接自动转为文末脚注）
- ✅ CSS 样式内联（完美适配微信公众号编辑器）
- ✅ 现代 Web 界面（在线编辑、实时预览、一键复制）

---

## 🔧 访问你的服务

部署完成后，你将获得一个 Zeabur 提供的域名：

```
https://your-app-name.zeabur.app
```

访问该地址即可使用 Web 界面，或通过 API 调用。

---

## 📝 项目说明

本项目为自用工具。

---

## 🙏 技术栈

- 后端：Express.js + TypeScript
- Markdown 解析：marked
- 样式处理：juice（CSS 内联）
- 代码高亮：Google Prettify
- 前端：Tailwind CSS + Vanilla JavaScript

---

## 📄 许可说明

本项目基于 Docker 镜像部署，镜像由作者构建并发布。

Docker 镜像：`xiangyugongzuoliu/wechat-markdown-formatter:latest`
