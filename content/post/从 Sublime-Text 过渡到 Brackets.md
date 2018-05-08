---
title: "从 Sublime Text 过渡到 Brackets"
comment: true
draft: false
date: 2018-05-08T10:43:12+08:00
lastmod: 2018-05-08T10:43:12+08:00
categories: ["学习笔记", "工具"]
tags: ["Brackets", "编辑器", "code editor"]
author: '<a href="https://github.com/kuleyu/" rel="noopener" target="_blank">kuleyu</a>'
weight: 10
---

自`3164版本`开始，轻巧美观的 **Sublime Text** 不注册就无法使用了，网络上所流出的激活码基本上也都已经被封殆尽。要想再使用它基本上也就只有两种方法了，付费与破解(*偷偷提示一下：其实用版本2的注册码来注册版本3依然有效，且版本2的激活码很多都没有被封，只不过顶部会提示“LICENSE UPGRADE REQUIRED”*)。不过就目前这趋势，倒不如早点投向 **Brackets** 、**VS Code** 或者 **Atom** 这几款免费的编辑器中去来的靠谱。

这三款软件都有接触过，总的来说都非常不错。但就我个人而言，**Brackets** 算是是用得比较舒服的。下面就来介绍介绍一下 **Brackets**。

<!-- more -->

## 安装及配置

