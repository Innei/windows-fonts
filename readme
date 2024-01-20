# Windows 11 全局替换微软雅黑到苹方

最近，某宝入手了一台 MATX 整机。然后装上了 Windows 11 系统。我自从高三之后就没这么用过 Windows 了，过了这么多年 Windows 的垃圾字体居然还没换。丑一批的雅黑和系统的字体渲染真的是一言难尽。即便是 4K 屏开 150% 缩放也就不回来字体太丑的问题。我决定把雅黑换成苹方。

关于如何提取苹方字体，请移步：[新版 macOS 苹方字体的提取移植与下载](https://blog.dsrkafuu.net/post/2020/extract-sf-pingfang/)

## 前置工具

首先下载大佬已经提取好的苹方字体，一般来说，macOS 中内置的苹方是加密，并不能直接在 Windows 上使用，这里直接用做好的字体就行。

然后需要 TTC 字体工具，用来提取雅黑的字体信息，和修改苹方字体的信息，最后重新合并为一个 TTC。

这里用到的工具：

- ttfname3+
- UniteTTC
- 字体替换工具

我把这些工具~~和成品雅黑苹方字体~~放下面分享链接了。

你可以略过教程，直接到字体替换章节。

不好意思，阿里云盘不让分享字体，自己动手丰衣足食。工具都在这了。

https://www.alipan.com/s/UmanLDu262z

::: warning
开始之前，请一定要备份原本的字体。
:::

## 过程

这里以替换微软雅黑为例，但事实上你还需要操作微软雅黑 Light 和雅黑 Bold。但是过程是一样的这里就不多展开，重复操作就行。

下载好大佬提取的 `PingFang.ttc` 之后，首先需要拆分 ttc 到 ttf。第一步，把 `PingFang.ttc` 拖到 `UniteTTC.exe` 上，或者直接在命令行输入 UniteTTC.exe PingFang.ttc 也可以。

这时候会生成很多个 `PingFang00x.ttf` 文件。

![](https://cdn.jsdelivr.net/gh/Innei/fancy-2023@main/2023/1217142905.png)

我们选取其中一个，常规体，苹方-简，这个可以通过打开文件查看。

然后拖动到 `ttfname3+.exe` 上，会生成一个 `PingFang00x.xml`。

对系统的雅黑也进行同样的操作。

现在比较重要的一步，用编辑器打开` PingFang00x.xm`l 和雅黑的 `msyh00x.xml` 进行编辑。

复制 `PingFang00x.xml` 的 `Header` Tag，粘贴到 `msyh00x.xml` 上。

![](https://cdn.jsdelivr.net/gh/Innei/fancy-2023@main/2023/1217142928.png)

这里需要操作两次，一个是 `msyh001.xml` 一个 `msyh002.xml`。第一个是雅黑第二个是雅黑 UI。

然后之后，把 msyh001.xml 和提取的 `PingFang00x.ttf` 同时选中然后拖到 `ttfname3+.exe` 上，会生成一个 `msyh001_mod.TTF`，需要做两次，得到 `msyh001_mod.TTF` 和 `msyh002_mod.TTF`。

然后打开命令行，使用 `UniteTTC.exe msyh_pingfang.ttc msyh001_mod.TTF msyh002_mod.TTF` 合并到 `msyh_pingfang.ttc`。

![](https://cdn.jsdelivr.net/gh/Innei/fancy-2023@main/2023/1217142959.png)

这里字体就做好了。

然后打开字体替换工具。

重启搞定。

