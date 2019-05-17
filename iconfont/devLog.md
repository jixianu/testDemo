### 学习日志
[阿里巴巴矢量图标库](http://www.iconfont.cn/home/index)
[图标字体化浅谈](http://isux.tencent.com/icon-font.html)
[真正了解CSS3背景下的@font face规则](http://www.zhangxinxu.com/wordpress/2017/03/css3-font-face-src-local/)
[字蛛-中文字体压缩器](http://font-spider.org/)

* 2017-07-12 目录创建；
* 图标字体  研究实践分享；
* 1.使用场景；
* 2.目前业内 使用方案；
* 3.实践 过程中遇到的问题、及其解决方案；

* 2017-07-13 小米官网、阿里巴巴矢量图标库 的图标字体实现方式还得观察！
* 2017-07-14 小米官网、阿里巴巴矢量图标库 的图标字体 实现方式都是 兼容性最好的 unicode方式；
* 图标字体实现方式有3：
* 1.unicode 兼容性最好、不支持多色图标；
* 2.font-class ie8+、书写直观 也不支持多色图标；（原理是使用伪类:before，bootstrap的图标字体就是这种实现）
* 3.symbol ie9+、 支持多色图标； （原理是使用svg集合）

* 2017-07-17 按照图标字体开发流程， 生成自定义小图标；
* 预计demo功能： 三个小图标：笑脸、黑脸、帽子； 默认显示笑脸+帽子，鼠标hover，变成黑脸+帽子（颜色变绿）；
* 2017-07-20 demo中的图标字体尝试变成 base64 样式中存放图标字体源文件；
* 方式一：使用[在线工具网页](http://www.css-js.com/tools/base64.html) 完成图标字体转base64；(方便、限制100K)
* 方式二：使用[gulp扩展工具](http://www.w3cplus.com/workflow/gulp-tutorial-7-base64.html)本地完成图标字体转base64；
