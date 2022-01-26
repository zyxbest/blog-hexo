---
title: 使用Hexo+Github+Hexo-theme-matery搭建自己的blog
date: 2022-01-25 22:36:02
tags: blog
---

## 我觉得很 dio 的几件事情

1. Github pages 可以免去自己使用服务器的麻烦， 将自己的个人静态博客网站发布到 github 的公网，可以给大家访问
2. Hexo 体积很小，下载起来飞快，运行也飞快，并且支持热部署。
   之前用 vuepress，修改 config 需要重新跑，每次时间很久，有些受不了
3. 样式美观，功能齐全，完全满足了我的需求和虚荣

## 操作步骤

### github 上的 quick start

https://github.com/hexojs/hexo#quick-start

#### Install Hexo

```bash
 npm install hexo-cli -g
```

#### Setup your blog

```bash
 hexo init blog
 cd blog
```

#### Start the server

```bash
hexo server
```

#### Create a new post or page

```bash
hexo new "Hello Hexo"
```

#### 部署到 github pages

https://hexo.io/docs/github-pages
等跑完 github actions 就可以在 你的姓名.github.io/你的项目 网站上看到效果了

## 遇到问题

1. 代码块显示异常

   https://github.com/zyxbest/image/blob/master/codeblog-error.png

   ```bash
   hexo clean
   ```

2. Error: `prism_plugin` options should be added to \_config.yml file
   增加以下内容到\_config.yml
   ```yml
   prism_plugin:
   mode: 'preprocess' # realtime/preprocess
   theme: 'default'
   line_number: false # default false
   ```
