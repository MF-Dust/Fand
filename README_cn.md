Fand
===========

[![Fand CI](https://github.com/FandMC/Fand/actions/workflows/Fand.yml/badge.svg)](https://github.com/FandMC/Fand/actions/workflows/Fand.yml)
[![Fand Download](https://img.shields.io/github/downloads/FandMC/Fand/total?color=0&logo=github)](https://github.com/FandMC/Fand/releases/latest)
[![Discord](https://badgen.net/discord/online-members/5hgtU72w33?icon=discord&label=Discord&list=what)](https://discord.gg/5hgtU72w33)
[![QQ](https://img.shields.io/badge/QQ_Unofficial-495796642-blue)](http://qm.qq.com/cgi-bin/qm/qr?_wv=1027&k=cgotyELe3jab6rKnUM5DuWWiaNakOIzZ&authKey=L8yT48eCSzqdtJZtE2%2F7qK8G3xnqs2O5u8zAOu56YLqSLccSo%2FOcjSGkXT8GjkQ1&noverify=0&group_code=495796642)

[English](README.md) | **中文**

> 一个致力于修复原版服务端被破坏特性的 [Paper](https://github.com/PaperMC/Paper) 分支

> 你可以在 [这里](https://docs.fandmc.cn) 查看所有的修改和修复内容

## 对于服务器管理员
此分支使用与 Paper 一致的 Fandclip(paperclip的分支) 分发

你可以从 [此处](https://github.com/FandMC/Fand/releases/latest) 下载最新的构建结果 (1.21.x)

也可以通过 [此处](#自行构建) 的指南自行构建

如果你想要获得更多信息，那么你可以访问我们的 [文档](https://docs.fandmc.cn)

## 对于插件开发者
Fand-API:
```kotlin
maven {
    name = "Fandmc-repo"
    url = "https://repo.fandmc.cn/snapshots/"
}

dependencies {
    compileOnly("com.Fandmc.Fand:Fand-api:1.21-R0.1-SNAPSHOT")
}
 ```

如果你要将 Fand 作为依赖,那么你必须进行 [自行构建](#自行构建)

Fand-Server:
```kotlin
dependencies {
    compileOnly("com.Fandmc.Fand:Fand:1.21R0.1-SNAPSHOT")
}
 ```

## 自行构建

你需要最低 JDK 21 和一个可以正常访问各种 git/maven 库的网络

首先克隆此储存库，然后在你的终端里依次执行 `./gradlew applyPatches` 和 `./gradlew createMojmapFandclipJar`

最后 你可以在 `build/libs` 文件夹里找到对应的jar文件

## 对于想要出一份力的开发者

可查看 [贡献须知](docs/CONTRIBUTING_cn.md)