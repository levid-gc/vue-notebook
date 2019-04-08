# 数据绑定

数据绑定连接了组件数据和模板中的 HTML 元素。它使得 Vue.js 应用具有了交互性，用户执行的操作能够修改应用的状态，而状态的改变又通过数据绑定反馈给了用户。文本插值是最简单的一种绑定形式，它通过使用两个配对的花括号来创建， `{{` 和 `}}`，这常常又被称之为**胡子绑定（mustache binding）**。

## 组件元素

组件是 Vue.js 应用的主要构建块。组件通常定义在 `*.vue` 文件中，当中包含了展示给用户的 HTML 内容，支撑内容的数据和 JavaScript 代码，以及 CSS 样式。组件由三种元素定义：`template`, `script`, `style` 元素。

### 模版

`template` 元素包含的是组件的 HTML 内容。模版中包含一个顶级元素，用于替换应用组件的元素。当中混合了常规的 HTML 元素，数据绑定，指令，以及自定义的组件元素。

### 脚本

`script` 元素包含的是组件的 JavaScript 模块。配置了组件的属性，定义了它的数据模型，提供支撑特性的逻辑。

### 样式

`style` 元素定义的是 CSS 样式。应用于 `template` 元素或更广的范围。并不是所有的组件都需要它们自己的 CSS 样式，

## 数据展示

数据绑定中实用全局对象和函数：

| 名称       | 描述                                                         |
| ---------- | ------------------------------------------------------------ |
| parseFloat | 解析浮点数据值的函数。                                       |
| parseInt   | 解析整型数据值的函数。                                       |
| Math       | 提供数学函数的对象。                                         |
| Number     | 提供处理数值类型方法的对象。                                 |
| Date       | 提供处理时间类型方法的对象。                                 |
| Array      | 提供处理数组类型方法的对象。                                 |
| Object     | 提供处理对象类型方法的对象。                                 |
| String     | 提供处理字符串类型方法的对象。                               |
| RegExp     | 用于处理正则表达式的对象。                                   |
| Map        | 用于表示键值对集合的对象。                                   |
| Set        | 用于表示唯一值集合的对象                                     |
| JSON       | 用于序列化/反序列化 JSON 数据的对象。                        |
| Intl       | 用于本地化处理的对象，详见 [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl)。 |
