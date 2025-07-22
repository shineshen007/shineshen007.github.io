---
layout: post
title: Cytoscape中使用Metascape app进行代谢-蛋白-基因网络分析
tags: [idea]
categories: [Multi-Omics]
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

选择网络组成
<img width="448" height="128" alt="image" src="https://github.com/user-attachments/assets/2fdc168e-1d88-43d9-9232-effc175765f9" />

选择目标通路
<img width="459" height="255" alt="image" src="https://github.com/user-attachments/assets/acdf0e06-8f00-4dfb-bb4c-08880632635b" />

build network

## 3.调整网络
根据需要调整overlap，然后导出pdf

## 4.legend
legend需要单独显示，保存为一个pdf，跟主图何必
