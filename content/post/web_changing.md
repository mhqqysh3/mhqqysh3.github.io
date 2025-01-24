---
title: "Web Changing"
date: 2024-12-03T11:32:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["网站"]


author: "Me"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: true
draft: false
hidemeta: false
comments: false
description: "Desc Text."
canonicalURL: "https://canonical.url/to/page"
disableShare: true
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/<path_to_repo>/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

## Waiting to do


## Done
### pic 

我把所有的相关poster，img都放在data下面，这样自然调用就行

### archive🐕

Archive 即博客中的归档、时间线功能，用于按照时间对博文分类管理。  
在 `<your_web_site>/content/` 目录下新建 `archive.md`，并添加以下模板内容：

```yaml
---
title: "Archive"
layout: "archives"
# url: "/archives"
summary: "archives"
---

```
修改网站配置文件，添加一个归档的菜单，即可通过点击菜单栏上归档按钮进入时间线

```yaml
menu:
  main:
    - name: 📦归档
      url: /archive
      weight: 3 # 自定义权重，菜单按照权重从小到大的顺序排列
defaultContentLanguage: zh  # 修改默认语言为中文，在归档界面展示中文
```
搜索

### Catogories🐕

把下面的句子放在每一个文件中
```yaml
categories: ['Blog']
```


- 其实现在已经可以了，然后就是下一层再按一下跳到那一层。

### font 🐕

这个就是可以保证随时更新 不需要新的hugo server
但是如果新的有问题的话，不会变成新的。

可能需要稍微等一会，加载字体


参考这个
[在 PaperMod 博客中设置自定义字体 | Aimer's Blog](https://aimerneige.com/zh/post/others/set-custom-fonts-on-papermod-site/)

最终文件结构如下图片
![[data/web_changing/Pasted image 20241202050413.png]]
### code blank修改代码块样式🐕


其实关键是前面需要写类型

其实已经可以了，虽然效果不是特别好，但是可以发现已经有了

最后就是看这个的后面
[FAQs / How To's Guide | PaperMod](https://adityatelange.github.io/hugo-PaperMod/posts/papermod/papermod-faq/#using-hugos-syntax-highlighter-chroma)




### 时间🐕
- 就是md的属性 data必须遵循格式

# 注意 各种css变化只有hugo sever重启的时候才能加载出来

