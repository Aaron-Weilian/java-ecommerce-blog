# 电商Java开发技术博客

这是一个基于Hugo静态网站生成器的技术博客框架，专门用于分享电商Java开发技术内容。

## 功能特性

- 使用Hugo Theme TechDoc主题，适合技术文档展示
- 自动GitHub Pages部署，提交Markdown文章后自动构建发布
- 支持分类、标签、归档等组织方式
- 代码高亮、搜索功能
- 响应式设计，移动端友好

## 快速开始

### 1. 安装Hugo

```bash
# 安装Hugo扩展版本（v0.120.4或更高）
# 参考：https://gohugo.io/installation/
```

### 2. 克隆此仓库并初始化主题

```bash
git clone <your-repo-url>
cd 技术博客
git submodule add https://github.com/thingsym/hugo-theme-techdoc themes/hugo-theme-techdoc
```

### 3. 本地预览

```bash
hugo server -D
```

访问 http://localhost:1313 查看效果。

### 4. 撰写新文章

```bash
hugo new posts/文章标题.md
```

编辑 `content/posts/文章标题.md` 文件。

### 5. 部署到GitHub Pages

1. 将代码推送到GitHub仓库的main分支
2. GitHub Actions会自动构建并部署到Pages
3. 访问 https://rabbit0610sc.github.io/ 查看在线博客

## 目录结构

```
技术博客/
├── archetypes/          # 文章模板
├── content/            # 网站内容
│   ├── posts/         # 博客文章
│   └── about.md       # 关于页面
├── static/            # 静态资源
├── themes/            # Hugo主题
│   └── hugo-theme-techdoc/
├── .github/workflows/ # GitHub Actions工作流
│   └── deploy.yml     # 自动部署配置
└── config.toml        # 网站配置
```

## 配置说明

### 基本配置

- `baseURL`: GitHub Pages地址
- `title`: 网站标题
- `theme`: 使用的主题名称

### 菜单配置

在 `config.toml` 的 `[[menu.main]]` 部分可以添加或修改导航菜单。

### 主题配置

详细主题配置请参考 [Hugo Theme TechDoc文档](https://github.com/thingsym/hugo-theme-techdoc)。

## 自动化流程

### 每日机会报告集成

博客框架已准备好与每日机会报告系统集成：

1. 每日生成的电商Java项目机会报告可以自动发布到博客
2. 每周技术短文直接使用Hugo文章格式
3. 所有内容自动归档和分类

### 后续扩展

- 添加评论系统（如Utterances）
- 集成分析工具（如Google Analytics）
- 添加SEO优化
- 支持多语言

## 注意事项

1. 确保GitHub仓库已启用Pages功能（设置 > Pages > Source选择GitHub Actions）
2. 首次部署可能需要手动触发工作流
3. 主题需要作为子模块添加，否则构建会失败
4. 建议定期更新Hugo版本和主题版本