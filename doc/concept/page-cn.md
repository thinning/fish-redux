<!--
 * @Author: zhengyuan
 * @LastEditors: zhengyuan
 * @Description: file content
 * @Date: 2019-04-25 17:28:15
 * @LastEditTime: 2019-04-26 10:25:00
 -->
# Page

-   一个页面内都有且仅有一个 Store
-   Page 继承于 Component，所以它能配置所有 Component 的要素
-   Page 能配置 Middleware，用于对 Redux 做 AOP 管理
-   Page 必须配置一个初始化页面数据的初始化函数  initState
    <img src="https://img.alicdn.com/tfs/TB1ASfDJ9zqK1RjSZFHXXb3CpXa-1636-756.png" width="818px" height="378px">

-   示例代码

```dart
/// Hello World
class HelloWordPage extends Page<String, String> {
    HelloWordPage():
        super(
            initState: (String msg) => msg,
            view:(String msg, _, __) => Text('Hello ${msg}'),
        );
}

HelloWordPage().buildPage('world')
```
---
<div style="width:100%;height:40px;">
    <a style="width:33%;float:left;" href="./Widget-Wrapper-cn.md">WidgetWrapper</a>
    <a style="width:33%;float:left;text-align:center;" href="./Page-cn.md">Page</a>
    <a style="width:33%;float:left;text-align:right;" href="./Adapter-cn.md">Adapter</a>
</div>