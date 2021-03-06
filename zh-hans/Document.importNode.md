TOPICS: Document.importNode
AUTHORS: mdn; mdn@mozilla-community.org; github:mdn

# `Document.importNode()`

将外部文档的一个节点拷贝一份,然后可以把这个拷贝的节点插入到当前文档中.

## 语法

```javascript
var node = document.importNode(externalNode, deep);
```

| 参数 | 说明 |
| :-- | :-- |
| `externalNode` | 将要从外部文档导入的节点. |
| `deep` 可选 | 一个布尔值,表明是否要导入节点的后代节点. |

!!! warn "注意"
    在DOM4规范中 (实现于Gecko 10.0 (Firefox 10.0 / Thunderbird 10.0 / SeaMonkey 2.7)) ,`deep`是个可选的参数. 如果省略不写,
    则使用默认值 `true`, 表示深度克隆. 如果你想使用浅克隆,则传入`false`参数.

在没有实现DOM4的浏览器中, 这个参数不可以省略.

## 示例

```javascript
var iframe = document.getElementsByTagName("iframe")[0];
var oldNode = iframe.contentDocument.getElementById("myNode");
var newNode = document.importNode(oldNode, true);
document.getElementById("container").appendChild(newNode);
```

## 备注

源节点不会从外部文档中删除,被导入的节点是源节点的一个拷贝.

将外部文档的节点插入当前文档之前,你必须使用 `document.importNode()` 从外部文档导入源节点,或者使用 `document.adoptNode()` 导入源节点, 想要了解更多的
`Node.ownerDocument` 问题,请参考 [W3C DOM FAQ](http://www.w3.org/DOM/faq.html#ownerdoc).

即使你不执行导入动作,就执行插入外部文档中的节点.Firefox目前也不会报错(如果严格按标准执行,很多已有的网站都无法正常运行). 我们鼓励开发者严格按标准修改自己已有的不符合上述标准的代码.
