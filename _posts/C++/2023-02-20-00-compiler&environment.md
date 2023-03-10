---
title: 从0开始的C++语言基础00：编译器及C++环境的设置
date: 2023-02-20
categories: [C++]
tags: [c++, environment, compiler]
math: true
---

### WHY: 为什么要使用编译器和搭建C++环境

- ~= 为什么吃饭要使用嘴巴

### WHAT: 什么是编译器和C++环境

- 本小节内容仅供有兴趣者阅读，因为本小节对于竞赛和平时使用并无太大帮助，当然在了解了编译器和环境后对以后的一些C++能够有更深的理解，也有助于以后真正使用C++写程序。
- 暂时不想写，先玩算法竞赛，本小节敬请期待。

### HOW: 如何搭建C++环境及编译器的选择

#### 对于中国体制内参加 `NOI` 的算法竞赛生：dev-cpp

- 不要想花里胡哨好玩的编译器了，老老实实给我用 [dev-cpp](https://sourceforge.net/projects/orwelldevcpp/files/latest/download) <https://sourceforge.net/projects/orwelldevcpp/files/latest/download！>
- 该软件是全国统一的竞赛软件（for c++），因此你即使掌握了再多各种软件和各种功能，考试的时候还是得使用dev-cpp，那为什么不一开始就使用这个软件呢？
- 点击上方即可下载，不要下载最新版。一方面全国的机考都是用该版本dev-cpp，另一方面最新版dev-cpp已闭源商用。开源就是最好的，那么闭源就是最差的，因此不要用最差的闭源软件。（个人喜欢拿逻辑开玩笑，别介意）
- 下载完安装（如果连安装都不会的话就一路点next就行）
  - 该软件会帮你直接安装好编译器并且搭建好C++环境
- 点击左上角空白的纸打开新的一页，写完程序按f11即可保存并运行。

### 其他的竞赛生（线上考生）：vs-code

- 编译器下载
  - 一律推荐使用[vs-code](https://code.visualstudio.com/download) <https://code.visualstudio.com/download>
    - 首先，这个软件比dev-cpp更好用，但是也会更麻烦。因此怕麻烦的话也可以使用上面的dev-cpp。
    - 如果你决定使用vs-code，那么恭喜你，你将获得一个可以使用一生的软件。vs-code支持所有语言，你还可以把它当作一个txt阅读器，上面还有一堆插件，你甚至可以把它折腾成一个 *all in one* 的软件。
  - 下载完后安装，没什么需要强调的，上面默认勾选的已经足够正常使用了（如果连安装都不会的话，请仔仔细细看完每个页面的内容，选择自己的需求，然后点击下一步。如果你不愿意那么麻烦的话，那不太建议你使用vs-code，可以使用上面dev-cpp，毕竟安装连使用的第一步都算不上）
  - 打开之后在最左边侧栏点击积木（插件extentions），搜索框输入c++，找到并点击由 `microsoft` 发布的 `C/C++`，之后在右边主界面上方点击 `Install`
  - 搜索 `Code Runner` ，下载由 `Jun Han` 发布的 `Code Runner`
- C++环境配置
  - 下载并安装[mingw64](http://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win32/Personal%20Builds/mingw-builds/installer/mingw-w64-install.exe/download) <http://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win32/Personal%20Builds/mingw-builds/installer/mingw-w64-install.exe/download>
  - 添加 `安装路径\mingw64\bin` 至全局变量
    - 打开按开始菜单，在搜索框输入 `environment` 找到更改全局变量并点击
    - 在新界面右下角由 `全局变量` 点击
    - 在新界面下方栏找到 `Path` 一项双击打开
    - 右上角点击 `新建`
    - 填入 `安装路径\mingw64\bin`
    - OK保存并退出
- 编译器配置
  - 在代码用文件夹创建 `.vscode` 文件夹并创建 `tasks.json` ，写入一下内容：（记得替换文件路径）

```json
{
    "tasks": [{
            "type": "cppbuild",
            "label": "C/C++: g++.exe build active file",
            "command": "文件路径（记得改为 \\ 形式）\\mingw64\\bin\\g++.exe",
            "args": [
                "-fdiagnostics-color=always",
                "-g",
                "${file}",
                "-o",
                "${fileDirname}\\${fileBasenameNoExtension}.exe"
            ],
            "problemMatcher": [
                "$gcc"
            ],
            "group": {
                "kind": "build",
                "isDefault": true
            },
        }
    ],
    "version": "2.0.0"
}
```

- 创建你的cpp文件并点击右上角三角号运行吧！
