categories: sass
title: Sass (Syntactically Awesome StyleSheets)
---

Sass 是对 CSS 的扩展，让 CSS 语言更强大、优雅。 它允许你使用变量、嵌套规则、 mixins、导入等众多功能， 并且完全兼容 CSS 语法。 Sass 有助于保持大型样式表结构良好， 同时也让你能够快速开始小型项目， 特别是在搭配 Compass 样式库一同使用时。

<!--more-->

## 特色
- 完全兼容 CSS3
- 在 CSS 语言基础上添加了扩展功能，比如变量、嵌套 (nesting)、混合 (mixin)
- 对颜色和其它值进行操作的{Sass::Script::Functions 函数}
- 函数库控制指令之类的高级功能
- 良好的格式，可对输出格式进行定制
- 支持 Firebug


## Sass 文件后缀名

sass 有两种后缀名文件：一种后缀名为 sass，不使用大括号和分号；另一种就是我们这里使用的 scss 文件，这种和我们平时写的 css 文件格式差不多，使用大括号和分号。本教程中所说的所有 sass 文件都指后缀名为 scss 的文件。在此也建议使用后缀名为 scss 的文件，以避免 sass 后缀名的严格格式要求报错。


## 使用变量;

sass让人们受益的一个重要特性就是它为css引入了变量。你可以把反复使用的css属性值 定义成变量，然后通过变量名来引用它们，而无需重复书写这一属性值。或者，对于仅使用过一 次的属性值，你可以赋予其一个易懂的变量名，让人一眼就知道这个属性值的用途。

sass使用$符号来标识变量(老版本的sass使用!来标识变量。改成$是多半因为!highlight-color看起来太丑了。)，比如$highlight-color和$sidebar-width。为什么选择$ 符号呢？因为它好认、更具美感，且在CSS中并无他用，不会导致与现存或未来的css语法冲突。







# 参考

## 参考链接

- [SASS用法指南](http://www.ruanyifeng.com/blog/2012/06/sass.html)
- [SASS中文文档](http://sass.bootcss.com/docs/sass-reference/)
- [Sass 基础教程](http://www.sasschina.com/guide/)