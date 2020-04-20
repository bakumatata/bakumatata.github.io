---
title: new day
date: 2020-04-20 11:42:19
categories:
- [Tech, Manual]
tags:
- intro
- code
---

## 搭建顺序

1. clone项目
2. 安装hexo(如已安装，跳到第3步)
   1. `git bash here`
      1. mac: 取得root权限 `sudo -i`
      2. 全局安装`npm install -g hexo-cli`
   2. 在文件夹下 `npm install hexo-cli -g`
   3. `npm install hexo --save`
   4. 检查是否成功 `hexo -version`
3. 写新文章 `hexo new [layout] <title>`
   1. 如果没有自定义layout，用`hexo new "title"`
4. 生成 `hexo generate` 或简写为 `hexo g`
5. 本地预览`hexo server`  或简写为`hexo s`，正常会使用`http://localhost:4000/`预览（如果没及时关闭客户端会报错，报错的话试以下命令
   1. clean cache `hexo clean`
   2. generate again `hexo g`
   3. `hexo server` again
6. 把根目录`public`里的文件全部剪切到根目录覆盖
7. git push
8. ~~部署 `hexo deploy` 简写为`hexo d`(不使用，使用git push就行)~~

## 压缩图片

```yaml
npm i hexo-all-minifier --save

# Mac 系统还需要额外安装
brew install libtool automake autoconf nasm

# 在博客配置中加入
all_minifier: true
```



## Hexo主题的优劣势

### 优势

- 集成性高，主题很漂亮，需要自定义修改的部分少

### 劣势

- 需要安装node.js环境
- 每次更新需要本地生成再发布，步骤繁琐
- 不能在移动端上随写随发布
- 同一个git账号只能有一个一级域名xxx.github.io，在同一个机器上切换不同git账户时，操作非常非常繁琐

## 参考

- 使用主题 [Fluid]([https://hexo.fluid-dev.com/docs/guide/#%E5%BF%85%E8%A6%81%E7%9A%84%E9%85%8D%E7%BD%AE](https://hexo.fluid-dev.com/docs/guide/#必要的配置))
- [hexo基本配置](https://hexo.io/zh-cn/docs/commands)