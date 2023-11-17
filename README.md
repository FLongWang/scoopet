# 🍨 Scoopet 🍨

[![Excavator](https://github.com/ivaquero/scoopet/actions/workflows/ci.yml/badge.svg)](https://github.com/ivaquero/scoopet/actions/workflows/ci.yml)
[![license](https://img.shields.io/github/license/ivaquero/scoopet)](https://github.com/ivaquero/scoopet/blob/master/LICENSE)
[![code size](https://img.shields.io/github/languages/code-size/ivaquero/scoopet.svg)](https://img.shields.io/github/languages/code-size/ivaquero/scoopet.svg)
[![repo size](https://img.shields.io/github/repo-size/ivaquero/scoopet.svg)](https://img.shields.io/github/repo-size/ivaquero/scoopet.svg)

A Bucket for the Best Windows Package Manager [Scoop](https://github.com/ScoopInstaller/Scoop): Continuously Assisting in Academic Research.

> If you would like to be a co-maintainer, feel free to create a new issue.

<p align="left">
<a href="README.md">English</a> |
<a href="README-CN.md">简体中文</a>
</p>

For ones familiar with Scoop:

```powershell
scoop bucket add myscoop https://github.com/FLongWang/scoopet.git
```

# :running: To Start

## :bike: Install Scoop

### :computer: Step 1: Enable remote policy in PowerShell

```powershell
Set-ExecutionPolicy RemoteSigned -scope CurrentUser
```

### :gear: Step 2: Download and install Scoop

```powershell
$env:SCOOP='D:\Scoop'
[Environment]::SetEnvironmentVariable('SCOOP',$env:SCOOP,'User')
iex (new-object net.webclient).downloadstring('https://get.scoop.sh')
```

> If you skip this step, all user installed Apps and Scoop itself will live in `D:\Scoop`.

### :book: Step 3: Glance at quick-start by `scoop help`

For more information, please visit Scoop official site at 👉 https://scoop.sh/ 👈

## :car: Install Apps from this bucket

### :train: Step 1: Install Aria2 to accelerate downloading

```powershell
scoop install aria2
```

### :ticket: Step 2: Install Git to add new repositories

```powershell
scoop install git
```

if you are using VPN, you need to turn off aria2 before installing Apps

```powershell
scoop config aria2-enabled false
```

### :airplane: Step 3: Add this wonderful bucket and update, mo-mo-da~ :kiss:

```powershell
scoop bucket add myscoop https://github.com/FLongWang/scoopet.git
scoop update
```

### :rocket: Step 4: Install Apps

#### Check the exact name of App by `scoop search`

```powershell
scoop search <app_name>
```

#### Install Apps with assistance of plugin `scoop-completion`

```powershell
scoop install scoop-completion
scoop install <app_name>
```

> to use `scoop-completion`, just to hit `tab` after initial letters of App names

### :100: Step 5: List the official recommended buckets by `scoop bucket known`

```powershell
scoop bucket known

main [default]
extras [strongly recommended]
versions
nightlies
nirsoft
php
nerd-fonts
nonportable
java
games
jetbrains
```

## :m: Trivial

### Tweak with Parameters in Aria2

```powershell
scoop config aria2-enabled true
scoop config aria2-retry-wait 4
scoop config aria2-split 16
scoop config aria2-max-connection-per-server 16
scoop config aria2-min-split-size 4M
```

## :star: Recommendation

### Research Tools
```powershell
scoop config aria2-enabled false
scoop bucket add myscoop https://github.com/FLongWang/scoopet.git
scoop install sudo
sudo scoop install 7zip openssh main/git --global
scoop install aria2 curl grep sed less touch
scoop install gow cmder winpython extras/obsidian extras/zotero extras/avogadro2 extras/docear  extras/jabref extras/sumatrapdf extras/github extras/irfanview main/ffmpeg extras/ffmpeg-batch extras/vscode extras/potplayer extras/vncviewer myscoop/autodarkmode
scoop install myscoop/texlive
scoop install extras/wechat myscoop/tim
```

