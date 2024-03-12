---
layout: post
title: 单细胞Featureplot 统一图例scale
tags: [单细胞]
categories: [多组学]
---

------------------------------------------------------------------------
## 美化legend
```
m_featureplot <- FeaturePlot(M_Aggregated_seurat, features = "Lepr", reduction = "tsne",
                             split.by = "orig.ident", pt.size = 1.8, repel = F, label = F,
                             order = T, max.cutoff = 1)
m_featureplot <- m_featureplot & scale_x_continuous(breaks=seq(-30, 20, 10)) ## 改x轴刻度标签
m_featureplot <- m_featureplot & scale_y_continuous(breaks=seq(-30, 20, 10)) ## 改y轴刻度标签
m_featureplot <- m_featureplot +  theme(axis.text.y = element_blank()) +   ## 删去所有刻度标签
                                  theme(axis.ticks.y = element_blank()) +  ##则只删去 Y 轴的刻度线
                                  theme(axis.line.y = element_blank())
m_featureplot <- m_featureplot + ylab("")
```

## 修改颜色
```
FeaturePlot(pbmc_small, "LYZ") + scale_colour_gradientn(colours = rev(brewer.pal(n = 11, name = "RdBu")))
```

## 修改scale范围
```
p1 <- FeaturePlot(pbmc_small, features = c("PPBP", "IGLL5", "SDPR"), combine = FALSE )
fix.sc <- scale_color_gradientn( colours = c('lightgrey', 'blue'),  limits = c(1, 8))
p2 <- lapply(p1, function (x) x + fix.sc)
CombinePlots(p2)
```

reference[https://www.jianshu.com/p/8cea50fcb30c]
