# idea-helper
此仓库基于 [Jekyll][1] 构建的 [IntelliJ IDEA][2] 帮助文档翻译库，是为了让初学者更好地掌握 [IntelliJ IDEA][2] 这个开发神器。

[![Release](https://img.shields.io/github/release/mrzhqiang/idea-helper.svg)](https://github.com/mrzhqiang/idea-helper/releases/latest)
[![Build Status](https://travis-ci.org/mrzhqiang/idea-helper.svg?branch=master)](https://travis-ci.org/mrzhqiang/idea-helper)

## 主题
当前使用：[just-the-docs][3]，因为它简洁、易用，对初次使用 [Jekyll][1] 非常友好。

## 在线查看
请访问：[idea-helper]。

### 本地预览？
- 安装[开发环境][4]
- 安装 [Jekyll][1]
```bash
$ sudo gem install jekyll bundler
```
- 安装主题
```bash
$ sudo gem install just-the-docs
```
- 开启本地预览
```bash
$ bundle exec jekyll serve
```
- 打开浏览器并访问 [http://localhost:4000](http://localhost:4000)

**注意：如果本地预览无效，请打开 `_config.yml` 第 28 行的注释，再开启本地预览。**

### 声明
**此仓库仅用于学习交流使用，不得用于任何商业目的。**

[idea-helper]:https://mrzhqiang.github.io/idea-helper

[1]:https://jekyllrb.com/
[2]:https://www.jetbrains.com/idea/?fromMenu
[3]:https://pmarsceill.github.io/just-the-docs/
[4]:https://jekyllrb.com/docs/installation/