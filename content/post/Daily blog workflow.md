---
title: "Workflows for DAILY blog"
date: 2024-12-01T12:31:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["Blog"]
categories: ['Blog']

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
    image: "https://raw.githubusercontent.com/mhqqysh3/mhqqysh3.github.io/refs/heads/main/data/Daily%20blog%20workflow/avator.jpg" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/<path_to_repo>/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

# 全流程

---

## Step1 本地下载
```
cd D:\YSH\My_BLOG1\2
hugo new site quickstart --format yaml
cd quickstart
git init
//有.git
git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
//有.gitmoduls
//然后粘贴到已经clone了github的文件夹
cd D:\YSH\My_BLOG1\mhqqysh3.github.io
```


修改hugo.yaml，链接theme
- 修改line1为你自己的github网站名字.github.io
- 其他行照着下面复制就行，我的文如下
```
baseURL: "https://mhqqysh3.github.io/"
title: ExampleSite
paginate: 5
theme: PaperMod

enableRobotsTXT: true
buildDrafts: false
buildFuture: false
buildExpired: false

minify:
  disableXML: true
  minifyOutput: true

params:
  env: production # to enable google analytics, opengraph, twitter-cards and schema.
  title: ExampleSite
  description: "ExampleSite description"
  keywords: [Blog, Portfolio, PaperMod]
  author: Me
  # author: ["Me", "You"] # multiple authors
  images: ["<link or path of image for opengraph, twitter-cards>"]
  DateFormat: "January 2, 2006"
  defaultTheme: auto # dark, light
  disableThemeToggle: false

  ShowReadingTime: true
  ShowShareButtons: true
  ShowPostNavLinks: true
  ShowBreadCrumbs: true
  ShowCodeCopyButtons: false
  ShowWordCount: true
  ShowRssButtonInSectionTermList: true
  UseHugoToc: true
  disableSpecial1stPost: false
  disableScrollToTop: false
  comments: false
  hidemeta: false
  hideSummary: false
  showtoc: false
  tocopen: false

  assets:
    # disableHLJS: true # to disable highlight.js
    # disableFingerprinting: true
    favicon: "<link / abs url>"
    favicon16x16: "<link / abs url>"
    favicon32x32: "<link / abs url>"
    apple_touch_icon: "<link / abs url>"
    safari_pinned_tab: "<link / abs url>"

  label:
    text: "Home"
    icon: /apple-touch-icon.png
    iconHeight: 35

  # profile-mode
  profileMode:
    enabled: false # needs to be explicitly set
    title: ExampleSite
    subtitle: "This is subtitle"
    imageUrl: "<img location>"
    imageWidth: 120
    imageHeight: 120
    imageTitle: my image
    buttons:
      - name: Posts
        url: posts
      - name: Tags
        url: tags

  # home-info mode
  homeInfoParams:
    Title: "Hi there \U0001F44B"
    Content: Welcome to my blog

  socialIcons:
    - name: x
      url: "https://x.com/"
    - name: stackoverflow
      url: "https://stackoverflow.com"
    - name: github
      url: "https://github.com/"

  analytics:
    google:
      SiteVerificationTag: "XYZabc"
    bing:
      SiteVerificationTag: "XYZabc"
    yandex:
      SiteVerificationTag: "XYZabc"

  cover:
    hidden: true # hide everywhere but not in structured data
    hiddenInList: true # hide on list pages and home
    hiddenInSingle: true # hide on single page

  editPost:
    URL: "https://github.com/<path_to_repo>/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link

  # for search
  # https://fusejs.io/api/options.html
  fuseOpts:
    isCaseSensitive: false
    shouldSort: true
    location: 0
    distance: 1000
    threshold: 0.4
    minMatchCharLength: 0
    limit: 10 # refer: https://www.fusejs.io/api/methods.html#search
    keys: ["title", "permalink", "summary", "content"]
menu:
  main:
    - identifier: categories
      name: categories
      url: /categories/
      weight: 10
    - identifier: tags
      name: tags
      url: /tags/
      weight: 20
    - identifier: example
      name: example.org
      url: https://example.org
      weight: 30
# Read: https://github.com/adityatelange/hugo-PaperMod/wiki/FAQs#using-hugos-syntax-highlighter-chroma
pygmentsUseClasses: true
markup:
  highlight:
    noClasses: false
    # anchorLineNos: true
    # codeFences: true
    # guessSyntax: true
    # lineNos: true
    # style: monokai
```

```
hugo server现在是可以看的localhost
```
![[Pasted image 20241202010753.png|300]]



## Step2 配置一键生成文章

- 设置一个template,创建archetypes/post.md内容复制下面就行
```
---
title: "My 1st post"
date: 2020-09-15T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["first"]
author: "Me"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Desc Text."
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
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
```
- 运行命令如下，可以创建一个名字为1.md，模板为post.md的文件
```
hugo new --kind post post/1.md
```

