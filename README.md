## paging

原生JS写的一个很轻量级很简单的分页组件  

页码显示逻辑比较友好

嗯 是写的一个栗子 所以 木有多少复杂配置 (๑•̀ㅂ•́) ✧

### 演示

注意分页在右边 

[传送门](https://aolose.github.io/paging/index.html)


### 用法
```
/**
 * 初始化
 * onSizeOrCurrPageChangeCallBack 这个回调可以用于取后端数据啥的
 * data:{page:xxx,size:xxx}
 */
var instance = macPaging(selector,onSizeOrCurrPageChangeCallBack(data))
instance.render(config); // 不触发change事件渲染 config 选项 见下面
instance.change(); // 强制触发onSizeOrCurrPageChangeCallBack
instance.page++ // 下一页
instance.page-- // 上一页
instance.size= 100 // 设置size
instance.total = 1000 // 设置总数量 会改变总页数
instance.max = 22 // 设置总页数 会改变最大数量
```
##### config 
```
{
    page:1,      // 当前页
    max:10,      // 总页码
    total:999,   // 和max选一个就好 总数
    size:10      // 分页大小
}
```
