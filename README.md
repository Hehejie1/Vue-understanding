# Vue-understanding
This is a self-understanding article of VueJs source code, the article contains detailed comments and code



## 1. 文件目录

├─two-way binding     # 解决了基本的数据双向绑定和部分事件
        ├─index.html
        ├─js
         |   └vue0.0.min.js   # 自己编译的vue模块



## 2. 原理

![Vue进行双向绑定的图示](https://www.wyjloveyl.com/hhImages/my/vue-binding.png)



>   MVVM。model,view,viewModel。其中数据(model)通过Object.defineProperty数据劫持监听get、set方法。Compile编译解析绑定更新函数Watcher添加到订阅。在数据的set方法改变时候通知Dep进行广播，通知所有watcher执行update操作更改视图。双向绑定就是数据更改和视图更改都被set方法监听通知Dep

