<!--
 * @Author: zhengyuan
 * @LastEditors: zhengyuan
 * @Description: file content
 * @Date: 2019-04-25 17:28:15
 * @LastEditTime: 2019-04-26 10:06:21
 -->
# ShouldUpdate

-   当数据发生变更，Store 扁平化地通知所有组件
-   框架默认使用 identical 比较新旧两份数据来决定是否需要刷新。
-   如果我们对组件的刷新会有非常精确化的诉求， 那么我们可以自己定义一个 ShouldUpdate。
-   示例代码

```dart
bool shouldUpdate(DetailState old, DetailState now) {
    return old.message != now.message;
}
```
---
<div style="width:100%;height:40px;">
    <a style="width:33%;float:left;" href="./Dependent-cn.md">Dependent</a>
    <a style="width:33%;float:left;text-align:center;" href="./Should-Update-cn.md">ShouldUpdate</a>
    <a style="width:33%;float:left;text-align:right;" href="./On-Error-cn.md">OnError</a>
</div>