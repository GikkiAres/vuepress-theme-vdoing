---
title: YamlFrontMatter
date: 2023-06-14 01:51:39
permalink: /pages/6918ca/
categories:
  - 02_VuePress
tags:
  - 
author: 
  name: xugaoyi
  link: https://github.com/xugaoyi
---
1,任何包含 YAML front matter 的 Markdown 文件都将由 [gray-matter (opens new window)](https://github.com/jonschlinkert/gray-matter)处理

2,front matter 必须是 markdown 文件中的第一部分，并且必须采用在三点划线之间书写的有效的 YAML。 这是一个基本的例子：

```
---
xxx
---

yyy
```

在这些三条虚线之间，你可以设置预定义变量（参见[下面](https://v1.vuepress.vuejs.org/zh/guide/frontmatter.html#预定义变量)），甚至可以创建自己的自定义变量。 然后，您可以使用 `$frontmatter` 在页面的其余部分、以及所有的自定义和主题组件访问这些变量。







## 参考资料

```
https://github.com/jonschlinkert/gray-matter
jonschlinkert/gray-matter
```

```
Front Matter
https://v1.vuepress.vuejs.org/zh/guide/frontmatter.html#%E5%85%B6%E4%BB%96%E6%A0%BC%E5%BC%8F%E7%9A%84-front-matter
```

