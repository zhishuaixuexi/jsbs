---
title: Create Jekyll Blog
layout: post
categories: ''
tags: ''
---
## 环境配置
1. 安装包
Git 环境（用于部署到远端）、[Ruby 环境（Jekyll 是基于 Ruby 开发的）](http://www.ruby-lang.org/en/downloads/)、[包管理器 RubyGems](http://rubygems.org/pages/download)。
2. mac用户补充安装
如果你是 Mac 用户，你就需要安装 Xcode 和 Command-Line Tools了。下载方式 Preferences → Downloads → Components。
3. jekyll教程
Jekyll 是一个免费的简单静态网页生成工具，可以配合第三方服务例如： Disqus（评论）、多说(评论) 以及分享 等等扩展功能，Jekyll 可以直接部署在 Github（国外） 或 Coding（国内） 上，可以绑定自己的域名。[Jekyll中文文档](http://jekyll.bootcss.com/)、[Jekyll英文文档](https://jekyllrb.com/)、[Jekyll主题](http://jekyllthemes.org/)。
4. Jekyll 环境配置
安装 jekyll：gem install jekyll
5. 创建博客：jekyll new myBlog
6. 进入博客目录：cd myBlog
7. 启动本地服务：jekyll serve
8. 再浏览器输入：http://localhost:4000，就可以看到你的博客效果了。

## 目录结构
Jekyll 的核心其实是一个文本转换引擎。它的概念其实就是： 你用你最喜欢的标记语言来写文章，可以是 Markdown，也可以是 Textile,或者就是简单的 HTML, 然后 Jekyll 就会帮你套入一个或一系列的布局中。在整个过程中你可以设置URL路径, 你的文本在布局中的显示样式等等。这些都可以通过纯文本编辑来实现，最终生成的静态页面就是你的成品了。

一个基本的 Jekyll 网站的目录结构一般是像这样的：
├── _config.yml
├── _includes
|   ├── footer.html
|   └── header.html
├── _layouts
|   ├── default.html
|   ├── post.html
|   └── page.html
├── _posts
|   └── 2016-10-08-welcome-to-jekyll.markdown
├── _sass
|   ├── _base.scss
|   ├── _layout.scss
|   └── _syntax-highlighting.scss
├── about.md
├── css
|   └── main.scss
├── feed.xml
└── index.html
这些目录结构以及具体的作用可以参考 [官网文档](http://jekyll.com.cn/docs/structure/)

进入 _config.yml 里面，修改成你想看到的信息，重新 jekyll server ，刷新浏览器就可以看到你刚刚修改的信息了。

到此，博客初步搭建算是完成了，

bundle exec jekyll serve
提示：Could not find gem 'github-pages' in rubygems repository https://rubygems.org/ or installed locally.
The source does not contain any versions of 'github-pages
bundle install
 jekyll -v
 提示：您已经激活了 i18n 1.8.10，但是您的 Gemfile 需要 i18n 0.9.5。 在您的命令中添加 `bundle exec` 可以解决这个问题
 bundle exec jekyll -v
 提示：jekyll 3.9.0
 
 提示
 jekyll new JSBSJekyll
 cd E:/SW/JSBSJekyll
 bundle exec jekyll serve 
 提示：:in `require': cannot load such file -- webrick (LoadError)
 gem install webrick和gem list
 提示：显示里面有安装webrick 1.7
 bundle list
 提示：显示里面没有webrick 
 bundle add webrick
 bundle list
 提示：出现webrick 1.7
 bundle exec jekyll serve --trace
 提示：服务启动
 Configuration file: E:/SW/JSBSJekyll/_config.yml
            Source: E:/SW/JSBSJekyll
       Destination: E:/SW/JSBSJekyll/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
       Jekyll Feed: Generating feed for posts
                    done in 0.568 seconds.
 Auto-regeneration: enabled for 'E:/SW/JSBSJekyll'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
如果你想使用我的模板请把 _posts/ 目录下的文章都去掉。
修改 _config.yml 文件里面的内容为你自己的。