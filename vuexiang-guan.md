## VUE {#vue-组件命名}

#### 1.尽量不要使用document.getElementById（‘xx’）/getElementByName\('xx'\)等获取元素的值

原因：执行该代码时，浏览器需要从头开始遍历DOM树，以找到相应的DOM节点进行更改，这个步骤非常耗时且产生不必要的计算。

#### 2.生命周期

vue的生命周期如下：

###### beforeCreate -&gt; created -&gt; beforeMount -&gt; Mounted -&gt; \( -&gt; beforeUpdate -&gt; updated \) -&gt; beforDestroy -&gt; destroyed

在生命周期函数里不要写过多表达式（如axios请求）或复杂的逻辑代码，应把该部分代码封装在methods或computed或watch

#### 3.组件



#### 4.axios

若重构代码，需要在axios做三件事, 可减少每个页面调用axios时重复的代码量

1.请求数据封装（无需在每个页面调用axios时重新封装请求数据）

2.统一捕获接口报错 （包括请求失败、错误码返回、账号别处登陆等错误）

3.如用户网络不佳导致等原因导致请求时间过长, 提供 加载中。。 等提示 （待商议）

