## vuex
### 核心概念
1. state  
单一状态树，每个应用只有一个状态树，便于管理和修改  
mapstate辅助函数获取状态树中的状态
2. getter  
Getter 会暴露为 store.getters 对象 或者mapGetters 辅助函数  
...mapGetters([
      'doneTodosCount',
      'anotherGetter',
      // ...
    ])  
    调用的时候this.doneTodosCount
3. mutation  
vuex中唯一修改state的方式就是提交mutation  
每个mutation都有事件类型和回调函数
一条重要的原则就是要记住 mutation 必须是同步函数
4. action  
Action 提交的是 mutation，而不是直接变更状态。  
Action 可以包含任意异步操作。  
Action接收一个context对象，对象提交mutation
5. module  
当状态树比较大的时候可以用module分模块，每个模块对于getter，mutation,action,state
