# DDBOT-WSa 命令可视化生成器

一个单页 HTML 工具，为 [DDBOT-WSa](https://github.com/cnxysoft/DDBOT-WSa) 提供可视化的命令拼装界面。在浏览器中双击打开即可使用。

![screenshot](https://img.shields.io/badge/status-ready-success)

## 功能

- **40+ 条命令完整覆盖** — 基于 `cnxysoft/DDBOT-WSa` 源码精确提取，包含所有群聊命令和私聊管理命令
- **可视化参数表单** — 根据参数类型自动生成合适的控件：文本框、数字框、下拉选择、开关 toggle、标签输入
- **实时命令预览** — 每填一个参数，底部立即生成完整命令字符串
- **一键复制** — 点击按钮复制到剪贴板，直接粘贴到 QQ 使用
- **深色模式** — 默认深色，可切亮色，刷新保持
- **零依赖** — 单个 `.html` 文件，CSS/JS 全内联，无需任何构建步骤或网络

## 使用方法

1. 下载 [`ddbot-command-builder.html`](ddbot-command-builder.html)
2. 双击用浏览器打开
3. 左侧选择命令 → 右侧填写参数 → 底部复制 → 粘贴到 QQ

### 快捷键

| 按键 | 功能 |
|------|------|
| `⌘K` / `Ctrl+K` | 聚焦搜索框 |
| `Esc` | 清空搜索 |

## 命令来源

所有命令参数（名称、类型、默认值、枚举值、必填/可选、权限要求）均提取自 `cnxysoft/DDBOT-WSa` 源码：

- `lsp/command.go` — 命令名常量
- `lsp/groupCommand.go` — 群聊命令 kong struct 定义
- `lsp/privateCommand.go` — 私聊/管理命令 kong struct 定义
- `lsp/iCommand.go` — 权限检查逻辑

## 部署

由于是纯静态 HTML 文件，可以部署到任何地方：

- **本地**：双击打开
- **GitHub Pages**：推送到 `gh-pages` 分支
- **任意静态托管**：Nginx / Caddy / Vercel / Netlify

```bash
# 一键部署到 GitHub Pages
gh repo edit --pages-branch main
```

## 许可证

本项目基于 [AGPL-3.0](LICENSE) 协议开源。

---

基于 [cnxysoft/DDBOT-WSa](https://github.com/cnxysoft/DDBOT-WSa) 源码生成。感谢 [Sora233](https://github.com/Sora233) 和 [cnxysoft](https://github.com/cnxysoft) 的 DDBOT 项目。
