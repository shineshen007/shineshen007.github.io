---
layout: post
title: Cytoscape中使用MCODE app进行代谢-蛋白-基因网络分析
tags: [idea]
categories: [multi-omics]
---
------------------------------------------------------------------------


## 1.下载MCODE 
可以在cytoscape或者网上直接搜索安装文件进行安装。[metscape](https://apps.cytoscape.org/apps/metscape)

## 2.使用方法
打开cytoscape-任务栏app-metscape-build network-选择pathway based或者correlation based-左下方控制面板select-上传基因和代谢物的数据，数据格式如下：

id|pvalue|fc
--|:--:|--:
gene1|0.02|3
gene2|0.01|1
gene3|0.06|2
