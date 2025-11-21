---
title: "代码项目"
date: 2025-01-21T00:00:00+08:00
draft: false
---

# 代码项目

这里展示我的一些开源项目和代码示例。

## 项目展示

### 1. Hugo 主题定制
- **描述**: 基于 PaperMod 主题的个性化定制
- **技术栈**: Hugo, HTML, CSS, JavaScript
- **功能**: 响应式设计、深色模式、搜索功能
- **GitHub**: [项目链接](https://github.com/username/hugo-theme)

### 2. 静态网站生成器
- **描述**: 使用 Go 语言开发的轻量级静态网站生成器
- **技术栈**: Go, Markdown, HTML
- **特点**: 快速构建、零依赖、易于扩展

### 3. 前端组件库
- **描述**: 现代化的 React 组件库
- **技术栈**: React, TypeScript, Tailwind CSS
- **组件**: 按钮、表单、导航、模态框等

## 代码示例

### Go 语言示例

```go
package main

import (
    "fmt"
    "net/http"
)

func handler(w http.ResponseWriter, r *http.Request) {
    fmt.Fprintf(w, "Hello, World!")
}

func main() {
    http.HandleFunc("/", handler)
    http.ListenAndServe(":8080", nil)
}
```

### JavaScript 示例

```javascript
// 深色模式切换
function toggleTheme() {
    const html = document.documentElement;
    const currentTheme = html.getAttribute('data-theme');
    const newTheme = currentTheme === 'dark' ? 'light' : 'dark';

    html.setAttribute('data-theme', newTheme);
    localStorage.setItem('theme', newTheme);
}

// 初始化主题
function initTheme() {
    const savedTheme = localStorage.getItem('theme') || 'light';
    document.documentElement.setAttribute('data-theme', savedTheme);
}
```

### Python 示例

```python
import requests
from bs4 import BeautifulSoup

def scrape_website(url):
    """
    简单的网页爬虫示例
    """
    try:
        response = requests.get(url)
        response.raise_for_status()

        soup = BeautifulSoup(response.content, 'html.parser')
        title = soup.find('title').text if soup.find('title') else 'No title'

        return {
            'title': title,
            'status_code': response.status_code
        }
    except Exception as e:
        return {'error': str(e)}

# 使用示例
result = scrape_website('https://example.com')
print(result)
```

## 技术栈

### 前端技术
- **框架**: React, Vue.js
- **样式**: Tailwind CSS, SCSS
- **构建工具**: Vite, Webpack

### 后端技术
- **语言**: Go, Python, Node.js
- **数据库**: PostgreSQL, MongoDB
- **API**: REST, GraphQL

### 开发工具
- **版本控制**: Git
- **CI/CD**: GitHub Actions
- **容器化**: Docker

## 开源贡献

我积极参与开源社区，主要贡献领域包括：

- Hugo 主题开发
- Go 语言工具库
- 前端组件库
- 文档改进

---

*欢迎查看我的 GitHub 主页获取更多项目信息*