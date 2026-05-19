# 🎮 迷你世界构建器 - 0基础部署教程

> 原文：https://github.com/BOBcool1989/tiny-world-builder

---

## 方法一：电脑直接打开（最简单⭐⭐⭐）

适合：只是想自己玩，不想折腾服务器

**步骤：**

1. 打开电脑浏览器（Chrome/Edge/QQ浏览器都行）
2. 地址栏输入：直接打开上方仓库里的 `tiny-world-builder.html` 文件
3. 开始玩！

**找不到文件？**
去这个链接下载整个项目 → 解压 → 双击 `tiny-world-builder.html`

---

## 方法二：部署到免费托管平台（免费⭐⭐）

适合：想分享给朋友，有GitHub账号

### 第一步：Fork项目

1. 打开链接：https://github.com/BOBcool1989/tiny-world-builder
2. 点击右上角 **Fork**（叉子图标）
3. 等待1分钟，自动创建完成

### 第二步：开启免费托管

1. 点击仓库 Settings（设置）
2. 左侧找到 **Pages**
3. Source 选 **Deploy from a branch** → Branch 选 **main** → 保存
4. 等待2分钟

### 第三步：打开你的网站

访问：`https://你的用户名.github.io/tiny-world-builder`

找到你的用户名：浏览器右上角点头像 → 你的用户名就是

---

## 方法三：部署到国内服务器（稳定⭐⭐⭐）

适合：想稳定访问、有自己的云服务器

### 准备

- 一台云服务器（推荐阿里云/腾讯云，最便宜的就行）
- 域名（可选）

### 步骤

**1. 连接服务器**

Windows用户：
- 下载 [FinalShell](http://www.hostbuf.com/) 或 Xshell
- 新建连接 → SSH → 填服务器IP和密码

Mac/Linux用户：
- 打开终端，输入：
  ```
  ssh root@你的服务器IP
  ```
- 输入密码

**2. 安装宝塔面板（可视化运维）**

```bash
# 复制这条命令，回车执行
wget -O install.sh https://download.bt.cn/install/install_6.0.sh && bash install.sh
```

等待5分钟 → 记录面板地址和账号密码

**3. 添加网站**

1. 浏览器打开宝塔面板地址（上面显示的）
2. 登录 → 左侧 **网站** → **添加站点**
3. 域名填你的IP（如 `123.45.67.89`）
4. 根目录选 `/www/wwwroot/tiny-world-builder`
5. 创建

**4. 上传项目文件**

1. 本地下载项目并解压
2. 宝塔面板 → 文件 → 找到你刚才的站点目录
3. 把解压出来的**所有文件**上传进去
4. 确保 `tiny-world-builder.html` 在最外层

**5. 访问**

浏览器打开：`http://你的服务器IP:8090`

---

## 常见问题

**Q：打开是空白页？**
A：确保 `tiny-world-builder.html` 在网站根目录，不在任何子文件夹里

**Q：3D很卡？**
A：Chrome浏览器 Ctrl+Shift+R 强制刷新清理缓存

**Q：AI生成功能用不了？**
A：去 `设置` → `AI` → 选 MiniMax → 填API Key（免费申请：platform.minimax.chat）

**Q：想改端口？**
A：宝塔面板 → 网站 → 设置 → 配置文件，找到 `listen 8090` 改成其他数字

---

有问题欢迎评论区留言！
