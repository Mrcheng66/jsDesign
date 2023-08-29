1.虽然 JavaScript 和 ECMAScript 基本上是同义词，但 JavaScript 远远不限于 ECMA-262 所定义的那样。完整的 JavaScript 实现包含以下几个部分

核心（ECMAScript）
文档对象模型（DOM）
浏览器对象模型（BOM）

1.1 ECMAScript
ECMAScript，即 ECMA-262 定义的语言，并不局限于 Web 浏览器。事实上，这门语言没有输入和
输出之类的方法。ECMA-262 将这门语言作为一个基准来定义，以便在它之上再构建更稳健的脚本语言。

Web 浏览器只是 ECMAScript 实现可能存在的一种宿主环境（host environment）。宿主环境提供
ECMAScript 的基准实现和与环境自身交互必需的扩展。扩展。扩展（比如 DOM）使用 ECMAScript 核心类型
和语法，提供特定于环境的额外功能。其他宿主环境还有服务器端 JavaScript 平台 Node.js

如果不涉及浏览器的话，ECMA-262 到底定义了什么？在基本的层面，它描述这门语言的如下部分：
 语法
 类型
 语句
 关键字
 保留字
 操作符
 全局对象

1.2 DOM
文档对象模型（DOM，Document Object Model）是一个应用编程接口（API），用于在 HTML 中使
用扩展的 XML。DOM 将整个页面抽象为一组分层节点。HTML 或 XML 页面的每个组成部分都是一种
节点，包含不同的数据。

<html> 
 <head> 
 <title>Sample Page</title> 
 </head> 
 <body> 
 <p> Hello World!</p> 
 </body> 
</html>
1998 年 10 月，DOM Level 1 成为 W3C 的推荐标准。这个规范由两个模块组成：DOM Core 和 DOM HTML。前者提供了一种映射 XML 文档，从而方便访问和操作文档任意部分的方式；后者扩展了前者，
并增加了特定于 HTML 的对象和方法。

DOM Level 1 的目标是映射文档结构，而 DOM Level 2 的目标则宽泛得多。这个对最初 DOM 的扩
展增加了对（DHTML 早就支持的）鼠标和用户界面事件、范围、遍历（迭代 DOM 节点的方法）的支
持，而且通过对象接口支持了层叠样式表（CSS）。另外，DOM Level 1 中的 DOM Core 也被扩展以包含
对 XML 命名空间的支持。
DOM Level 2 新增了以下模块，以支持新的接口。
 DOM 视图：描述追踪文档不同视图（如应用 CSS 样式前后的文档）的接口。
 DOM 事件：描述事件及事件处理的接口。
 DOM 样式：描述处理元素 CSS 样式的接口。
 DOM 遍历和范围：描述遍历和操作 DOM 树的接口。

DOM Level 3 进一步扩展了 DOM，增加了以统一的方式加载和保存文档的方法（包含在一个叫 DOM
Load and Save 的新模块中），还有验证文档的方法（DOM Validation）。在 Level 3 中，DOM Core 经过扩
展支持了所有 XML 1.0 的特性，包括 XML Infoset、XPath 和 XML Base。

目前，W3C 不再按照 Level 来维护 DOM 了，而是作为 DOM Living Standard 来维护，其快照称为
DOM4。DOM4 新增的内容包括替代 Mutation Events 的 Mutation Observers。

1.3 BOM
IE3 和 Netscape Navigator 3 提供了浏览器对象模型（BOM） API，用于支持访问和操作浏览器的窗
口。使用 BOM，开发者可以操控浏览器显示页面之外的部分。

总体来说，BOM 主要针对浏览器窗口和子窗口（frame），不过人们通常会把任何特定于浏览器的
扩展都归在 BOM 的范畴内。比如，下面就是这样一些扩展：
 弹出新浏览器窗口的能力；
 移动、缩放和关闭浏览器窗口的能力；
 navigator 对象，提供关于浏览器的详尽信息；
 location 对象，提供浏览器加载页面的详尽信息；
 screen 对象，提供关于用户屏幕分辨率的详尽信息；
 performance 对象，提供浏览器内存占用、导航行为和时间统计的详尽信息；
 对 cookie 的支持；
 其他自定义对象，如 XMLHttpRequest 和 IE 的 ActiveXObject。
