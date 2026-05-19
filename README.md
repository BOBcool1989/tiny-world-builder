# 迷你世界构建器 🌍

[![Star](https://img.shields.io/github/stars/BOBcool1989/tiny-world-builder?style=social)](https://github.com/BOBcool1989/tiny-world-builder)

> 浏览器里的 3D 体素世界构建器，基于 [jasonkneen/tiny-world-builder](https://github.com/jasonkneen/tiny-world-builder) 本地化

### [👉 在线体验](http://110.42.230.2:8090/)

![3D体素世界](https://github.com/user-attachments/assets/1b19a5f7-def5-42bf-b85f-01714f502afa)

---

## 能做什么

- 🏗️ **拖放搭建** — 体素方块搭建筑、地形、农场
- 🌿 **多种地形** — 草地/沙地/水域/熔岩/雪地
- 🐄 **农场经营** — 养牛羊、种南瓜玉米向日葵
- 🤖 **AI 生成** — 输入一句话，自动生成完整世界（MiniMax / OpenAI / Anthropic / xAI）
- 📐 **程序化生成** — 点击即生成，无需任何 API Key
- 🌦️ **天气系统** — 晴天/雨天/雪天，实时切换
- 💾 **存档导入导出** — 浏览器本地存储，分享给朋友

---

## 快速部署

### 方式一：直接打开（最简单）

下载本仓库，浏览器直接打开 `tiny-world-builder.html`

```bash
git clone https://github.com/BOBcool1989/tiny-world-builder.git
cd tiny-world-builder
# macOS
open tiny-world-builder.html
# Linux
xdg-open tiny-world-builder.html
# Windows
start tiny-world-builder.html
```

### 方式二：本地服务

```bash
cd tiny-world-builder
python3 -m http.server 8080
# 浏览器访问 http://localhost:8080
```

### 方式三：部署到自己的服务器

把整个仓库传到你的 Web 服务器目录（如 `/var/www/tiny-world-builder/`），nginx 配置：

```nginx
server {
    listen 8090;
    server_name _;
    root /var/www/tiny-world-builder;
    index tiny-world-builder.html;
    location / {
        add_header Access-Control-Allow-Origin *;
        try_files $uri $uri/ =404;
    }
}
```

---

## AI 生成功能

### 支持的 AI 提供商

| 提供商 | 默认模型 | 说明 |
|--------|---------|------|
| **MiniMax** | MiniMax-M2.7 | 🇨🇳 国内可用，推荐 |
| OpenAI | gpt-5.5 | 需国际网络 |
| Anthropic | claude-opus-4-7 | 需国际网络 |
| xAI | grok-4.3-latest | 需国际网络 |

### 使用方法

1. 打开 `设置` → `AI` 页签
2. 选择提供商，填入你的 API Key
3. 返回主界面，点击 `生成` → `AI 生成`
4. 输入世界描述（如"有河流的村庄"），等待 AI 生成

> MiniMax API Key 获取：https://platform.minimax.chat（免费额度）

### 程序化生成（无需 API Key）

`生成` → `程序化` — 完全离线，任意使用

---

## 技术栈

- **Three.js** r128 — 3D 渲染
- **纯原生 JS** — ~16k 行，无框架依赖
- **单 HTML 文件** — 零构建，浏览器直开
- **AGPL-3.0** 开源协议

---

## 项目结构

```
tiny-world-builder.html   # 主应用
world.schema.json        # 存档格式定义
vendor/three/            # Three.js 运行时（自托管，不依赖 CDN）
sounds/                  # 音效
models/                  # 3D 模型
plugins/                 # 插件
tools/                   # 静态检查脚本
```

---

## 控制说明

| 操作 | 按键 |
|------|------|
| 放置方块 | 点击格子 |
| 擦除 | `E` 然后点击，或选橡皮擦 |
| 旋转视角 | 拖拽 |
| 缩放 | 滚轮 |
| 升高/降低地形 | `R` / `F` |
| 切换视角 | `P`（等距）或 `I`（透视） |
| 清空为草地 | `C` |
| 打开命令面板 | `⌘ K` |

---

## License

基于 [jasonkneen/tiny-world-builder](https://github.com/jasonkneen/tiny-world-builder) 进行本地化改编。

- 源码修改版本遵循 **AGPL-3.0** 协议开源
- 网络使用必须开源修改版本源码

---

## 关注作者

📕 **小红书**：[上杉的小马驹🐴](https://www.xiaohongshu.com/user/profile/xxx)  
🌐 **在线体验**：[http://110.42.230.2:8090/](http://110.42.230.2:8090/)  
💻 **GitHub**：[BOBcool1989/tiny-world-builder](https://github.com/BOBcool1989/tiny-world-builder)

有问题或建议？欢迎提 Issue！
