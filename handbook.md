https://medium.freecodecamp.org/the-complete-javascript-handbook-f26b2c71719c

JavaScript是世界上最流行的编程语言之一，同时在浏览器之外的领域也有广泛的应用。最近几年Node.js的兴起解锁了后端编程-曾经Java,Ruby,Python,PHP以及其他后端编程语言的领域。

本文 "JavaScript Handbook" 遵循80/20原则：花20%的时间学习80%的JavaScript

来学习你所需要的JavaScript相关知识吧！

索引列表
- ECMAscript
- ES6
- ES2016
- ES2017
- ES2018
- Coding Style
- Lexical Structure
- Variables
- Types
- Expressions
- Prototypal Inheritance
- Classes
- Exceptions
- Semicolons
- Quotes
- Template Literals
- Functions
- Arrow Functions
- Closures
- Arrays
- Loops
- Events
- The Event Loop
- Asynchronous Programming and Callbacks
- Promises
- Async and Await
- Loops and Scope
- Timers
- This
- Strict Mode
- Immediately-Invoked Function Expressions (IFFE’s)
- Math Operators
- The Math Object
- ES modules
- CommonJS
- Glossary

#前言
JavaScript是世界上最流行的语言之一。20年前面世，在低调地开头之后走过了很长的一段路。

作为第一个，同时也是唯一的浏览器原生支持的脚本语言，它太糟糕了（译者注:原文是"stuck"卡住的意思，目测是手滑了，应该是"suck"）。

最初的时候，它并不像今天这样强大，它只是为了做酷炫的动画和`the marvel known at the time as ` 动态Html(DHTML)

当对于网页端的需求不断扩大时，JavaScript也有义务去成长，来适应世界上最大生态圈的需求。

平台上增加了很多新的东西，比如浏览器API，语言本身也成长了很多。

现在JavaScript在浏览器之外也成长了很多。过去几年Node.js的兴起解锁了后端开发，一个曾经由Java,Ruby,Python,PHP以及其他传统后端编程语言主宰的领域。

JavaScript现在也可以增强数据库和其他很多应用。它甚至可以开发嵌入式应用，移动端应用，电视端应用以及更多。一个由浏览器内嵌的小语言现在成长为世界上最流行的语言。

#JavaScript的基础定义
JavaScript是一个有如下特征的编程语言：
（译者注：当然这不是JavaScript特有的，比如Python也有如下特性）
- **高级语言**: 提供了抽象性让你可以忽略运行机器的细节。自动管理内存以及垃圾回收机制，所以你可以更专注于代码本身而不是管理内存地址，提供许多contructs??让你使用功能强大的变量和对象。
- **动态**: 对立于静态编程语言, 一个动态语言在运行时做很多静态语言在编译时。这样有很多优缺点，同时提供许多强大的功能例如动态类型，懒绑定，映射，函数式编程，对象运行中修改，闭包以及更多
- **动态类型**: 一个变量不强行规定成一个类型。你可以重新赋值一个变量到另一个类型，比如给一个字符串变量赋值一个整数。
- **弱类型**: 对立于强类型，弱类型语言不规定对象的类型。这样允许更多的变通性但是阻碍了类型安全和类型检查（TypeScript和Flow注重于强化这点）
- **解释型**: 经常说的解释型语言，意思为运行前不需要编译阶段的语言，对立于C,Java,Go等。实际上浏览器为了性能还是会在编译前进行编译的，但是这是透明的因为并没有额外一步。
- **多种范式(paradigm)**: 不像例如Java那样的推崇面向对象编程，或者C那样的面向步骤编程，这个语言并没有强行规定某一种编程理念。你可以用新的语法(从ES6开始)进行面向对象编程。你也可以通过头等函数(frist-class function)进行函数式编程，或者甚至像C那样的面向步骤编程。

万一你在想的话, **JavaScript和Java完全没有关系**, 这只是一个非常不幸的名字选择并且这么流传下来了

#JavaScript版本
首先让我介绍一下这个单词**ECMAScript**。我们有专门关于ECMAScript的介绍你可以深入阅读，但是现在你仅仅需要知道ECMAScript（也叫做ES）是JavaScript标准的名字。

