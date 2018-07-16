---
layout: post
title:  "博客写作指南"
date:   2018-07-15 13:53:12 +0800
categories: jekyll update
---

本博客基于[jekyll](https://jekyllrb.com/)，通过[Ruby](https://www.ruby-lang.org/en/)脚本根据模板生成静态网页，实现了内容与排版的分离。生成的静态网页通过[Github Pages](https://pages.github.com/)托管，域名默认为`${Github Username}.github.io`，可通过创建`CNAME`文件绑定自定义域名。

## 规范

### 命名

博客写作时，**必须**统一使用Markdown格式([快速入门](https://www.appinn.com/markdown/basic.html))，文件名称格式为`{yyyy-MM-dd}-{blog-title}.md`。其中，前半部分必须按格式指定年月日，后半部分的博客标题可以较为随意的填写。

### 元数据

博客内容中，**必须**在头部放置如下元数据：

~~~
---
layout: post
title:  "博客写作指南"
date:   2018-07-15 13:53:12 +0800
categories: jekyll update
---
~~~

元数据指定方式：

1. `layout`值固定为`post`
2. `title`为本篇博客的标题，会在列表页及内容详情页展示
3. `date`为本篇博客的完成日期，格式为`yyyy-MM-dd HH:mm:ss Z`(带时区)
4. `categories`值以空格分隔的方式指定多级目录，与生成后的静态URL相关，如`jekyll update`对应/jekyll/update/

### 内容区

指定完成后就可以开始书写博客内容了，推荐使用Markdown编辑器，可以帮助我们即时查看写作内容及格式是否正确，如果Markdown常用语法已经很熟也可以使用普通的文本编辑器。可选编辑器：

Windows: [MarkdownPad](http://markdownpad.com/) [Typora](https://www.typora.io/)

MacOS: [Typora](https://www.typora.io/)

### 目录结构

本博客采用了较为简单的Jekyll主题，目录结构也很简单，如下所示，只要知道将自己写的Markdown格式的博客文件放置于`_posts`目录下即可。

~~~
_posts   博客源文件(Markdown格式)
_layouts 布局格式，对应元数据中指定的layout项
_site    生成的静态文件(已被gitignore)
~~~

## 发布

只需要将自己新增的Markdown文件推送到Github仓库中，Github便会通过Jekyll及Ruby进行自动构建及发布。推送有两种方式：

1. 联系Github仓库Owner，申请成为仓库的Collaborators
2. Fork Github仓库，新增或修改后提交Pull Request，由仓库Owner审核后进行Merge

本博客仓库所在的Github地址为[https://github.com/xspurs/xspurs.github.io](https://github.com/xspurs/xspurs.github.io)。

## 本地Jekyll Server

搭建本地Jekyll Server可以帮助我们在提交到Github仓库前，通过在浏览器中输入`localhost`地址查看文章内容及格式是否正确，从而避免在一次博客的写作过程中多次操作Git进行提交。

### 搭建方式

Windows: [参考博客](https://blog.csdn.net/qiujuer/article/details/44620019)

MacOS:

~~~
$ brew install gem
$ gem install bundler jekyll
~~~

## 启动

Jekyll安装完成后，进入博客所在Git的本地父目录中，通过如下命令启动：

~~~
$ jekyll serve
~~~

Jekyll Server默认监听4000端口，在浏览器中访问[http://localhost:4000/](http://localhost:4000/)一睹为快吧~

## 最后

Happy blogging!
