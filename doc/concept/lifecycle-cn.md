<!--
 * @Author: zhengyuan
 * @LastEditors: zhengyuan
 * @Description: file content
 * @Date: 2019-04-25 17:28:15
 * @LastEditTime: 2019-04-26 09:56:02
 -->
# Lifecycle

-   默认的所有生命周期，本质上都来自于 flutter State<StatefulWidget> 中的生命周期。
    -   initState
    -   didChangeDependencies
    -   build
    -   didUpdateWidget
    -   deactivate
    -   dispose
-   在组件内，Reducer 的生命周期是和页面一致的，Effect 和 View 的生命周期是和组件的 Widget 一致的。
-   在适配器中，Reducer 的生命周期是和页面一致的，Effect 的生命周期是和 ListView 的生命周期一致，View 的生命周期是短暂的(划入不可见区域即销毁)。同时增加了 appear 和 disappear 的生命周期， 代表这个 adapter 管理的视图数组，刚进入显示区和完全离开显示区的回调。


---
<div style="width:100%;height:40px;">
    <a style="width:33%;float:left;" href="./Higher-Effect-cn.md">HigherEffect</a>
    <a style="width:33%;float:left;text-align:center;" href="./Lifecycle-cn.md">Lifecycle</a>
    <a style="width:33%;float:left;text-align:right;" href="./Dependencies-cn.md">Dependencies</a>
</div>