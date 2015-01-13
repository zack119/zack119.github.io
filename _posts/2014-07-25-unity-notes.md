---
layout: post
title: Unity 手记
---

# {{ page.title }}

## 备忘

### Assets Store 下载目录
PC： `C:\Users\[UserName]\AppData\Roaming\Unity\Asset Store`  
MAC： `~/Library/Unity/Asset\ Store`

### 多开方法
首先找到桌面快捷方式，右键点击，选择属性，找到快捷方式一栏，查看目标，例如，会有如下`E:\UnityEditor\Editor\Unity.exe`，只要我们在后边添加（ -projectPath），即变成`E:\UnityEditor\Editor\Unity.exe -projectPath`

### gitignore排除列表
```
[Ll]ibrary/
[Tt]emp/
[Oo]bj/

/*.csproj
/*.unityproj
/*.sln
/*.suo
/*.user
/*.userprefs
/*.pidb
/*.booproj

sysinfo.txt
```