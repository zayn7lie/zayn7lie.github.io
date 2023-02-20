---
title: 从0开始的博客网站搭建
date: 2023-2-20 # HH:MM:SS +/-TTTT
categories: [Misc]
tags: [blog, building, jekyll, chirpy, github]     # lowercase
---
基于GitHub Page和jekyll的chirpy主题

# 基本网站的搭建
- 创建GitHub账号并登录
- 模板库的复制
  -  [点我](https://github.com/cotes2020/chirpy-starter/generate) 复制（folk）chirpy主题的模板库
  -  `Repository name` 一栏输入 `用户名.github.io` ，例如我的是 `zayn7lie.github.io`
  -  点击 `Create repository from template` 生成网站后端库
- 模板库的配置
  -  进入库，找到 `_config.yml` 并打开
  -  在代码栏的右上角点击笔的图案，进入编辑模式
  -  修改 `title: ` 后的内容，为你的博客取个名字
  -  拉到最下方，点击 `Commit changes`
- 模板库的初始化
  -  提交完成后，在上方点击 `Setting` -> 左方 `Code and automation` -> `pages` -> 右方 `Build and deployment` -> `Source` 从 `Deploy from a branch` 换成 `GitHub Actions`
  -  过一会后打开 `用户名.github.io` 你的博客界面就创建完毕啦
-  更多的设置可以自己在后端调配，本篇教程也会列出一些我自己遇到的问题和解决方案
-  有关chirpy主题的教程可以在 [这里](https://chirpy.cotes.page/) 查看

