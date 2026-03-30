# 个人简历 & 作品集网站

一个现代化、响应式的个人网站，包含简历展示、作品集展示、博客文章和联系表单等功能。

## 功能特点

- ✨ **响应式设计**：完美适配桌面端、平板和手机
- 🎨 **现代UI风格**：渐变配色、流畅动画、卡片式布局
- 📝 **完整功能模块**：
  - 首页 Hero 展示
  - 关于我（个人信息+技能展示）
  - 项目作品展示
  - 博客文章模块
  - 联系方式表单
- 🔧 **易于定制**：所有内容都是模板化，只需替换[方括号]中的内容
- 🚀 **纯静态网站**：无需数据库，部署简单

## 文件结构

```
personal-website/
├── index.html          # 主页面文件
├── style.css           # 样式文件
├── script.js           # 交互脚本
└── README.md          # 说明文档
```

## 快速开始

### 1. 编辑个人信息

打开 `index.html` 文件，搜索并替换以下内容：

**基本信息：**
- `[你的名字]` → 你的真实姓名
- `[你的职位/身份]` → 如：全栈工程师、UI设计师等
- `[你的专业领域]` → 如：Web开发、移动应用等
- `[你的工作内容]` → 如：用户界面、后端服务等
- `[X]年行业经验` → 填写具体年数

**联系方式：**
- `[your-email@example.com]` → 你的邮箱地址
- `[+86 XXX XXXX XXXX]` → 你的电话号码
- `[你的城市，国家]` → 你的所在地
- `[你的学历]` → 如：本科、硕士等

### 2. 添加个人简介

在"关于我"部分添加你的详细介绍，包括：
- 教育背景
- 工作经历
- 个人兴趣
- 职业目标

### 3. 设置技能专长

找到技能展示部分，修改以下内容：
- `[技能1]` → 如：JavaScript
- `[技能2]` → 如：React.js
- `[技能3]` → 如：Python
- `[技能4]` → 如：UI设计

调整 `style="width: 90%;"` 中的百分比来设置技能熟练度。

### 4. 添加项目作品

找到项目卡片部分，添加你的项目信息：
- `[项目名称1]` → 项目名称
- `[项目描述]` → 详细描述项目功能和特点
- `[技术1]`、`[技术2]` → 项目使用的技术栈
- `href="#"` → 替换为实际的项目演示链接和代码仓库链接

### 5. 发布博客文章

找到博客卡片部分，添加你的文章：
- `[文章标题1]` → 文章标题
- `[文章摘要]` → 文章内容摘要
- `[2024-XX-XX]` → 发布日期
- `[分类]` → 文章分类
- `href="#"` → 替换为实际文章链接

### 6. 替换图片

网站中使用了占位符图标，替换为真实图片：

**方法1：直接替换HTML**
```html
<!-- 找到 -->
<div class="image-placeholder">
    <i class="fas fa-user-circle"></i>
    <p>个人照片</p>
</div>

<!-- 替换为 -->
<img src="your-photo.jpg" alt="个人照片" style="width: 100%; height: 100%; object-fit: cover; border-radius: 50%;">
```

**方法2：添加图片资源**
1. 创建 `images` 文件夹
2. 将你的图片放入其中
3. 修改HTML中的图片路径

### 7. 配置社交媒体链接

在页面底部找到社交媒体链接部分，修改 `href` 属性：
```html
<a href="https://github.com/yourusername" class="social-link"><i class="fab fa-github"></i></a>
<a href="https://linkedin.com/in/yourusername" class="social-link"><i class="fab fa-linkedin"></i></a>
<a href="https://twitter.com/yourusername" class="social-link"><i class="fab fa-twitter"></i></a>
```

## 自定义样式

### 修改主题色

打开 `style.css`，找到 CSS 变量部分：

