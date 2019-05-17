### 开发日志
* 20150629 tr 设置了border无效
* 解决方案：table设置 border-collapse 为collapse, border-collapse属性设置表格的边框是否被合并为一个单一的边框，还是象在标准的 HTML 中那样分开显示。
* 20150712 给canvas标签添加控制宽高的样式后，绘制出来的宽高会异常；
* 解决方案： 不用样式控制宽高，使用属性控制之。
* 20150714 canvas context.translate 改动后会将设置保存在内存中（下次获取 该元素的context位置还是translate后的）
* 解决方案： 使用完后将位置变回去， es： context(100, 100); afater used: context(-100, -100);
* 20150721 canvas ctx.getImageData方法： 读取图像文件需要tomcat服务器环境
* 20150724 canvas ctx.globalCompositeOperation 作用区间是整个canvas画布，演示所有参数得使用ctx.createPattern在画布上绘制画布。
* 解决方案： 新生成一个canvas节点， 然后在这个节点操作合成。
* 20150831 编码风格： 文件夹使用驼峰命名法，如：flashDemo， 文件蛇形命名方式，例如：exam_questions.md；
* 2015年9月25日 开始维护请假同事代码，研究其代码风格编写博文代码：vue/vue_vs_jquery.html中脚本实现。
* 2015-10-16 vue.js 如何实现新增表单操作（在不操作dom的情况下）， 思考如何VUE 完成 jq实现中
* 解决方案：从样式上解决，正常文档流布局display:inline-block; text-align:justify; 两端对齐
* 2015-11-9 滚动条代码优化,前端实现自动滚动（每隔5秒向上滚动）效果，只有滚动条数大于2时滚动；鼠标放置上面停止滚动，移开继续滚动；
* 优化方案：
* 1.在 操作dom时 隐藏， 操作完后出现；
* 2. dom 动画 脱离文档流，使用 position: absolute; fixed;等
* 3.尽量少 获取导致 回流（reflow）的全局样式值， 例如 offsetTop(left Height Width)  top left;  
* 2015-11-16 浏览器缓存方案总结: 2015，研究IE使用 userData模拟localStorage方案；

* 2016-09-06 [gulp-sass](https://www.npmjs.com/package/gulp-sass)(不依赖ruby环境使用sass) 学习，[gulp-rev-collector](https://www.npmjs.com/package/gulp-rev-collector)(前端去除缓存)学习;
* [gulp 组合任务顺序执行](http://zhangruojun.com/gulpshun-xu-zhi-xing-ren-wu/)
* 2016-11-16 gulp-sprite 学习，本项目文件结构迁移：将 gulp 依赖包上移至顶级目录；

* 2016-12-02  DOM节点信息包括节点类型（nodeType）、节点名称（nodeName）和节点值（nodeValue）；
* 2016-12-04 在gitHub上使用了gh-pages分支后就可以使用浏览器访问该项目（相当于放置服务器内容了）；
* 2017-06-29 后续研究： 1.字体图标实践+博文； 2.mock学习；
* 2017-07-18 gitHub演示地址： wteam-xq.github.io/testDemo/index.html；

* 2018-04-14 目前工程依赖包越来越大，需要整理项目依赖包， 将依赖包分散到各自Demo文件夹内， 
* 例如: gulp 相关依赖包放置gulp文件夹， webpack 相关依赖包放置 webpack文件夹；
* 另： 所有依赖包需要升级到兼容node 8.x;

* 2018-12-25 确定基本编码规范 - 格式化： 不使用规范文档限制， 不使用编辑器插件扩展， 不使用node扩展运行检查实现；
直接vscode编辑器(后续可换成更前卫的主流编辑器)默认格式化快键键格式化代码；代码检查后续可使用编辑器插件自动检查；

```
"engines": {
  "node": ">=8.9.0"
},
```
* 待添加： CSS 渲染原理， 解析原理；

### 遗留bug:
1.项目中 IE8下，弹出层bug无法重现；（challenge_case/IE8_position）
2.IE7 中（模拟）使用json2.js 堆栈溢出报错；
