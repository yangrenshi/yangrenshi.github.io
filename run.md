# 网站运行逻辑说明

## 项目结构
```
yangrenshi.github.io/
├── hugo.toml                    # Hugo配置文件，包含多语言设置
├── content/                     # 内容目录
│   ├── about/                   # 关于页面
│   │   ├── index.md            # 中文版关于页面
│   │   └── index.en.md         # 英文版关于页面
│   ├── post/                   # 博客文章
│   │   ├── welcome.md          # 中文版欢迎文章
│   │   ├── welcome.en.md       # 英文版欢迎文章
│   │   ├── ai-introduction.md  # 中文版AI介绍
│   │   └── ai-introduction.en.md # 英文版AI介绍
│   └── search/                 # 搜索页面
│       ├── index.md            # 中文版搜索页面
│       └── index.en.md         # 英文版搜索页面
├── themes/stack/               # Hugo主题目录
└── public/                     # 生成的静态网站文件
```

## 运行流程

### 1. 配置文件解析 (hugo.toml)
- Hugo读取配置文件，识别多语言设置
- 解析中文(zh-cn)和英文(en)的语言配置
- 设置每种语言的标题、副标题、菜单等

### 2. 内容处理
- Hugo扫描content目录下的所有.md文件
- 根据文件名后缀(.en.md)识别语言版本
- 没有语言后缀的文件默认为默认语言(zh-cn)

### 3. 页面生成
- 中文页面：生成到根目录(/)
- 英文页面：生成到/en/目录
- 每种语言都有独立的菜单导航

### 4. 语言切换
- 中文页面菜单包含"English"链接，指向/en/
- 英文页面菜单包含"中文"链接，指向/
- 用户可以通过菜单轻松切换语言

## 访问路径
- 中文首页：http://localhost:1313/ 或 https://yangrenshi.github.io/
- 英文首页：http://localhost:1313/en/ 或 https://yangrenshi.github.io/en/
- 中文关于页面：http://localhost:1313/about/
- 英文关于页面：http://localhost:1313/en/about/

## 部署说明
1. 运行 `hugo` 命令生成静态文件到public目录
2. 将public目录内容推送到GitHub Pages
3. 网站将自动支持双语访问
