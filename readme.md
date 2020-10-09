# Electron_demo

项目本身是一个黑客帝国数字雨前端页面的效果，但是突然想到是不是可以打包成桌面app或者壁纸，找到了一个开源的前端打包源--Electron。

[Electron官方构建](https://www.electronjs.org/docs/tutorial/first-app)
## 环境

- node.js
- git+npm
- electron


# 使用

配置好环境后,在cmd输入 “node -v” ，回车，显示Node版本；再输入 “npm -v” ，回车，如果正常显示npm版本，说明你安装成功了.

可以新建文件夹或者在本文件夹打开cmd或者power shell进行初始化。其中entry point修改为main.js、

```
npm init
```


- 安装electron
```
npm install --save-dev electron
```

然后新建一个main.js文件，文件内容可以根据自己的需求修改。项目中的main.js就是一个例子。

- 安装electron-package。打开Windows PowerShell，输入“npm install electron-packager -g”，回车。

然后修改package.json。在"scripts"中加入"packager"配置：
```
 "start": "electron .",
 "packager":"electron-packager ./ Myexe --platform=win32 --arch=x64 --electron-version=1.8.4 --out=hack --overwrite"  

```


./表示当前路径
Myexe ：exe应用的名称
platform: 打包平台 darwin, linux, mas, win32或者选择all
arch: 可选 ia32, x64, armv7l, arm64或者选择all
electron-version： electron的版本（）
out：生成的exe保存目录
overwrite:使用了这个参数，每次打包就不用把原来exe删除，可直接覆盖了。

- 运行

```
npm run-script packager

```

::: tip 参考

https://blog.csdn.net/qq_35057009/article/details/89638688


:::