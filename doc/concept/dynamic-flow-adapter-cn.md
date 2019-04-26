<!--
 * @Author: zhengyuan
 * @LastEditors: zhengyuan
 * @Description: file content
 * @Date: 2019-04-25 17:28:15
 * @LastEditTime: 2019-04-26 10:10:44
 -->
# DynamicFlowAdapter

-   模版是一个 Map，接受一个数组类型的数据驱动
-   示例代码

```dart
class RecommendAdapter extends DynamicFlowAdapter<RecommendState> {
    RecommendAdapter()
        : super(
            pool: <String, Component<Object>>{
                'card_0': RecommendTitleComponent(),
                'card_1': RecommendRowComponent(),
            },
            connector: RecommendCardListConnector(),
        );
}
```
<img src="https://img.alicdn.com/tfs/TB10lxHLMDqK1RjSZSyXXaxEVXa-1838-1024.png" width="919px" height="512px">

---
<div style="width:100%;height:40px;">
    <a style="width:33%;float:left;" href="./Static-Flow-Adapter-cn.md">StaticFlowAdapter</a>
    <a style="width:33%;float:left;text-align:center;" href="./Dynamic-Flow-Adapter-cn.md">DynamicFlowAdapter</a>
    <a style="width:33%;float:left;text-align:right;" href="./Custom-Adapter-cn.md">CustomAdapter</a>
</div>