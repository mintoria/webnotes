# redux
- 概述

###### react-redux=>vue-vuex

###### react全局状态管理

###### 容器->存储数据

###### 一致化应用

###### js state类型增多

- 三大核心

  - 单一数据源头
  - state只读：改变state需要触发一个action
  - 纯函数执行修改，action改变state tree 需要编写reducers（纯函数：可复用）
> 总结：
1. redux是一个js容器，全局状态管理
2. 三大核心

- 组成
    - state状态

    DomainDate：服务端数据

    UiState：当前UI组件决定展示的状态

    App State：App级别的状态，比如：当前是否请求loading
    

```
graph LR
A2[Component] -- store.dispatch:发送一个action --- B2[Store] 
```

- Action
1. 只描述了有事情要发生，并没有描述如何去更新
2. 必须有type属性（没有会报错）
3. 一般用创建action函数
4. 本质是js对象
- Reducer
1. 函数，参数为action和state ：return的值给store
2. 必须有返回值给store（不会报错，但store不会接收到值）
- Store
1. 维持应用的state
2. getState（）获取state
3. dispatch（）发送action
4. subscribe（）注册监听，通过返回值注销监听：组件加载完毕时监听（componentDidMount）
5. 关联action和reducer
> import {createStore} from "redux";

> const store = createStore(传递reducer);











    
    
    
    

