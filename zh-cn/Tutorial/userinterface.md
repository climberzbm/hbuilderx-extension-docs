### 用户界面@userinterface

像许多其他代码编辑器一样，HBuilderX采用通用的用户界面和左侧的资源管理器布局，而右侧的编辑器则显示已打开文件的内容。 

<img src="/static/snapshots/tutorial/userinterface/HBuilderX.png" style="zoom:90%" />

### 基本布局@basic-layout

用户界面主要分为：

* 编辑器 - 编辑文件的主要区域。您可以在垂直和水平方向上并排打开任意数量的编辑器。
* 项目管理器 - 包含诸如资源管理器之类的不同视图，可在您处理项目时为您提供帮助。
* 工具栏
* 状态栏 - 有关打开的项目和您编辑的文件的信息。
* 控制台 - 您可以在编辑器区域下方显示不同的面板，以获取输出或调试信息，错误和警告或集成终端。面板也可以向右移动以获得更多垂直空间。

每次启动HBuilderX时，它的打开状态与上次关闭时的状态相同。

### 迷你地图@minimap

`迷你地图`，为您提供了源代码的高级概述，这对于快速导航和理解代码很有用。

迷你地图, 显示在编辑器的右侧。您可以单击或拖动阴影区域以快速跳至文件的不同部分。

<img src="/static/snapshots/tutorial/userinterface/minimap.png" style="zoom:90%" />

提示：
- 您可以在编辑器最右侧，点击右键，关闭或打开迷你地图。
- 【设置】【编辑器设置】，也可以调整迷你地图像素宽度，默认100

### 文档结构图@outline

左边的大纲是长文档导航的利器。HBuilderX提供了优雅简洁的文档导览界面。

可以点底栏左侧红框内的大纲按钮，对应的快捷键是【win：alt+w、mac：ctrl+w】

<img src="/static/snapshots/tutorial/userinterface/outline.png" style="zoom:90%" />

### 内置资源管理器@Built-in-Explorer

> 此处只是简单介绍下内置资源管理器，请查看[详细用法](Tutorial/UserGuide/built-in-explorer)

传统开发工具，仅仅依靠左侧的项目树来管理资源文件，便利性和效率是远远不够的。
HBuilderX内置的资源管理器，给你一个更大的资源管理界面，大幅提高文件的管理效率。

相比OS自带的资源管理器，HBuilderX资源管理器为编程文件提供专门的优化。

- 在大图预览界面下直接显示html标题、vue页面、组件的名字
- 直接预览markdown的内容
- 在列表详情界面扩充单独的列来显示svn/git状态

<img src="/static/snapshots/tutorial/explorer/explorer.gif" style="zoom:98%" />

### 编辑器布局@editor-layout

HBuilderX，默认情况下，编辑器组以垂直列布局。

当然，您也可以轻松按自己喜欢的任何布局在垂直和水平方向上排列编辑器。

菜单 “视图 -> 分栏”，有一组预定义的编辑器布局。

<img src="/static/snapshots/tutorial/userinterface/subfield.png" style="zoom:98%" />

### 单窗体@single-window

单窗体： 就是项目管理器，只显示一个项目。

在主窗体上，点击菜单【视图】【新建HBuilder窗体】，就可以新建一个单项目窗体。

在主窗体上，选中某个项目，右键菜单，点击【在新窗体中打开】，即可将项目在单项目窗体中打开

[关于单窗体的详细说明与介绍](/Tutorial/UserGuide/multi-window)