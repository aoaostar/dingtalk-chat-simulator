# 钉钉聊天记录模拟器

一个纯前端的钉钉聊天记录模拟工具，单文件 HTML，无需构建、无需后端，打开即用。

在线体验：<https://www.aoaostar.com/dingtalk-chat-simulator/>

> 注：账号的 GitHub Pages 配置了自定义域名，`aoaostar.github.io` 会自动跳转到 `www.aoaostar.com`，两个地址均可使用。

## 功能

- **聊天记录编辑**：左侧编辑、右侧实时预览，所见即所得
- **单聊 / 群聊**：一键切换会话类型，群聊显示成员昵称，单聊自动隐藏
- **成员管理**：添加、删除、重命名成员，支持自定义头像
  - 文字头像：钉钉风格浅蓝底 + 蓝字，自动取名字前两字
  - 图片头像：上传本地图片（≤3MB）作为头像，可随时还原为文字头像
- **消息编辑**：选发送者（任意成员或"我"）、输入内容，支持上移、下移、删除
- **消息类型**：文本消息、时间分割、系统消息（如"xxx 加入群聊"）
- **会话设置**：自定义群名 / 对方名、我的昵称、我的头像
- **导出长图**：一键导出为 PNG 图片，适合分享或存档

## 使用方法

1. 用浏览器打开 `index.html`（本地双击或访问线上地址）
2. 在左侧"会话设置"中填写群名和我的昵称
3. 在"群成员"中编辑发言人的名字和头像
4. 在"消息内容"中选择发送者、输入内容，点击"添加消息"
5. 右侧预览确认效果后，点击"导出长图 PNG"保存

## 部署到 GitHub Pages

项目为单文件静态页面，`index.html` 已在仓库根目录，直接开启 Pages 即可：

1. 进入仓库 **Settings → Pages**
2. **Source** 选择 `Deploy from a branch`
3. **Branch** 选择 `main`，目录选择 `/ (root)`，点击 **Save**
4. 等待约 1 分钟，访问 `https://www.aoaostar.com/dingtalk-chat-simulator/`（或 `https://aoaostar.github.io/dingtalk-chat-simulator/`，会自动跳转）

也可以通过命令行推送到已有仓库：

```bash
git init
git add .
git commit -m "feat: 钉钉聊天记录模拟器"
git branch -M main
git remote add origin git@github.com:aoaostar/dingtalk-chat-simulator.git
git push -u origin main
```

## 技术说明

- 原生 HTML + CSS + JavaScript，无框架、无构建步骤
- 导出长图依赖 [html2canvas](https://html2canvas.hertzen.com/)（CDN 引入，导出时需联网）
- 头像图片以 base64 形式保存在页面内存中，刷新后重置，不会上传到任何服务器

## 说明

本工具仅用于界面演示、原型设计与产品示意，生成内容不涉及真实通信数据，请勿用于伪造聊天记录等不当用途。

## License

MIT
