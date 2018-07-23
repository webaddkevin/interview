## redux
1. 核心概念
 state 用来存储数据，你需要修改state只能发起一个action 
 reducer是用来联系action和state
2. 三大原则
单一数据源，整个应用的 state 被储存在一棵 object tree 中，并且这个 object tree 只存在于唯一一个 store 中。  
state是只读的只有触发action才能修改  
3. 使用纯函数来执行修改
