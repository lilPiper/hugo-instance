---
title: "初识 Hugo & 搭建一个自己的博客"
description: "My Path to Learn Hugo and how do I Build a Blog"
keywords: "Hugo,Vercel,Blog"

date: 2022-11-07T19:20:00+08:00
lastmod: 2022-11-08T09:20:00+08:00

categories:
 - SliceOfLife
tags:
  - Hugo
  - Vercel
  - Blog

url: post/my-path-to-learn-hugo.html
---

本文记录了初次接触 [Hugo](https://gohugo.io/) 以及用 [Hugo](https://gohugo.io/) / [Hugo theme NexT](https://github.com/hugo-next/hugo-theme-next) 搭建博客的过程。
<!--more-->

看技术文章看久了，手痒想搭建一个博客，写点什么，供以后的自己参考。

有句话说得好：“靠山山会倒。”近年来几大中文博客服务陆续关停正说明 `self-hosted` 的重要性。

在我看来，博客属于 C/S 架构网站，而 C/S 网站想要运行，离不开服务器、网站管理程序、域名。下面围绕这几点说明这次搭建的过程。
## 服务器
这几年 PaaS 风头正猛，不像博客空间、轻博客服务之流，悄无声息地倒下。年初到现在汇率变动了不少，叠加全球通货膨胀，相当于 USD 结算的东西都大幅涨价。由于目前的博客处于试运行状态，不需要高自由度定制和大量存储空间，我舍不得下血本买 VPS。所以转向使用 PaaS 的 dev 套餐试试水。

注册 Vercel 时遇到了一些波折。现在 telephone number 的填写似乎是必须的，不过总归比绑信用卡来得简单点。 

## 网站管理程序

像 SSM/SpringBoot 这些技术，不适合如此少访问量的博客。

要是真的只用 HTML/CSS 从头写起，恐怕违背了“尽量不要重复造轮子”的原则。而且偷懒的效果也容易像手机浏览器上的 WAP 网站。

WordPress 功能太多，漏洞不少。

于是，收集了一下，最近流行的有：
* Hexo
* Hugo
* Gastby
* Jekyll
* VuePress

根据现有的知识储备来说，刨掉 Node.js/PHP/Ruby/Vue ，就是 Hugo。Hugo 在自己的最短技术学习路径上。虽然 Golang 接触的也比较少。

### Windows 系统怎么下载安装 the extended version of Hugo
1. 到 [release 页面](https://github.com/gohugoio/hugo/releases) 下载 Windows 版本的 extended version of Hugo
2. 解压到自己想要的位置，记下 Hugo 所在位置，在该位置新建一个 `Sites` 目录
3. 配环境变量，将 **"Hugo所在位置\bin"** 添加到系统环境变量
4. 打开"命令提示符"，输入 `hugo version` 检查是否安装成功

选主题的时候，跑到常去的博客看了下页尾，主题是 NexT。用搜索搜到了 [Hugo theme NexT](https://github.com/hugo-next/hugo-theme-next)。开发者还贴心地给小白写了一键部署的说明，于是决定选这个主题。
### Hugo 一键部署到 PaaS
有了 Vercel 账号之后，可以直接照着 [Hugo theme NexT Starter](https://github.com/hugo-next/hugo-theme-next-starter) 里的说明，GitHub 授权 Vercel， 再一键部署 Hugo NexT theme 到 Vercel。

Ta-Da! 崭新的博客就出现了！由于 Vercel 自动分配一个二级域名，所以等于已经上线试运行了！
## 域名

域名先用 Vercel 的就好。手头上买的域名暂时还没有申请 HTTPS 证书。等申请完 HTTPS 证书再改域名商那边的 DNS 。
