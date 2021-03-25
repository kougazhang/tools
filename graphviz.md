Graphviz 是用 dot 语言进行绘图的工具.

为什么使用 graphviz 绘图. 因为 graphviz 绘图能自动排版, 所以可以用来绘制关系非常复杂的图.

## QuickStart

**安装**

```
brew install graphviz
```

**入门例子**

编辑文本 `pic.dot`:

```
digraph pic { 
  Hello -> World
}
```

生成图片: `dot pic.dot -T png -o pic.png`

## dot 语法学习

+ https://blog.zengrong.net/post/graphviz-brief/