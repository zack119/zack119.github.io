---
layout: post
title: OSX 使用手记
---

# {{ page.title }}

## 系统设置

- **清除OpenWith的重复项**  
在终端中进入 `/Applications/Utilities/` 目录，执行  
```
/System/Library/Frameworks/CoreServices.framework/Versions/A/Frameworks/\
LaunchServices.framework/Versions/A/Support/\
lsregister -kill -r -domain local -domain user
killall Finder
```
如果执行完了没效果，可以删掉 `~/Library/Preferences/com.apple.LaunchServices.plist` 再试。

- **清除DNS缓存**  
在终端中输入 `sudo killall -HUP mDNSResponder`

- **在Dock上显示最近使用的10个APP**  
在终端中输入：
`defaults write com.apple.dock persistent-others -array-add '{ "tile-data" = { "list-type" = 1; }; "tile-type" = "recents-tile"; }'`

- **删除未下载完的App图标**  
```
defaults write com.apple.dock ResetLaunchPad -bool true
killall Dock
```

## 软件设置

- **设置Sublime Text命令行**  
`sudo ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/bin/subl`

- **删掉迅雷对浏览器的劫持插件**  
需要清除两个目录的插件: `~/Library/Internet Plug-Ins/` 和 `/Applications/Thunder.app/Contents/BrowserPlugins`

- **备份 Alfred Custom Search 设置**  
Custom Search 配置路径：`~/Library/Application Support/Alfred/customsites`，可以通过"AlfredTips":http://alfredtips.com/home/ 收集到一些不错的Custom Search配置。


