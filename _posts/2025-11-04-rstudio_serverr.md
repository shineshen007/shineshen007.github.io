---
layout: post
title: Rstudio Server卡死
tags: [R]
categories: [error]
---
------------------------------------------------------------------------

# 一、紧急恢复操作
## 查找具体PID后强制终止：

```
rstudio-server active-sessions
rstudio-server kill-session [PID]
```
## 清理会话缓存文件,同时清理临时目录：

```
rm -rf ~/.local/share/rstudio/sessions/* ~/.rstudio-desktop .rproj.user
rm -rf ~/.config/rstudio/* ~/.cache/rstudio
```


```
find /tmp -maxdepth 1 -user "$USER" -name 'rsession-*' -exec rm -rf {} +
```
## 重启RStudio服务

```
sudo systemctl restart rstudio-server
```
