---
layout: post
title: "Correlation analysis in R"
tags: ["Correlation analysis"]
categories: ["R"]
---

## Introduction to Correlation analysis

  In correlation analysis, we estimate a sample correlation coefficient, more specifically the Pearson Product Moment correlation coefficient. The sample correlation coefficient, denoted r,
ranges between -1 and +1 and quantifies the direction and strength of the linear association between the two variables. 

  The correlation between two variables can be positive or negative.The sign of the correlation coefficient indicates the direction of the association. The magnitude of the correlation coefficient indicates the strength of the association.
  
  For example, a correlation of r = 0.9 suggests a strong, positive association between two variables, whereas a correlation of r = -0.2 suggest a weak, negative association. A correlation close to zero suggests no linear association between two continuous variables.
  
From --Boston University School of Public Health

# correlation plot
```{r mtcars}
head(mtcars)
cor<-psych::corr.test(mtcars,adjust = 'fdr')
r<-cor[["r"]]
  col=colorRampPalette(c("navy","white","firebrick3"))
  corrplot::corrplot(r,tl.col="black", tl.srt=45,tl.cex = 0.6,number.cex = 0.6,
           addCoefasPercent = TRUE,cl.lim = c(-1,1),addCoef.col = "black",col = col(10))
```