Brackets 是 Adobe 旗下的一款代码编辑器，风格和其兄弟软件 Dreamweaver 有很多相似之处。不过 Brackets 是开源免费的，且提供多平台支持。  👉 [前往官方下载](http://brackets.io/)

### 切换软件语言

Brackets 本身提供多语言配置，`默认语言`为英文，你可以在 `Debug > Switch Language` 中切换到你需要的语言来显示。

### Brackets 扩展

Brackets 扩展的安装方法有两种：

  - 从软件的扩展管理器中直接搜索、安装。
  - 从[官网Brackets Extension Registry](https://registry.brackets.io/) 或者 Github 上搜索下载对应的 zip 压缩文件，然后直接拖到软件的扩展管理器中即可安装。
  
> 虽然官网上 Brackets 软件本身的下载源用的是`https://github.com/adobe/brackets/releases/`，但官网扩展以及软件扩展管理器中扩展的下载源都用的是`https://s3.amazonaws.com/extend.brackets/`。这个下载源在国内多数情况是被屏蔽状态，所以你可能需要翻-墙。  

> 不想或没办法翻-墙的话，你就只能在 Github 上搜索下载 zip格式 压缩包再安装。漫无目的地一个一个找可能比较麻烦，这个网站可以帮到你 👉 `http://ingo-richter.io/BracketsExtensionTweetBot/` 虽然已经久未更新了。  

下面是我的一些扩展：  
1. [VSCode Dark][01] 算是用过的最舒服的一个主题了。
- [Brackets Markdown Preview][02] 提供 `markdow` 文件实时预览功能。一栏编辑，一栏显示。
- [Beautify][03] 从排版格式上美化你的代码，使之易于阅读。
- [Indent Guides][04] 在每个标签的起始处与闭合处添加一条辅助线，辅助阅读。
- [Emmet][05] 快速编码神器。
- [Autoprefixer][06] 自动补全兼容前缀，让CSS适配不同浏览器。
- [W3C Validation (by Umoxfo)][07] 检测代码是否合乎 W3C 标准。
- [HTML5 Template][08] 再页面内插入 HTML5 模板（带有响应式相关标签）
- [Color Highlighter][09] 将 css 等样式文件中的色彩值以其自生色彩颜色为背景高亮显示。
- [Smart JSDoc Comment][10]
- [ColorKeeper][11] 在界面底部自定义一个色板，方便快捷取得预定义色彩。
- [Display Shortcuts][12] 提供了一个快捷键对应表以供显示。
- [bracket-color-finder][13]
- [AEM Brackets Extension][14] 详细说明见[AEM Brackets Extension
](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/aem-brackets.html?wcmmode=disabled)
- [Brackets Outline List][15] 在侧边栏显示节点树，可快速定位到某行对应的代码。
- [Brackets Vue][16]
- [BracketstoIX][17]
- [Brackets SASS][21]

![](http://opifddwc7.bkt.clouddn.com/18-5-8/77661856.jpg)

### 快捷键配置

> 👉 官方 WIKI - [User Key Bindings][18]

参考以上 Wiki 中的配置说明，你可以轻松的将你的 Brackets 快捷键配置成 Sublime Text 的使用风格。

同时，上文中的 `Display Shortcuts` 扩展 提供了显示快捷键表格的功能，通过 `help > Show Shortcuts` 可以调出快捷键表格。

## 特色内置功能

### 快速编辑(Quick Edit)功能

![](http://opifddwc7.bkt.clouddn.com/18-5-8/74884389.jpg)

快速编辑<kbd>Ctrl+E</kbd>相当于一个功能集合，主要包括四个方面的功能： **取色器**、**HTML**、**JavaScript**、**CSS(CSS/LESS/SCSS)**

  - **取色器**  
  取色器对任意类型文件*(只要该文件中存在任意格式的颜色值[包括：hex / rgb / rgba / hsl / hsla];如若没有，你可以先随便写入一个)*都有效。  
  只需将光标移入颜色值上，然后按下 快捷键 <kbd>Ctrl+E</kbd> 即可调取任意颜色。  
  
  
  - **HTML**  
  可针对 HTML 文件中的 `标签名`、`id属性`、`class属性` 来调出某个元素标签与`这三种选择符`对应的 **css样式**。  
  只需将光标移入以上三者任一之上，然后按下 快捷键 <kbd>Ctrl+E</kbd> 即可编辑操作。
  
  > 如果某个元素标签匹配多种选择符，其所有样式规则都会以对应的组合选择符在右侧列出。  
  > 如果还没有样式，单击`新建规则(New Rule)`按钮或者<kbd>Ctrl+Alt+N</kbd>可以创建新的样式。  
  
  
  - **JS**  
  可以针对 JS 文件中的`函数名称`调出该`函数主体`（即使它是在其他js文件中创建的也可以）。
  
  
  - **CSS(CSS / LESS / SCSS)**  
  可以针对`样式文件`中的`过度时间函数`[cubic-bezier()][19]或[steps()][20]，调出其**转换曲线的图形化编辑器**。
  预先定义的时间函数 ease，ease-in，ease-out，ease-in-out，step-start，和 step-end 也是有效的作用点。  
  

### 快速文档(Quick Docs)

![](http://opifddwc7.bkt.clouddn.com/18-5-8/10491422.jpg)

快速文档<kbd>Ctrl+K</kbd>功能就相当于一个 HTML 与 CSS(CSS/LESS/SCSS) 的知识文档储备库。

当你对某个 标签元素 或 属性/属性值 不熟悉的时候，只需将光标移至其上，然后按下快捷键 <kbd>Ctrl+K</kbd>，即可在该行代码下面显示出相关文档的相关知识点。

### 实时预览

对于实时预览功能而言，普通使用基本无需配置。如果想要在 `SASS / LESS` 样式环境下依然有效，则需要以下扩展来完成。 相应的，你需要按装 [Brackets SASS][21] 或者 [LESS AutoCompile][22]。

## 其他

### 关于 JSLint 与 ESLint

![](http://opifddwc7.bkt.clouddn.com/18-5-8/9528370.jpg)

Brackets 自带 JSLint 与 ESLint 扩展，作为 js 与 es6 的代码质量检测工具。

在 JSLint 中将 console 和 alert、prompt、confirm 视为 development 方法，需要我们打开 development 模式才允许使用，打开方式是使用规则：devel:true；否则会有错误提示。

> 同类型的检测工具还有 JSHint 与 ESHint, 与前两者的区别请参考 👉 [JSHint 与 JSLint 的区别与选择](https://blog.csdn.net/devil2119971/article/details/52191323)


## 参考

1. [How to Use Brackets](https://github.com/adobe/brackets/wiki/How-to-Use-Brackets)
2. [css动画里的steps()用法详解][19]
3. [CSS3 三次贝塞尔曲线(cubic-bezier)][20]

[01]: https://s3.amazonaws.com/extend.brackets/vscode-dark/vscode-dark-0.9.1.zip
[02]: https://s3.amazonaws.com/extend.brackets/brackets-markdown-preview/brackets-markdown-preview-2.2.0.zip
[03]: https://s3.amazonaws.com/extend.brackets/brackets-beautify/brackets-beautify-2.5.1.zip
[04]: https://s3.amazonaws.com/extend.brackets/brackets-indent-guides/brackets-indent-guides-1.3.11.zip
[05]: https://s3.amazonaws.com/extend.brackets/brackets-emmet/brackets-emmet-1.2.2.zip
[06]: https://s3.amazonaws.com/extend.brackets/mikaeljorhult.brackets-autoprefixer/mikaeljorhult.brackets-autoprefixer-0.7.5.zip
[07]: https://s3.amazonaws.com/extend.brackets/umoxfo.w3cvalidation/umoxfo.w3cvalidation-1.1.0.zip
[08]: https://s3.amazonaws.com/extend.brackets/tanishbaansal.html5template/tanishbaansal.html5template-1.0.0.zip
[09]: https://s3.amazonaws.com/extend.brackets/qw0101.colorhighlighter/qw0101.colorhighlighter-1.2.2.zip
[10]: https://s3.amazonaws.com/extend.brackets/jsdoc.smartcomment/jsdoc.smartcomment-0.0.4.zip
[11]: https://s3.amazonaws.com/extend.brackets/dez.color.keeper/dez.color.keeper-1.0.1.zip
[12]: https://github.com/redmunds/brackets-display-shortcuts
[13]: https://s3.amazonaws.com/extend.brackets/bracket-color-finder/bracket-color-finder-1.0.0.zip
[14]: https://s3.amazonaws.com/extend.brackets/aem-sightly-brackets-extension/aem-sightly-brackets-extension-0.0.14.zip
[15]: https://s3.amazonaws.com/extend.brackets/hirse.outline-list/hirse.outline-list-1.4.1.zip
[16]: https://s3.amazonaws.com/extend.brackets/brackets.vue/brackets.vue-0.1.0.zip
[17]: https://s3.amazonaws.com/extend.brackets/bracketstoix/bracketstoix-3.4.0.zip
[18]: https://github.com/adobe/brackets/wiki/User-Key-Bindings
[19]: https://segmentfault.com/a/1190000007042048
[20]: https://blog.csdn.net/zhaozjc112/article/details/52909172
[21]: https://github.com/jasonsanjose/brackets-sass
[22]: https://github.com/jdiehl/brackets-less-autocompile