```css
:root {
    --primary-color: #667eea;    /* 主色调 */
    --secondary-color: #764ba2;  /* 次要色 */
    --text-color: #333;          /* 文字颜色 */
    --light-text: #666;          /* 浅色文字 */
    --bg-color: #f8f9fa;         /* 背景色 */
    --white: #ffffff;            /* 白色 */
    --dark: #1a1a2e;             /* 深色 */
}
```

修改这些颜色值即可改变整个网站的主题色。

### 修改字体

网站使用 Google Fonts 的 Noto Sans SC 字体，可以替换为其他字体：

```html
<!-- 在 index.html 的 <head> 中替换 -->
<link href="https://fonts.googleapis.com/css2?family=你的字体&display=swap" rel="stylesheet">
```

```css
/* 在 style.css 中修改 */
body {
    font-family: '你的字体', sans-serif;
}
```

## 部署网站

### 方式1：GitHub Pages（推荐）

1. 创建 GitHub 仓库
2. 上传所有文件
3. 进入仓库设置 → Pages
4. 选择 `main` 分支作为源
5. 几分钟后即可通过 `https://yourusername.github.io/repo-name` 访问

### 方式2：Netlify

1. 注册 Netlify 账号
2. 拖拽包含网站文件的文件夹到 Netlify
3. 自动部署完成，获得域名

### 方式3：Vercel

1. 安装 Vercel CLI：`npm i -g vercel`
2. 在项目目录运行：`vercel`
3. 按照提示完成部署

### 方式4：传统服务器

将文件上传到你的 Web 服务器（如 Nginx、Apache）的网站根目录即可。

## 联系表单配置

当前网站的联系表单是前端演示版本，如需实际发送邮件，需要：

1. **使用 Formspree**（简单方案）：
   - 注册 Formspree 账号
   - 获取表单 URL
   - 修改 HTML 表单：`<form action="https://formspree.io/f/your-id" method="POST">`

2. **使用 EmailJS**：
   - 注册 EmailJS 账号
   - 配置邮件服务
   - 修改 script.js 中的表单提交逻辑

3. **后端集成**：
   - 创建后端 API 接口
   - 前端通过 AJAX 提交数据

## 性能优化建议

1. **图片优化**：使用 WebP 格式，适当压缩图片
2. **代码压缩**：使用工具压缩 CSS 和 JS 文件
3. **CDN 加速**：使用 CDN 加载字体和图标库
4. **懒加载**：为图片添加懒加载属性 `loading="lazy"`

## 浏览器兼容性

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ⚠️ IE 不支持

## 技术栈

- HTML5
- CSS3 (Flexbox, Grid, CSS Variables)
- JavaScript (ES6+)
- Font Awesome 6.4.0 (图标库)

## 自定义和扩展

### 添加新的部分

1. 在 `index.html` 中添加新的 `<section>`
2. 在 `style.css` 中添加对应的样式
3. 在 `script.js` 中添加交互逻辑（如需要）

### 修改导航菜单

在 `index.html` 中找到 `.nav-menu` 部分，添加或删除菜单项：
```html
<li><a href="#new-section">新部分</a></li>
```

### 添加动画效果

网站已包含基础动画，可通过修改 `style.css` 中的 `transition` 属性调整动画速度和效果。

## 常见问题

**Q: 如何修改网站标题？**
A: 修改 `index.html` 中的 `<title>个人简历 & 作品集</title>`

**Q: 如何添加更多项目？**
A: 复制项目卡片代码块，粘贴到相应位置并修改内容

**Q: 如何去除返回顶部按钮？**
A: 在 `script.js` 中删除创建和绑定返回顶部按钮的代码

**Q: 网站在移动端显示异常？**
A: 检查媒体查询是否正确配置，确保 `<meta name="viewport">` 标签存在

## 许可证

此模板为 MIT 许可证，可自由使用和修改。

## 联系方式

如有问题或建议，欢迎通过网站中的联系表单或社交媒体联系我。

---

**祝你的个人网站建设顺利！** 🎉