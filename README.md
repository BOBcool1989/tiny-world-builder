# 迷你世界构建器 🌍

[![Star](https://img.shields.io/github/stars/BOBcool1989/tiny-world-builder?style=social)](https://github.com/BOBcool1989/tiny-world-builder)

> 浏览器里的 3D 体素世界构建器，基于 [jasonkneen/tiny-world-builder](https://github.com/jasonkneen/tiny-world-builder) 本地化

---

## 🚀 快速部署到自己的服务器

本项目为单 HTML 文件，零依赖，可直接部署到任意 Web 服务器：

```bash
# 1. 克隆仓库
git clone https://github.com/BOBcool1989/tiny-world-builder.git
cd tiny-world-builder

# 2. 上传到服务器（以 nginx 为例）
scp -r . root@你的服务器:/var/www/tiny-world-builder/

# 3. nginx 配置
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

或本地直接用浏览器打开 `tiny-world-builder.html`，无需任何服务。

---

## ✨ 功能一览

- 🏗️ **拖放搭建** — 体素方块搭建筑、地形、农场
- 🌿 **多种地形** — 草地/沙地/水域/熔岩/雪地
- 🐄 **农场经营** — 养牛羊、种南瓜玉米向日葵
- 🤖 **AI 生成** — 输入提示词自动生成世界（MiniMax / OpenAI / Anthropic / xAI）
- 📐 **程序化生成** — 无需 API Key，离线可用
- 🌦️ **天气系统** — 晴天/雨天/雪天实时切换
- 💾 **存档导入导出** — 浏览器本地存储

---

## AI 生成功能

### 支持的 AI 提供商

| 提供商 | 默认模型 | 备注 |
|--------|---------|------|
| **MiniMax** | MiniMax-M2.7 | 🇨🇳 国内可直接使用，推荐 |
| OpenAI | gpt-5.5 | 需国际网络 |
| Anthropic | claude-opus-4-7 | 需国际网络 |
| xAI | grok-4.3-latest | 需国际网络 |

### 使用方法

1. `设置` → `AI` 页签，选择 **MiniMax**，填入你的 API Key
2. 点击工具栏 `生成` 按钮
3. 输入世界描述（如"漂浮在云海上的魔法村庄"）
4. 等待 AI 生成

> **MiniMax API Key**：https://platform.minimax.chat 注册即有免费额度

### 程序化生成（无需 Key）

`生成` → 勾选 `程序化（离线）` → 完全免费，无需任何账户

---

## 🕹️ 操作说明

| 操作 | 按键 |
|------|------|
| 放置方块 | 左键点击 |
| 擦除 | `E` + 点击，或选橡皮擦工具 |
| 旋转视角 | 拖拽画面 |
| 缩放 | 滚轮 |
| 升高/降低地形 | `R` / `F` |
| 切换等距/透视视角 | `P` / `I` |
| 清空为草地 | `C` |
| 命令面板 | `⌘ K` |

---

## 🏗️ 技术栈

- **Three.js** r128 — 3D 体素渲染
- **纯原生 JS** — ~16k 行，无框架依赖
- **单 HTML 文件** — 零构建，浏览器直开
- **AGPL-3.0** 开源协议

---

## 项目结构

```
tiny-world-builder.html   # 主应用（直接浏览器打开即可）
world.schema.json        # 存档格式
vendor/three/            # Three.js 运行时
sounds/                  # 音效
models/                  # 3D 模型
plugins/                 # 插件
```

---

## License

基于 [jasonkneen/tiny-world-builder](https://github.com/jasonkneen/tiny-world-builder) 进行本地化改编。

- 修改版本遵循 **AGPL-3.0** 协议开源
- 使用网络功能须开源源码

---

## 关注作者

📕 **小红书**：上杉的小马驹🐴
💻 **GitHub**：[BOBcool1989/tiny-world-builder](https://github.com/BOBcool1989/tiny-world-builder)

有问题或建议？欢迎提 Issue！
