title: NW.js 安装
---

## 背景

最近公司的 electron 桌面应用有了兼容 windows xp 系统的需求，决定用 NW.js 的 v0.14.7 版本来重新实现一下。然而第一步安装 NW.js 就受阻了。

经过若干次的安装失败和仅有的两次安装成功（狗屎运，在家安装两次都成功了，以为公司网有问题），最终找到合适的解决方案。

主要原因 NW.js 的 NPM 包没有包括所有文件，部分文件需要另行下载。而这些文件都是托管在 Amazon 的 AWS 上的。由于 GFW 的存在，国内直接访问 AWS 很困难，用 VPN 访问也困难。

## 解决方案

### 1、更改 nwjs_urlbase，使用国内镜像，比如淘宝镜像。

> nwjs_urlbase=http://npm.taobao.org/mirrors/nwjs/v

### 2、更改 nwjs_urlbase，使用离线包。

使用离线包安装，需要将离线包放在版本号文件夹下，比如 somewhere/v0.14.7/xx.zip。

> nwjs_urlbase=file:///home/somewhere/v

> nwjs_urlbase=file://D:/somewhere/v

> nwjs_urlbase=http://localhost:5399/somewhere/v

### 3、直接解压离线包。

先用 NPM 安装 nwjs，失败后（或在安装到运行 Node install.js 时手动放弃）将下载的 NW.js SDK 压缩包解压到对应的 node_modules\nw\nwjs 文件夹下。（注意包的完整性，作者使用 Chrome 浏览器在 AWS 下载的若干个包都是不完整的，最后用迅雷才下载到完整的包）

### 备注

由于 NWjs 的 install.js 会从 urlBase(nwjs_urlbase) + version(0.14.7) 路径寻找安装文件。

- 如果离线安装只要路径与 urlBase(nwjs_urlbase) + version(比如'0.14.7') 相同即可。
- 如果淘宝镜像安装，其资源的路径是 v0.14.7，所以 urlBase 最后要加上 'v'。
- 官方源会默认 urlBase=http://dl.nwjs.io/v。

## Reference & Further Reading

- [nwjs/npm-installer](https://github.com/nwjs/npm-installer)
- [淘宝 NPM 镜像](https://npm.taobao.org)