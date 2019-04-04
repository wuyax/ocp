# Order the CSS properties

CSS属性排序规则

## 在VSCode中使用
1. 下载本项目中的`.csscomb.js`，放在项目根目录；
2. 下载VSCode插件 [CSScomb](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-csscomb)
3. 在编辑器中按`F1`，搜索`CSScomb`，按下`enter`键即完成`CSS`代码格式化

本项目提供一个非常细致的CSS属性排序规则，`.csscomb.json` 是[CSScomb](http://csscomb.com/) 的配置文件，你有很多方法来使用它，我推荐使用VSCode插件来使用，更多的使用方式可以访问[CSScomb文档](https://github.com/csscomb/csscomb.js)

## 为什么要给CSS属性排序
  给CSS属性排序是一个各执己见的问题，很多人觉得没必要，但是统计结果却不这么认为:
  ![img](./resource/orgchart.png)
  
  在一份调查中有45%的人认为应该按照类型来给CSS属性分组和排序，我当然也是其中之一。

## CSS属性顺序
  1. 影响文档流的属性（比如：display, position, float, clear, visibility, table-layout等） 
  2. 自身盒模型的属性（比如：width, height, margin, padding, border等） 
  3. 排版相关属性（比如：font, line-height, text-align, text-indent, vertical-align等等） 
  4. 装饰性属性（比如：color, background, opacity, cursor等） 
  5. 生成内容的属性（比如：content, list-style, quotes等） 

## 关于CSS中的下划线
  1. `_`符号在 **CSS Hack** 年代有这[特殊的作用](http://www.zui88.com/blog/view-336.html)；
  2. `_`在 `JS` 中表示用户自定义的属性；
  3. 有人测试了其它的字符作为CSS中的连字符，结果除了`-`之外都失败了，你可以戳这个链接查看结果[test css hyphen](https://codepen.io/wuyax/pen/pYOpGK);
  4. 因此，我本在CSS class的命名中强烈建议只使用 `-`

## CSS编写规则
  1. 避免使用`html`标签作为`css`选择器；
  2. 不要使用id选择器，[When using IDs can be a pain in the class...](https://csswizardry.com/2011/09/when-using-ids-can-be-a-pain-in-the-class/)
  3. 在使用属性简写的时候你要清楚你在做什么，否则请使用完整的属性名。比如`line-height:30px;font:12px Arial;`这两行代码会得到和你想的不一样的结果。
  4. 慎用`margin-top`，尽量使用`padding-top`或者`margin-bottom`来解决，如果你非要使用，务必注意**外变局重叠问题**，一般加一个`.clearfix`(全局引入了该类的情况下)
  5. 慎用`!improtant`，除了要去覆盖用JS设置的样式外，你还用`!important`就是偷懒！，当然JS设置的样式也能用哪个JS更改，因此，完可以避免使用`!important`。如果非得要用，那么写下注释，告诉别人是为了解决什么问题！

## 参考链接
[Poll Results: How do you order your CSS properties?](https://css-tricks.com/poll-results-how-do-you-order-your-css-properties/)

[idiomatic-css](https://github.com/necolas/idiomatic-css/tree/master/translations/zh-CN)

[Ordering CSS3 Properties](https://css-tricks.com/ordering-css3-properties/)

[Dropbox (S)CSS Style Guide](https://github.com/dropbox/css-style-guide)

## 贡献
如果你有更好的建议或者对规则列表的补充欢迎提交PR。