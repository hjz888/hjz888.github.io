---
layout: post
title: "Visual Studio Code Python 基本設定篇"
subtitle: "Visual Studio Code Python 基本設定篇"
author: "灰兔"
header-style: text
tags:
  - vscode
---











# Visual Studio Code Python 基本設定篇



這篇文章將會教大家如何建立自己的 Visual Studio Code Python 開發環境 📝

- [Youtube - Visual Studio Code Python 基本設定篇](https://youtu.be/tS4beaq9ies)
- [Youtube - Visual Studio Code Python Importmagic - Auto import,complete](https://youtu.be/5MgvnPKfrMg)

## 說明



最近剛好接觸到使用 VSCode 開發 Python，所以就有了這篇文章:smile:

其實我之前都是使用 Pycharm Professional 來開發的 ( 雖然他要付費，但是功能真的強:+1:)

如果想當免費仔，可以使用 VSCode，但我覺得需要稍微設定一下 ( 這篇文章會教大家 )。

請先準備以下的功課

- 安裝 python 以及 Visual Studio Code

## 步驟一 - 建立 virtual environments



首先，別急著打開 VSCode，先來建立環境，如果你不知道如何建立環境，

可參考這篇文章 [python venv 建立 virtual environments](https://github.com/twtrubiks/python-creation-of-virtual-environments)

( 以前我教過大家 [使用 Anaconda 建立 Python 環境](https://github.com/twtrubiks/FaceDetect/tree/master/How Easy Install OpenCV  for Python use Anaconda#使用-anaconda-建立-python-環境)，但因為 Anaconda 實在很肥，

如果沒有特別的需求，使用 python venv 即可 )

這邊就先建立一個 venv_demo 的環境，

[![alt tag](https://camo.githubusercontent.com/5c6b831a8b6eda3d5a37d78f29f7fcca592e644c0454216e2e1cd740473f664e/68747470733a2f2f692e696d6775722e636f6d2f636d784b6839412e706e67)](https://camo.githubusercontent.com/5c6b831a8b6eda3d5a37d78f29f7fcca592e644c0454216e2e1cd740473f664e/68747470733a2f2f692e696d6775722e636f6d2f636d784b6839412e706e67)

## 步驟二 - 設定 VSCode



這邊為了方便後續的說明，先建立一個資料夾，資料夾名稱 demo，裡面新增一個 demo.py 的檔案，

開啟的方式很多種，這邊直接右鍵開啟，

[![alt tag](https://camo.githubusercontent.com/31a42c064e464ec9a8a0096e63609b24dc782f658b76079b5dbac0c5a03366ff/68747470733a2f2f692e696d6775722e636f6d2f577a6b6f43544e2e706e67)](https://camo.githubusercontent.com/31a42c064e464ec9a8a0096e63609b24dc782f658b76079b5dbac0c5a03366ff/68747470733a2f2f692e696d6775722e636f6d2f577a6b6f43544e2e706e67)

打開後，快捷鍵 `Ctrl+Shift+P`，然後輸入 settings

[![alt tag](https://camo.githubusercontent.com/809fa1ef5b3d3761ae9d6184131964d3d5dba25779a73b39b58b1cc0de0bba00/68747470733a2f2f692e696d6775722e636f6d2f485437595344742e706e67)](https://camo.githubusercontent.com/809fa1ef5b3d3761ae9d6184131964d3d5dba25779a73b39b58b1cc0de0bba00/68747470733a2f2f692e696d6775722e636f6d2f485437595344742e706e67)

主要先看這兩個即可，分別是

Preferences: Open User Settings : 你可以簡單把他想成是全域的。

Preferences: Open Workspace Settings : 只在你的工作目錄內才會生效 ( 工作目錄內會多出一個資料夾 )。

這邊我們先選擇 Preferences: Open User Settings，

這邊是 ui 的呈現 ( 可直接在這邊修改 )，但我喜歡用 json 的方式，點選右邊

[![alt tag](https://camo.githubusercontent.com/a48c667ee500659cba02a3aa3a2fa629a0b4d895511f7ab723e4d8f4a6e517f7/68747470733a2f2f692e696d6775722e636f6d2f616a467a514d322e706e67)](https://camo.githubusercontent.com/a48c667ee500659cba02a3aa3a2fa629a0b4d895511f7ab723e4d8f4a6e517f7/68747470733a2f2f692e696d6775722e636f6d2f616a467a514d322e706e67)

這裡面有可能有你自己的設定，這邊是我自己的設定，大家可以參考一下，

[![alt tag](https://camo.githubusercontent.com/e89e5f4ae23eeddd43e6c32b6c5678a22021c4bfc0f39fa689f851689f0308ec/68747470733a2f2f692e696d6775722e636f6d2f327856716346532e706e67)](https://camo.githubusercontent.com/e89e5f4ae23eeddd43e6c32b6c5678a22021c4bfc0f39fa689f851689f0308ec/68747470733a2f2f692e696d6775722e636f6d2f327856716346532e706e67)

```
{
    // User Settings

    "window.zoomLevel": 1, // 視窗縮放
    // "editor.fontSize": 22,
    // "editor.lineHeight": 26,
    // "terminal.integrated.fontSize": 30, // terminal 字體大小
    // "editor.formatOnSave": true, // 當儲存時，是否自動格式化
    "files.autoSave": "onFocusChange", // 是否自動儲存檔案

    // 注意，win 用戶都要使用 "\\"
    //"python.defaultInterpreterPath": "C:\\Users\\twtru\\Anaconda3\\envs\\venv_temp\\python.exe", // 預設的 PYTHON 執行環境

    "extensions.ignoreRecommendations": true, // 是否忽略顯示建議的套件
    "files.encoding": "utf8", // 設定預設編碼
    "files.trimTrailingWhitespace": true, // 儲存的時候，會幫你自動過濾多餘的空格
    "files.autoGuessEncoding": false, // 是否自動猜測檔案的編碼
    "terminal.integrated.shell.windows": "C:\\WINDOWS\\System32\\cmd.exe",
    // "workbench.welcome.enabled": false, // 使否關閉 vscode 歡迎的顯示頁面
    "workbench.startupEditor": "newUntitledFile",
    "explorer.confirmDelete": false,

    // "workbench.colorTheme": "One Dark Pro", // 需安裝 One Dark Pro
    "workbench.iconTheme": "vscode-icons",  // 需安裝 vscode-icons
}
```



( `python.defaultInterpreterPath` 這個其實不用另外設定，已註解掉 )

( 其實 json 是不適合註解的，所以才會變成這樣，但不註解我怕大家不了解 )

儲存後就會生效。

也不用擔心亂輸入或輸入錯了會造成什麼問題，如果你打錯字或沒這個東西，VSCode 會提醒你。

接著選擇 Preferences: Open Workspace Settings，

你會發現目錄資料夾底下多了一個 `\.vscode\settings.json` ( 因為這是 Workspace Settings )

[![alt tag](https://camo.githubusercontent.com/9d8b0f56b8e34f4fb134e4ae32d7f47381ee2bee9c745ab070be7f7ab7116ecf/68747470733a2f2f692e696d6775722e636f6d2f704b444e5950392e706e67)](https://camo.githubusercontent.com/9d8b0f56b8e34f4fb134e4ae32d7f47381ee2bee9c745ab070be7f7ab7116ecf/68747470733a2f2f692e696d6775722e636f6d2f704b444e5950392e706e67)

這邊是我自己的設定，大家可以參考一下，

[![alt tag](https://camo.githubusercontent.com/91b45f6f5165b3771c7f1572b0c8e7199276ff20e409a87f7fbd253dd794b05d/68747470733a2f2f692e696d6775722e636f6d2f426d31466f65372e706e67)](https://camo.githubusercontent.com/91b45f6f5165b3771c7f1572b0c8e7199276ff20e409a87f7fbd253dd794b05d/68747470733a2f2f692e696d6775722e636f6d2f426d31466f65372e706e67)

```
{
    // Workspace Settings

    // virtual environments 中的 python 執行檔
    // "python.defaultInterpreterPath": "C:\\Users\\twtru\\OneDrive\\work\\venv\\venv_demo\\Scripts\\python.exe",

    // 可以設定你放全部的 venvs 環境的根目錄資料夾
    "python.venvPath": "C:\\Users\\twtru\\OneDrive\\work\\venv",

    "python.terminal.activateEnvironment": true, // 自動啟動環境
    "python.linting.pylintEnabled": true,  // 需要 pip install pylint
    "python.linting.enabled": true,  // 需要 pip install pylint
}
```



( `python.defaultInterpreterPath` 這個其實不用另外設定，已註解掉 )

( 其實 Workspace Settings 這邊的設定，都可以搬到 User Settings 裡面)

如果你的 python.venvPath 有設定對，你看你的左下角

[![alt tag](https://camo.githubusercontent.com/c5ab44aad62cb626fd21cc180136c713012d5c3ee1a7d04681ebb85f2bfd1a84/68747470733a2f2f692e696d6775722e636f6d2f50426f326162302e706e67)](https://camo.githubusercontent.com/c5ab44aad62cb626fd21cc180136c713012d5c3ee1a7d04681ebb85f2bfd1a84/68747470733a2f2f692e696d6775722e636f6d2f50426f326162302e706e67)

選他你會看到資料夾裡面全部的 venv，點了就可以啟動。

[![alt tag](https://camo.githubusercontent.com/699e0b0e855da8f1859a65855bacbb294cb9172f742657092c491b4d2e0b81f6/68747470733a2f2f692e696d6775722e636f6d2f716e3178564d322e706e67)](https://camo.githubusercontent.com/699e0b0e855da8f1859a65855bacbb294cb9172f742657092c491b4d2e0b81f6/68747470733a2f2f692e696d6775722e636f6d2f716e3178564d322e706e67)

( 如果看不到，請重新打開 VSCode，另外要 **注意 Workspace Settings 會覆蓋 User Settings** )

linting 有很多種，這邊選擇 pylint，更多資訊可參考 [Linting Python in Visual Studio Code](https://code.visualstudio.com/docs/python/linting)，

儲存完畢後，快捷鍵 Ctrl+Shift+` 開啟 terminal，

你會發現環境自動啟動了 ( 看前面的小括號 venv_demo )。

( 另外一點要注意的是，VSCode 是偵測你有沒有 .py 的檔案，所以記得要在 .py 的檔案下 Ctrl+Shift+` 開啟 terminal，

否則你會覺得很怪，一直無法自動啟動環境 )

( 如果沒有啟動，可以關掉目前的 terminal 再開一個 terminal 試試看，如果還是不行，關掉 VSCode 重開，

再不行，檢查是不是設定錯了 )

[![alt tag](https://camo.githubusercontent.com/1171f5a4c40e7fb54ee2451b53799e81194d9a497914db6a2857c6198ba9e4d4/68747470733a2f2f692e696d6775722e636f6d2f6176355874564b2e706e67)](https://camo.githubusercontent.com/1171f5a4c40e7fb54ee2451b53799e81194d9a497914db6a2857c6198ba9e4d4/68747470733a2f2f692e696d6775722e636f6d2f6176355874564b2e706e67)

大家應該有發現右下角告訴我們沒安裝 pylint ，這時候請安裝 `pip install pylint`

[![alt tag](https://camo.githubusercontent.com/ef8e2a125e4a3eb56159c19ba75ec8b7a6e1cfda61c5614dbf8881b02637f41c/68747470733a2f2f692e696d6775722e636f6d2f484350794c6c4a2e706e67)](https://camo.githubusercontent.com/ef8e2a125e4a3eb56159c19ba75ec8b7a6e1cfda61c5614dbf8881b02637f41c/68747470733a2f2f692e696d6775722e636f6d2f484350794c6c4a2e706e67)

也可以 快捷鍵 `Ctrl+Shift+P`，然後輸入 linting 檢查一下

[![alt tag](https://camo.githubusercontent.com/7a918fa9c0fa557c568af3a0e11387e8af300edad92948d1bb54986b88f99ff1/68747470733a2f2f692e696d6775722e636f6d2f355631426f556a2e706e67)](https://camo.githubusercontent.com/7a918fa9c0fa557c568af3a0e11387e8af300edad92948d1bb54986b88f99ff1/68747470733a2f2f692e696d6775722e636f6d2f355631426f556a2e706e67)

會是 on 的狀態，因為設定了 `"python.linting.enabled": true`

[![alt tag](https://camo.githubusercontent.com/1c8010c73d78c46b41b9e50e8fc6540baa5ef7a3ec28008e9f552ef822a092c0/68747470733a2f2f692e696d6775722e636f6d2f735834767163392e706e67)](https://camo.githubusercontent.com/1c8010c73d78c46b41b9e50e8fc6540baa5ef7a3ec28008e9f552ef822a092c0/68747470733a2f2f692e696d6775722e636f6d2f735834767163392e706e67)

如果成功設定,

在 problems 底下會有很多提醒 ( code 會有一些毛毛蟲 )

[![alt tag](https://camo.githubusercontent.com/a77cc1f0042752c80a165f9816f2bb71e3c72809fe2dfbe8f100cf728b9a4670/68747470733a2f2f692e696d6775722e636f6d2f455446436a42582e706e67)](https://camo.githubusercontent.com/a77cc1f0042752c80a165f9816f2bb71e3c72809fe2dfbe8f100cf728b9a4670/68747470733a2f2f692e696d6775722e636f6d2f455446436a42582e706e67)

( 如果一直沒正確啟用 pylint, 可以重新開啟 vscode 或檢查安裝環境 )

也可以新增 `.pylintrc` 設定一些過濾

```
[MASTER]
# Exclude specific files or directories (comma-separated)
# ignore=.vscode/*,/test/src/tests/*
# ignore-patterns=**/test/src/tests/*.py

[pylint.messages_control]
disable = C0115,C0116,C0115,W0718
```



## 推薦的擴充套件



### Todo Tree



顯示 TODO, FIXME, etc. comment tags in a tree view

[Todo Tree](https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.todo-tree)

### YAML



YAML 格式工具

[YAML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml)

### Rainbow CSV



CSV 格式工具

[Rainbow CSV](https://marketplace.visualstudio.com/items?itemName=mechatroner.rainbow-csv)

### One Dark Pro



Atom's iconic One Dark theme

[One Dark Pro](https://marketplace.visualstudio.com/items?itemName=zhuangtongfa.Material-theme)

### Git History



查看 git 的工具

[Git History](https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory)

### Code Spell Checker



檢查錯字.

[Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)

### EditorConfig for VS Code



統一設定檔案 可參考 [.editorconfig](https://github.com/twtrubiks/vscode_python_note/blob/master/.editorconfig)

[EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)

### Ruff



更強大更快的 Python linter (使用 Rust 寫的)

[Ruff](https://marketplace.visualstudio.com/items?itemName=charliermarsh.ruff)

```
pip install ruff
```



設定 Ruff 為預設的 formatter,

```
{
  "[python]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "charliermarsh.ruff"
  }
}
```



設定自動 import 排版以及 fixAll

```
{
  "[python]": {
    "editor.codeActionsOnSave": {
      "source.fixAll.ruff": "explicit",
      "source.organizeImports.ruff": "explicit"
    }
  }
}
```



### Python Debugger



[Python Debugger](https://marketplace.visualstudio.com/items?itemName=ms-python.debugpy)

建議搭配 [Python debugging in VS Code](https://code.visualstudio.com/docs/python/debugging) 一起觀看

必要時需要安裝 `pip install debugpy`

`request` 主要有 `launch` 和 `attach`,

```
launch
```

這個就是最一般從 vscode 中 debug 重頭開始這樣.

```
attach
```

差別在於, 是調用已經啟動的進程, 意思就是必須再開一個視窗去執行這個 debug,

通常會用在已經運行的程式, 或是外部工具啟用的程序(像是 docker)

這兩個的差別使用 [vscode-django-note](https://github.com/twtrubiks/vscode_django_note) 來參考.

```
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Django launch",
            "type": "debugpy",
            "request": "launch",
            "program": "${workspaceFolder}\\manage.py",
            "args": [
                "runserver",
                "--noreload",
            ],
            "django": true
        },
        {
            "name": "Django attach",
            "type": "debugpy",
            "request": "attach",
            "connect": {
                "host": "localhost",
                "port": 18000
            },
            "django": true
        }
    ]
}
```



`launch` Django launch

這很簡單, 中斷點開下去就可以了.

`attach` Django attach

首先, 先打開一個 terminal 執行 django, 並且要監聽一個 port, 這邊設定 18000

```
python -m debugpy --listen 0.0.0.0:18000 manage.py runserver 0.0.0.0:8000
```



接著再開啟一個 terminal 去執行中斷點 Django attach (也是設定 18000 port),

透過這個就可以成功的進入中斷點.

### Dev Containers



vsocde 可以在 docker 內建立容器並且開發.

[Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

### Importmagic



這個已經一陣子沒更新了.

- [Youtube - Visual Studio Code Python Importmagic - Auto import,complete](https://youtu.be/5MgvnPKfrMg)

一定有人問 VScode 是否有 auto Import 以及 auto complete 的功能:smile:

Vscode 原生是不支援 auto Import 而且不完整，

這些功能其實需要搭配 [Importmagic](https://marketplace.visualstudio.com/items?itemName=brainfit.vscode-importmagic&fbclid=IwAR2WIhgRxvxeCv3vEGDc56dDQp2idFuDCDPgDqF2vXAiF7nQ4eoDGL_2q7E)😏 ( pylint 建議啟用 )，

當你安裝好 Importmagic 之後 ( 建議重啟 )，看下面這個例子，

當我輸入 `datetim` 的時候，他就會偵測到

[![alt tag](https://camo.githubusercontent.com/b490ab0aa1dd9449dbb67bdeedf9ad9612dbb5e100d92111dfd5048a7b1e87ad/68747470733a2f2f692e696d6775722e636f6d2f50535477586a692e706e67)](https://camo.githubusercontent.com/b490ab0aa1dd9449dbb67bdeedf9ad9612dbb5e100d92111dfd5048a7b1e87ad/68747470733a2f2f692e696d6775722e636f6d2f50535477586a692e706e67)

必且有 auto import 的功能

[![alt tag](https://camo.githubusercontent.com/56b52672adb7db86259a1625bdb55332bac6bdc18c770451b8b9f137e53805fa/68747470733a2f2f692e696d6775722e636f6d2f655a4b447a49452e706e67)](https://camo.githubusercontent.com/56b52672adb7db86259a1625bdb55332bac6bdc18c770451b8b9f137e53805fa/68747470733a2f2f692e696d6775722e636f6d2f655a4b447a49452e706e67)

當你第二次再打的時候，可能輸入 `d` 就會跳出選項了。

[![alt tag](https://camo.githubusercontent.com/90ab929b06e34a53f3ea943bf3d4a8b98817e2f204950b68f9487fc6b0234629/68747470733a2f2f692e696d6775722e636f6d2f4c72714336677a2e706e67)](https://camo.githubusercontent.com/90ab929b06e34a53f3ea943bf3d4a8b98817e2f204950b68f9487fc6b0234629/68747470733a2f2f692e696d6775722e636f6d2f4c72714336677a2e706e67)

但今天假設是我們自訂的 Class 可以自動 import 嗎:question:

答案是不行的:cry:

[![alt tag](https://camo.githubusercontent.com/88254ae41f2a93ba300f675d3ef18a2d840ebc1af92eabc366f2656afcdfc2b6/68747470733a2f2f692e696d6775722e636f6d2f3746676e39526c2e706e67)](https://camo.githubusercontent.com/88254ae41f2a93ba300f675d3ef18a2d840ebc1af92eabc366f2656afcdfc2b6/68747470733a2f2f692e696d6775722e636f6d2f3746676e39526c2e706e67)

這時侯，我們就需要透過

[settings.json](https://github.com/twtrubiks/vscode_python_note/blob/master/.vscode/settings.json)

```
{
    //"python.defaultInterpreterPath": "D:\\python_venv\\tutorial-venv\\Scripts\\python.exe",  //已說明過
    "python.linting.pylintEnabled": true, //已說明過
    "python.linting.enabled": true, //已說明過
    "python.autoComplete.extraPaths": [
        "D:\\python_venv\\tutorial-venv",  // 設定你的 venv 的環境目錄資料夾，為了偵測一些 python library
        "E:\\temp\\work\\self\\vscode_python_note\\src", // 目的是偵測自己自定義的 class
    ],
    "python.autoComplete.addBrackets": true, // 是否自動加上括號 (等等文章會補充說明)
    "files.autoSave": "afterDelay", // delay 後儲存
    "files.autoSaveDelay": 500,    // 延遲 500ms
}
```



這邊先補充說明一下 `"python.autoComplete.addBrackets": true`，

假設今天輸入 `import os`，然後輸入 `os.getcwd`，當他跳出提示給你選的時候，

當你選擇它，會自動幫你補括號，也就是 `os.getcwd()`; 相反的，如果是設定為

`false`，你就只會顯示 `os.getcwd`。 ( 如果這邊看不懂建議看影片說明 )

接著繼續講 [Importmagic](https://marketplace.visualstudio.com/items?itemName=brainfit.vscode-importmagic&fbclid=IwAR2WIhgRxvxeCv3vEGDc56dDQp2idFuDCDPgDqF2vXAiF7nQ4eoDGL_2q7E) 這個套件，

最重要的就是設定 `"python.autoComplete.extraPaths"`，

而且要設定正確，否則你會發現為什麼它不 work:question:

( 我這邊是指定某個資料夾底下的 Class 而已，如果你要讓它全部都偵測到，也可以設定

`"E:\\temp\\work\\self\\vscode_python_note"`，其實就是設定這個目錄 )

如果你設定正確，當你切換到任意 python 檔案的時候，

請注意下面 ( 很重要 ❗❗❗我被雷到，想說怎麼沒 work )

[![alt tag](https://camo.githubusercontent.com/1d95779b670f4b482733db0003d1dcab5539d6a753d42067246860481d43f3a1/68747470733a2f2f692e696d6775722e636f6d2f325752747950692e706e67)](https://camo.githubusercontent.com/1d95779b670f4b482733db0003d1dcab5539d6a753d42067246860481d43f3a1/68747470733a2f2f692e696d6775722e636f6d2f325752747950692e706e67)

[![alt tag](https://camo.githubusercontent.com/2c0f0d994b9853d3a060138f27d32c8c73aa9c1a01a50e89c861823d8a845650/68747470733a2f2f692e696d6775722e636f6d2f366f68696749302e706e67)](https://camo.githubusercontent.com/2c0f0d994b9853d3a060138f27d32c8c73aa9c1a01a50e89c861823d8a845650/68747470733a2f2f692e696d6775722e636f6d2f366f68696749302e706e67)

一定要讓他 scan 完以及 index 都跑完，這樣才會有效果，

當你每次改 code，儲存的時候也會重跑。

如果你設定正確，效果如下，可以偵測到自定義的 Class 了

[![alt tag](https://camo.githubusercontent.com/8b91153ea99351a837447048bd30a56165ac9ab24b42df18c45a05376430cdac/68747470733a2f2f692e696d6775722e636f6d2f344d53305256782e706e67)](https://camo.githubusercontent.com/8b91153ea99351a837447048bd30a56165ac9ab24b42df18c45a05376430cdac/68747470733a2f2f692e696d6775722e636f6d2f344d53305256782e706e67)

也有 auto import 的功能

[![alt tag](https://camo.githubusercontent.com/cf772df5deba1904480405c3e374442a3bf5c2073a087341733d2bb35e05afe1/68747470733a2f2f692e696d6775722e636f6d2f623643366151312e706e67)](https://camo.githubusercontent.com/cf772df5deba1904480405c3e374442a3bf5c2073a087341733d2bb35e05afe1/68747470733a2f2f692e696d6775722e636f6d2f623643366151312e706e67)

第二次輸入，打幾個字就會跳出選項了

[![alt tag](https://camo.githubusercontent.com/916d05acfd1d5aa27ba2856ccb74dd6ce4bbbca1f0b219d024c82f230ee02367/68747470733a2f2f692e696d6775722e636f6d2f717830584848412e706e67)](https://camo.githubusercontent.com/916d05acfd1d5aa27ba2856ccb74dd6ce4bbbca1f0b219d024c82f230ee02367/68747470733a2f2f692e696d6775722e636f6d2f717830584848412e706e67)

以上就是 [Importmagic](https://marketplace.visualstudio.com/items?itemName=brainfit.vscode-importmagic&fbclid=IwAR2WIhgRxvxeCv3vEGDc56dDQp2idFuDCDPgDqF2vXAiF7nQ4eoDGL_2q7E) 的介紹。

## 結論



基本上 VSCode 可以設定的東西真的非常的多，大家可以自行摸索。:relaxed:

這篇是教大家一些很基本的設定，未來如果有機會，再介紹更多的功能給各位認識。