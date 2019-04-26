<!--
 * @Author: zhengyuan
 * @LastEditors: zhengyuan
 * @Description: file content
 * @Date: 2019-04-25 17:28:15
 * @LastEditTime: 2019-04-26 10:06:52
 -->
# OnError

-   集中处理由 Effect 产生的业务异常，无论是同步函数还是异步函数。有了统一的异常处理机制，我们就能站在一个更高的抽象角度，对业务代码做出合理的简化。
-   示例代码

```dart
bool onMessageError(Exception e, Context<String> ctx) {
    if(e is BizException) {
        ///do some toast
        return true;
    }
    return false;
}

class MessageComponent extends Component<String> {
    MessageComponent(): super(
            view: buildMessageView,
            effect: buildEffect(),
            reducer: buildMessageReducer(),
            onError: onMessageError,
        );
}
```
---
<div style="width:100%;height:40px;">
    <a style="width:33%;float:left;" href="./Should-Update-cn.md">ShouldUpdate</a>
    <a style="width:33%;float:left;text-align:center;" href="./On-Error-cn.md">OnError</a>
    <a style="width:33%;float:left;text-align:right;"href="./Filter-cn.md">Filter</a>
</div>