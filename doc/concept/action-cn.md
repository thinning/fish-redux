<!--
 * @Author: zhengyuan
 * @LastEditors: zhengyuan
 * @Description: file content
 * @Date: 2019-04-25 17:28:15
 * @LastEditTime: 2019-04-26 10:24:40
 -->
# Action

-   Action 包含两个字段
    -   type
    -   payload
-   推荐的写法是
    -   为一个组件|适配器创建一个 action.dart 文件，包含两个类
        -   为 type 字段起一个枚举类
        -   为 Action 的创建起一个 ActionCreator 类，这样利于约束 payload 的类型。
    -   Effect 接受处理的 Action，以 on{Verb} 命名
    -   Reducer 接受处理的 Action，以{verb} 命名
    -   示例代码

```dart
enum MessageAction {
    onShare,
    shared,
}

class MessageActionCreator {
    static Action onShare(Map<String, Object> payload) {
        return Action(MessageAction.onShare, payload: payload);
    }

    static Action shared() {
        return const Action(MessageAction.shared);
    }
}
```

---
<div style="width:100%;height:40px;">
    <a style="width:33%;float:left;" href="./Redux-cn.md">Redux</a>
    <a style="width:33%;float:left;text-align:center;" href="./Action-cn.md">Action</a>
    <a style="width:33%;float:left;text-align:right;" href="./Connector-cn.md">Connector</a>
</div>