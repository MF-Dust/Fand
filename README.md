Fand 
===========

[![Fand CI](https://github.com/FandMC/Fand/actions/workflows/build.yml/badge.svg)](https://github.com/FandMC/Fand/actions/workflows/Fand.yml)
[![Fand Download](https://img.shields.io/github/downloads/FandMC/Fand/total?color=0&logo=github)](https://github.com/FandMC/Fand/releases/latest)
[![QQ](https://img.shields.io/badge/QQ_Unofficial-495796642-blue)](http://qm.qq.com/cgi-bin/qm/qr?_wv=1027&k=cgotyELe3jab6rKnUM5DuWWiaNakOIzZ&authKey=L8yT48eCSzqdtJZtE2%2F7qK8G3xnqs2O5u8zAOu56YLqSLccSo%2FOcjSGkXT8GjkQ1&noverify=0&group_code=495796642)

**English** | [中文](README_cn.md)

> Fork of [Paper](https://github.com/PaperMC/Paper) aims at repairing broken vanilla properties.

> You can see what we modify and fix at [here](https://docs.Fandmc.top)

## How To (Server Admins)
Fand use the same Fandclip(paperclip fork) jar system that Paper uses.

You can download the latest build (1.21.x) of Fand by going [here](https://github.com/FandMC/Fand/releases/latest)

You can also [build it yourself](#building).

You can visit our [documentation](https://docs.Fandmc.top) for more information.

## How To (Plugin developers)
Fand-API:
```kotlin
maven {
    name = "Fandmc-repo"
    url = "https://repo.Fandmc.top/snapshots/"
}

dependencies {
    compileOnly("com.Fandmc.Fand:Fand-api:1.21-R0.1-SNAPSHOT")
}
 ```

In order to use Fand as a dependency you must [build it yourself](#building).
Each time you want to update your dependency, you must re-build Fand.

Fand-Server:
```kotlin
dependencies {
    compileOnly("org.Fandmc.Fand:Fand:1.21-R0.1-SNAPSHOT")
}
 ```

## Building

You need JDK 21 and good Internet conditions

Clone this repo, run `./gradlew applyPatches`, then run `./gradlew createMojmapFandclipJar` in your terminal.  

You can find the jars in the `build/libs` directory.

## Pull Requests

See [Contributing](docs/CONTRIBUTING.md)

## Special Thanks To:

[<img src="https://user-images.githubusercontent.com/21148213/121807008-8ffc6700-cc52-11eb-96a7-2f6f260f8fda.png" alt="" width="150">](https://www.jetbrains.com)

[JetBrains](https://www.jetbrains.com/), creators of the IntelliJ IDEA, supports Fand with one of their [Open Source Licenses](https://www.jetbrains.com/opensource/). Fand recommend using IntelliJ IDEA as your IDE.
