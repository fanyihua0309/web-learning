**应用程序接口（Application Programming Interfaces**（**API**））

API 是已经建立好的一套代码组件，可以让开发者实现原本很难甚至无法实现的程序。

API 通常分为两类。

**浏览器 API** 内建于 web 浏览器中，它们可以将数据从周边计算机环境中筛选出来，还可以做实用的复杂工作。

​		其中一种是：`文档对象模型 API（DOM（Document Object Model）API）`能通过创建、移除和修改 HTML，为页面动态应用新样式等手段来操作 HTML 和 CSS。比如当某个页面出现了一个弹窗，或者显示了一些新内容（像上文小 demo 中看到那样），这就是 DOM 在运行。JavaScript 最普遍的用处是通过 DOM API动态修改 HTML 和 CSS 来更新用户界面。

**第三方 API** 并没有默认嵌入浏览器中，一般要从网上取得它们的代码和信息。



HTML引入外部js文件

```
<script src="script.js" async></script>
```

（`async` “异步”属性）告知浏览器在遇到 `<script>` 元素时不要中断后续 HTML 内容的加载。

脚本调用策略小结：

- 如果脚本无需等待页面解析，且无依赖独立运行，那么应使用 `async`。
- 如果脚本需要等待页面解析，且依赖于其它脚本，调用这些脚本时应使用 `defer`，将关联的脚本按所需顺序置于 HTML 中。



在 JavaScript 中，`true && expression` 总是会返回 `expression`, 而 `false && expression` 总是会返回 `false`。因此，如果条件是 `true`，`&&` 右侧的元素就会被渲染，如果是 `false`，React 会忽略并跳过它。

元素的 key 只有放在就近的数组上下文中才有意义。

比方说，如果你[提取](https://react.docschina.org/docs/components-and-props.html#extracting-components)出一个 `ListItem` 组件，你应该把 key 保留在数组中的这个 `<ListItem />` 元素上，而不是放在 `ListItem` 组件中的 `<li>` 元素上。

在 `map()` 方法中的元素需要设置 key 属性。

key 会传递信息给 React ，但不会传递给你的组件。

### 