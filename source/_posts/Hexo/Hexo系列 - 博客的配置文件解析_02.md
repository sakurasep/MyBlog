---
title: Hexo_02-博客的配置文件解析
author: 上杉九月
date: 2022-04-11 19:20:50
updated: 2022-06-25 17:07:41
## 基本设置
tags: 
- Hexo
- 零基础
categories: Hexo系列
excerpt: 本篇文章讲述了`_config.yml`的内容配置
## 密码设置
password: 
abstract: 
wrong_pass_message: 密码错误,请重新输入
## 置顶设置
sticky: 10000
top: false
pin: false
## 文章头图设置
index_img: https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/5199/Hexo/index_2.jpg
banner_img: https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/5199/Hexo/index_2.jpg
headimg: https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/5199/Hexo/index_2.jpg
img: https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/5199/Hexo/index_2.jpg
cover: https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/5199/Hexo/index_2.jpg
## 相关开关
mermaid: false
mathjax: false
math: false
comments: true
hide: false
abbrlink: hexo02
## Aplayer播放器设置
music:
  server: netease
  type: song
  id: 1403774122
## 博客引用了哪些文章
references:
  - title: '个人博客搭建笔记-hexo根目录下的`_config.yml`配置解释-前端小黑的博客-CSDN博客'
    url: 'https://blog.csdn.net/zemprogram/article/details/104288872'
---

{% noteblock info::config文件介绍 %}
此文件是对于Hexo最基本的修改，在使用主题后，由于主题作者设计的不同，某些设置将不会生效，你只需要填写必要设置，并且按照主题作者的文档进行修改即可。
{% endnoteblock %}
## Site

{% folding green, Site部分 %}
```yaml
# 网站标题(必填)
title: 九月的生活 
# 副标题(在某些主题不生效)
subtitle: New Dream New Start 
# 网站描述(建议填写，优化SEO)
description: 希望在这里分享我的经验与生活！ 
# 网站的关键字(选填，优化SEO)
keywords: 
# 网站作者(必填)
author: 上杉九月 
# 网站使用的语言(取决于你主题目录下的语言文件)
language:
- zh-CN
- en
- zh-TW 
# 网站对应的时区(无需设置)
timezone: '' 
```
{% endfolding %}

## Url
{% folding green, Url部分 %}
```yaml
## url这里有个主题分站的玩法，后期会讲到
# 网站网址，如果设置了自定义域名，这里改为自定义的域名(必填)
# Github: https://Github用户名.github.io
# Gitee: https://Gitee仓库路径名.gitee.io
url: https://sakurasep.gitee.io 
# 文章的永久链接格式(选择性修改)
permalink: :year/:title/  
# (无需修改)
permalink_defaults:
pretty_urls:
  trailing_index: true 
  trailing_html: true 
```
{% endfolding %}

## Directory
{% folding green, Directory部分 %}
```yaml
# 以下内容保持默认即可
source_dir: source
public_dir: public
tag_dir: tags
archive_dir: archives
category_dir: categories
code_dir: downloads/code
i18n_dir: :lang
# 跳过指定文件的渲染，这里在后期做分站时需要跳过分站的目录，防止二次渲染
skip_render:
```
{% endfolding %}

## Writing
{% folding green, Writing部分 %}
```yaml
# 新建文章的默认名称(无需修改)
new_post_name: :title.md 
# 预设布局，hexo new命令可以创建post,draft,page三种页面，这里的值为post，hexo new "文章名“ 默认生成的是post
default_layout: post
# 将标题转换为首字母大写(无需修改)
# 影响的是title属性，后续可以通过安装插件实现该功能，所以此处的设置在某些主题不生效
titlecase: false
# 是否在新标签页中打开链接(按需修改)
external_link:
  enable: true 
  # 仅仅对post类型的文章生效
  field: site 
  # 排除的域名
  exclude: ''
# 文件名称转换 0是不转换 1小写 2大写(无需修改)
filename_case: 0
# 是否渲染草稿文件(无需修改)
render_drafts: false
# 是否启用资源文件夹(按需修改)
# 开启此选项后在hexo new文章时，会创建一个同名文件夹，用于保存你文章中所需资源。不过我建议使用网络图床。
post_asset_folder: false
# 相对链接(无需修改)
relative_link: false
# 是否显示未来的文章(按需修改)
# 如果你文章的时间设置的未来的时间，打开这个即可显示
# 这个可以用于定时发布某些文章，建议关闭
future: false
# 代码块高亮设置(根据所用主题按需设置)
highlight:
  enable: true
  line_number: true
  auto_detect: false
  tab_replace: ''
  wrap: true
  hljs: false
prismjs:
  enable: false
  preprocess: true
  line_number: true
  tab_replace: ''
```
{% endfolding %}

## Home page setting
{% folding green, Home page setting部分 %}
```yaml
index_generator:
  path: ''
  # 每页显示的文章数量(按需修改)
  per_page: 7
  # 文章排序方式，默认最新日期在最前面(无需修改)
  order_by: -date
```
{% endfolding %}

## Category & Tag
{% folding green, Category & Tag部分 %}
```yaml
# 以下内容不建议修改
# 默认分类
default_category: uncategorized
# 分类别名
category_map:
# 标签别名
tag_map:
```
{% endfolding %}

## Metadata elements
{% folding green, Metadata elements部分 %}
```yaml
# 元数据元素(无需修改)
meta_generator: true
```
{% endfolding %}

## Date / Time format
{% folding green, Date / Time format部分 %}
```yaml
# 时间/日期格式(无需修改)
date_format: YYYY-MM-DD
time_format: HH:mm:ss
# 文章更新时间格式(按需修改)
# 提供了三个选项 
# mtime: 将文章修改时间作为文章更新时间
# date: 将文章创建时间作为文章更新时间
# empty: 没有文章更新时间
updated_option: 'mtime'
```
{% endfolding %}

## Pagination
{% folding green, Pagination部分 %}
```yaml
# 分页时每页文章数量 设置为0 不分页(按需修改)
per_page: 7
pagination_dir: page
```
{% endfolding %}

## Include / Exclude file(s)
{% folding green, Include / Exclude file(s)部分 %}
```yaml
# 包括/不包括的文件(无需修改)
include:
exclude:
ignore:
```
{% endfolding %}

## Extensions
{% folding green, Extensions部分 %}
```yaml
# 主题
# 使用的主题名
theme: volantis
```
{% endfolding %}

## Deployment
{% folding green, Deployment部分 %}
```yaml
# 部署设置
deploy:
  type: git
  # 仓库地址
  repo: https://gitee.com/sakurasep/sakurasep.git
  # 仓库分支
  branch: master
```
{% endfolding %}

---

{% gallery %}
![关于我](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/5199/about_me.png)
{% endgallery %}
