<!--
 * @Author: zhengyuan
 * @LastEditors: zhengyuan
 * @Description: file content
 * @Date: 2019-04-25 17:28:15
 * @LastEditTime: 2019-04-26 10:17:12
 -->
# Directory

推荐的目录结构会是这样

```
sample_page
    -- action.dart /// define action types and action creator
    -- page.dart /// config a page or component
    -- view.dart /// define a function which expresses the presentation of user interface
    -- effect.dart /// define a function which handles the side-effect
    -- reducer.dart /// define a function which handles state-change
    -- state.dart /// define a state and some connector of substate
    components
        sample_component
        -- action.dart
        -- component.dart
        -- view.dart
        -- effect.dart
        -- reducer.dart
        -- state.dart
```

上层负责组装，下层负责实现。

---
<div style="width:100%;height:40px;">
    <a style="width:33%;float:left;" href="./What's-connector.md">What's-connector</a>
    <a style="width:33%;float:left;text-align:center;" href="./Mechanism-cn.md">Mechanism</a>
    <a style="width:33%;float:left;text-align:right;" href="../introduction/README-cn.md">关于</a>
</div>