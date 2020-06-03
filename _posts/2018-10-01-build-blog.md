---
layout: default
title: 如何创建在github上建blog
---

## {{ page.title }}

0. 安装git，申请[github账户](https://github.io)

1. 创建项目
  在本地建一个目录，作为项目主目录，如：xxx.github.io (xxx是你的github账户名)

  ```
  mkdir xxx.github.io
  ```

  对该目录进行git初始化

  ```
  cd xxx.github.io
  git init
  ```

  创建一个没有父节点的分支gh-pages。因为github规定，只有该分支中的页面，才会生成网页文件。

  ```
  git checkout --orphan gh-pages
  ```

2. 创建设置文件

   ```
   vim _config.yml

   #文件内容
   baseurl: /xxx.github.io
   ```

3. 创建模板文件

   ```
   mkdir _layouts
   ```
4. 创建文章

   ```
   mkdir _posts
   ```
5. 创建首页


6. 发布内容

  提交内容到本地仓库

  ```
  git add .
  git commit -m "first post"
  ```

  前往github网站，登录后创建名为xxx.github.io的库，然后将本地仓库内容推送到github上刚刚创建的库。

  ```
  git remote add origin https://github.com/xxx/xxx.github.io.gitgit push origin gh-pages
  ```

7. 编辑内容

  新增或修改文章后，将修改内容提交到github即可。

  ```
  git add .
  git commit -m "message"
  git push
  ```



参考：
[搭建一个免费的，无限流量的Blog----github Pages和Jekyll入门](http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html)
[写作环境搭建(git+github+markdown+jekyll)](https://site.douban.com/196781/widget/notes/12161495/note/264946576/)