JavaScript是那个标准的一种实现。所以你一只听到 ES6,ES2015,ES2016,ES2017,ES2018等等。

在很长时间里，大部分浏览器运行的JavaScript版本是ECMAScript3。版本4因为功能地狱而取消了(他们尝试一次加入太多的功能了)。ES5是JavaScript的一个大版本, ES2015(也叫做ES6)也是。

从那以后，核心人员决定每年做一次发布来避免版本之间等待太久，同时也缩短反馈周期。

现在最新通过的JavaScript版本是ES2017
（译者注: 原文发布于2018年10月30日）

#ECMASCRIPT
每当你读到JavaScript的时候你都不可避免地遇到以下术语:
- ES3
- ES5
- ES6
- ES7
- ES8
- ES2015
- ES2016
- ES2017
- ECMAScript 2017
- ECMAScript 2016
- ECMAScript 2015

他们都代表什么呢？

他们都代表一个**标准**，叫做ECMAScript.

ECMAScript是**JavaScript所遵循的一个标准**，很多时候缩写为**ES**.

除了JavaScript，还有其他语言实现了ECMAScript，包括：
- *ActionScript* (Flash脚本语言)因为Flash将在2020年被官方中断所以现在正在走下坡路。
- *JScript* (微软脚本语言) 因为当时JavaScript只被网景(Netscape)支持而且正是浏览器争霸的火热时期，所以微软为IE打造了他们自己的版本


当然，JavaScript是**最受欢迎**和广泛使用的ES实现。

为什么这个名字这么怪？`Ecma International`是一个瑞士的组织，他们负责定义国际标准。

当JavaScript被创造的时候，网景(Netscape)和Sun Microsystems把它呈现给Ecma然后他们命名为ECMA-262别名**ECMAScript**

[网景和Sun Microsystems的这篇出版](https://web.archive.org/web/20070916144913/http://wp.netscape.com/newsref/pr/newsrelease67.html)可能对解释名字选择有些帮助，[根据wiki](https://en.wikipedia.org/wiki/ECMAScript)可能包括和微软相关法律和品牌问题。

IE9之后，微软不再把他们浏览器的ES支持称为JScript并且开始称之为JavaScrit(至少我没再发现任何对它的饮用)

至201x，唯一流行的支持ECMAScript的语言是JavaScript.

#当前ECMAScript版本
当前ECMAScirpt版本是ES2018。发布于2018年6月。

#下一个版本什么时候发布？
从过往经验来看，JavaScript的修改在夏季的时候被标准化，所以我们可以期待**ECMAScript 2019**在2019年夏天发布，当然这是只是推断。

#TC39是什么
TC39是进化JavaScrpt的委员会。

TC39的成员是跟JavaScript有紧密关系的公司和浏览器提供方，包括Mollia，谷歌，脸书(Facebook)，苹果，微软，英特尔，PayPal, SalesForce等等。

每一个版本的提议都要经过几个阶段，[这里有详细解释](https://tc39.github.io/process-document/)

#ES版本
ES版本号有时候用年份有时候用升序版号表示让我感觉很困惑。

ES2015之前，ECMAScript标准一般用升序版号。所以ES5是2009年发布的ECMAScript标准的更新的官方名称。

为什么会这样呢？往ES2105演进的过程中，名称由ES6改成了ES2015，但是因为慢了一步，所以大家还称之为ES6，社区也没有扔下升序编号 - *全世界还是用生序编号来命名ES的发布*

这个表格应该能解释清楚其中关系：

TODO image

ES.Next是代表下一个版本的JavaScript的名字。

在我写下这些的时候，ES9已经被发布了，并且**ES.Next是ES10**

#ES6的修正
ECMAScript2015, 也叫做ES6, 是ECMAScript的一个基础版本。

**发布于最新的标准版本之后的4年**，ECMAScript 5.1，也是从升序版本号到年份版本号的切换开关。

所以**它不应该被称为ES6**(尽管大家都如此称呼它)而是ES2015。

从1999年到2009年ES5打造了整整10年，并且它是一个基础并且非常重要的版本。现在已经过去了那么多时间所以去谈ES5之前的代码如何运行已经没有价值了。

