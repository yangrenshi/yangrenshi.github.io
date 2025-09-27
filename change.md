# 网站双语化修改记录

## 修改时间
2024年12月19日

## 修改内容

### 1. Hugo配置文件修改 (hugo.toml)
- 添加了多语言配置支持
- 配置了中文(zh-cn)和英文(en)两种语言
- 为每种语言设置了独立的菜单导航
- 添加了语言切换器配置
- 在菜单中添加了语言切换链接

### 2. 英文页面内容创建
- 创建了 `content/about/index.en.md` - 英文版关于页面
- 创建了 `content/post/welcome.en.md` - 英文版欢迎文章
- 创建了 `content/post/ai-introduction.en.md` - 英文版AI介绍文章
- 创建了 `content/search/index.en.md` - 英文版搜索页面
- 创建了 `content/_index.md` - 中文版首页
- 创建了 `content/_index.en.md` - 英文版首页
- 创建了 `personal-intro.html` - 全英文个人介绍HTML文件

### 3. 语言切换功能
- 在中文页面添加了"English"切换链接
- 在英文页面添加了"中文"切换链接
- 使用地球图标表示语言切换

## 技术实现
- 使用Hugo的多语言功能
- 每种语言有独立的URL路径（中文：/，英文：/en/）
- 保持了原有的中文内容不变
- 添加了完整的英文翻译

## 访问方式
- 中文版：https://yangrenshi.github.io/
- 英文版：https://yangrenshi.github.io/en/
- 本地测试：http://localhost:1313/ 和 http://localhost:1313/en/
