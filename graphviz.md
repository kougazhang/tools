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

+ 语法: https://leojhonsong.github.io/zh-CN/2020/03/12/Graphviz%E7%AE%80%E8%A6%81%E8%AF%AD%E6%B3%95/

+ 为组件加注释 `xlabel`

`record` 画格子:

```
digraph G {
  
  // node [shape=record] 表示要画格子
  node [shape=record];
  
  // label 内的内容会变成一系列小格子
  // <f0> 是小格子的命名
  // memory:f0 表示 memory 组件里的 f0
  memory [label="<f0> 56014|<f1> 56015|<f2> 56016|<f3> 56017|<f4> 56018|<f5> 56019|<f6> 56020|<f7> 56021", xlabel="机器地址"];
  array[label="<f0> dates[0]|<f1> dates[1]|<f2> dates[2]|<f3> dates[3]", xlabel="数组元素"];
  
  memory:f0 -> array:f0;
  memory:f1 -> array:f0;
  memory:f2 -> array:f1;
  memory:f3 -> array:f1;
  memory:f4 -> array:f2;
  memory:f5 -> array:f2;
  memory:f6 -> array:f3;
  memory:f7 -> array:f3;
}
```



