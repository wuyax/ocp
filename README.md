# Order the CSS properties

CSS属性排序规则

## 在VSCode中使用
1. 下载本项目中的`.csscomb.js`，放在项目根目录；
2. 下载VSCode插件 [CSScomb](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-csscomb)
3. 在编辑器中按`F1`，搜索`CSScomb`，按下`enter`键即完成`CSS`代码格式化

本项目提供一个非常细致的CSS属性排序规则，`.csscomb.json` 是[CSScomb](http://csscomb.com/) 的配置文件，你有很多方法来使用它，我推荐使用VSCode插件来使用，更多的使用方式可以访问[CSScomb文档](https://github.com/csscomb/csscomb.js)

## CSS属性顺序
   1. 影响文档流的属性（比如：display, position, float, clear, visibility, table-layout等） 
   2. 自身盒模型的属性（比如：width, height, margin, padding, border等） 
   3. 排版相关属性（比如：font, line-height, text-align, text-indent, vertical-align等等） 
   4. 装饰性属性（比如：color, background, opacity, cursor等） 
   5. 生成内容的属性（比如：content, list-style, quotes等） 

## 贡献
如果你有更好的建议或者对规则列表的补充欢迎提交PR。