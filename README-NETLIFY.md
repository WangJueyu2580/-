# 学生口译助手 - Netlify 部署指南

## 📦 部署到 Netlify

这个文件夹包含了完整的静态网站文件，可以直接部署到 Netlify。

### 方法 1：拖拽上传（最简单）

1. 访问 [Netlify Drop](https://app.netlify.com/drop)
2. 将整个文件夹拖拽到页面中
3. 等待部署完成，获得公开链接

### 方法 2：使用 Netlify CLI

```bash
# 安装 Netlify CLI
npm install -g netlify-cli

# 登录 Netlify
netlify login

# 部署
netlify deploy --prod --dir=.
```

### 方法 3：连接 Git 仓库

1. 将代码推送到 GitHub/GitLab
2. 在 Netlify 中连接仓库
3. 配置构建命令：`pnpm build`
4. 发布目录：`dist/public`

## 🔧 配置说明

- **_redirects**：处理 SPA 路由，所有请求都指向 index.html
- **netlify.toml**：Netlify 配置文件，包含缓存和安全头设置

## ⚙️ 使用前的重要步骤

### 1. 配置 DeepSeek API

部署后，用户需要：
1. 访问网站
2. 点击右上角设置按钮（⚙️）
3. 填入 DeepSeek API 密钥
4. 保存设置

**API 密钥仅存储在浏览器本地，不会上传到服务器。**

### 2. 获取 DeepSeek API 密钥

访问 [DeepSeek Platform](https://platform.deepseek.com) 获取 API 密钥。

## 📱 功能

- ✅ 中英文实时翻译
- ✅ 语音识别（Web Speech API）
- ✅ 文字转语音
- ✅ 翻译历史记录
- ✅ 完全离线运行（除了 API 调用）
- ✅ 无需服务器

## 🔒 隐私说明

- API 密钥仅存储在您的浏览器中
- 翻译内容不会保存到任何服务器
- 所有数据处理都在客户端进行

## 📊 文件大小

- HTML: ~368 KB
- CSS: ~118 KB
- JavaScript: ~619 KB

## 🚀 性能优化建议

如果需要进一步优化：
1. 启用 Gzip 压缩（Netlify 默认启用）
2. 使用 CDN 加速（Netlify 默认提供）
3. 考虑代码分割以减少初始加载

## 📞 支持

如有问题，请检查：
1. 浏览器控制台是否有错误
2. DeepSeek API 密钥是否正确
3. 网络连接是否正常

---

**祝您使用愉快！** 🎉
