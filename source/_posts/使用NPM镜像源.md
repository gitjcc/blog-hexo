title: 使用 NPM 镜像源
---

由于一些原因，国内访问国外 Internet 并不是那么顺畅。虽然对程序员来说，会访问国外 Internet 是基本素质，但有的时候也会遇到不容易跨过去的沟沟坎坎。比如 NPM 安装项目依赖包的时候，有些包（比如 node-sass, electron）需要另行下载额外的文件，这些文件大都是托管在 Amazon 的 AWS 上，安装成功的几率很低。好在国内有镜像（感谢国内提供开源镜像的公司和机构），只需要把源改到国内镜像，就可以解决这个问题，同时大大提升各种包的安装速度。

以修改 .npmrc 文件，将 NPM 源改为淘宝镜像源为例。

## .npmrc文件

``` bash
registry=https://registry.npm.taobao.org

NVM_NODEJS_ORG_MIRROR=http://npm.taobao.org/mirrors/node/
disturl=https://npm.taobao.org/dist    ; node/dist

phantomjs_cdnurl=http://npm.taobao.org/mirrors/phantomjs
chromedriver_cdnurl=http://npm.taobao.org/mirrors/chromedriver
operadriver_cdnurl=http://npm.taobao.org/mirrors/operadriver

ELECTRON_MIRROR=http://npm.taobao.org/mirrors/electron/

SASS_BINARY_SITE=http://npm.taobao.org/mirrors/node-sass/

NWJS_URLBASE=http://npm.taobao.org/mirrors/nwjs/v
```

## Reference & Further Reading

[淘宝NPM镜像](https://npm.taobao.org/mirrors)

[npmrc](https://docs.npmjs.com/files/npmrc)

[npm-config](https://docs.npmjs.com/misc/config)

[package.json](https://docs.npmjs.com/files/package.json)

[NPM](https://docs.npmjs.com/cli/npm)