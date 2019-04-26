### WidgetWrapper

-   它用来解决 flutter 的 ui 体系下，一些需要实现特色接口的 Widget，比如 KeepAlive，因为通过 Component 产生的 Widget 会被一个框架内部的 Stateful 的 Widget 所包裹。
-   示例代码

```dart
import 'package:flutter/material.dart';

Widget repaintBoundaryWrapper(Widget widget) {
  return RepaintBoundary(child: widget);
}
```
---
<div style="width:100%;height:40px;">
    <a style="width:33%;float:left;" href="./OOP-cn.md">OOP</a>
    <a style="width:33%;float:left;text-align:center;" href="./Widget-Wrapper-cn.md">WidgetWrapper</a>
    <a style="width:33%;float:left;text-align:right;" href="./Page-cn.md">Page</a>
</div>