- 同样的道理，如果你需要第二个模板，首现在archetypes/post2.md贴入内容
```
---
title: "My 2st post"
date: 2020-09-15T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["first"]
author: "Me"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Desc Text."
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
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
```
- 然后运行如下命令，就会有遵循第二个模板的文件生成
```
hugo new --kind post2 post/2.md
```
- 看看效果（补充一下，如果用两个命令行窗口，一个用来执行命令，一个待机着hugo server可以无延迟看变化）
```
hugo server现在是可以看的localhost
```


## Step3 有关基本配置
打开hugo.yaml
比较好调整的主要是以下几个
- line75 首页标题 
- line79 wechat可以引用一张你的wechat号
- [其他待补充，包括toc]



## Step4 上传github

- gitkraken ssh 连接github（我不知道为什么，但是我直接设置ssh就是连接不上，但是gitkraken就可以连接上，当然每次输入设置git config也可以，但是图形化git还是要舒服一点）
- git kraken clone下来自己的 用户名.github.io 仓库，应该只有一个git
- 然后复制除了git的刚刚文件夹的文件到其中，然后分别做下面的两个事情、
	gitkraken stage->descrip->commit->push
	以后你上传的时候其实就是用这几个命令
- 然后打开你的github可以看到已经传上去了，但是网站build失败，这是因为你只提供了源文件，hugo网站的编译需要自己的一些环境配置，而这些是没有的
- 所以下一步你需要让github在build的时候先下载hugo然后各种步骤，这些已经被写成了脚本，你只需要新建一个.github/workflows/hugo.yaml,里面填充下面的内容，无需更改
```
name: Deploy Hugo site to Pages

on:
  # Runs on pushes targeting the default branch
  push:
    branches:
      - main
  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

permissions:
  contents: read
  pages: write
  id-token: write

# Allow only one concurrent deployment, skipping runs queued between the run in-progress and latest queued.
# However, do NOT cancel in-progress runs as we want to allow these production deployments to complete.
concurrency:
  group: "pages"
  cancel-in-progress: false

# Default to bash
defaults:
  run:
    shell: bash

jobs:
  # Build job
  build:
    runs-on: ubuntu-latest
    env:
      HUGO_VERSION: 0.137.1
    steps:
      - name: Install Hugo CLI
        run: |
          wget -O ${{ runner.temp }}/hugo.deb https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_extended_${HUGO_VERSION}_linux-amd64.deb \
          && sudo dpkg -i ${{ runner.temp }}/hugo.deb          

      - name: Install Dart Sass
        run: sudo snap install dart-sass

      - name: Checkout
        uses: actions/checkout@v4
        with:
          submodules: recursive
          fetch-depth: 0

      - name: Setup Pages
        id: pages
        uses: actions/configure-pages@v5

      - name: Install Node.js dependencies
        run: "[[ -f package-lock.json || -f npm-shrinkwrap.json ]] && npm ci || true"

      - name: Build with Hugo
        env:
          HUGO_CACHEDIR: ${{ runner.temp }}/hugo_cache
          HUGO_ENVIRONMENT: production
          TZ: America/Los_Angeles
        run: |
          hugo \
            --gc \
            --minify \
            --baseURL "${{ steps.pages.outputs.base_url }}/"          

      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: ./public

  # Deployment job
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4

```

- 然后重复上面的gitkraken的步骤
- 进入github这个repo/settings/Pages Source下面选择Github Actions 别的不用管，然后看Code红应该有一个正在旋转的红圈，等其变为绿色就可以使用了

## Step4 快速写文章Workflow

- 命令行运行
```
cd D:\YSH\My_BLOG1\WebsiteUpdate
code . //打开vscode修改
```
- gitkraken打开websiteupdate
- 需要的obsidian的md文章打开
- 命令行
```
hugo new --kind post post/Daily Blog .md
```
- （+各种更改）vscode中复制自己的obsidian文章进去,改标题，tags
- gitkraken view change->stage all change->descrip->commit->push
- 等github转圈转完 大约1min 不要着急 确实没法做到几秒直接搞定，但是whatever已经可以了







## 遇到的bug
- 因为我想转自己的网站，但是一开始mhqqysh3.github.io还没渲染完就链接了mhqqysh.cn然后导致每次都是出错。然后后来删掉dns链接还是一点mhqqysh3.github.io就是出错，并且导向mhqqysh,cn.后来我切换大号mhqqysh.github.io链接了mhqqysh.cn然后两个网址都可以访问大号的网站，但是mhqqysh3.github.io还是立刻重定向到mhqqysh.cn。后来gpt之后知道了是【浏览器缓存问题，需要用inprivate即可，或者清楚浏览记录】
- 或者链接不到的原因可能是阿里云dns还没有传播到，需要多开开几次
- 还有一个事情，就是即使github上说没有连接成功，但是可能你输入mhqqysh.cn的时候已经显示的是mhqqysh3.github.io的内容了

