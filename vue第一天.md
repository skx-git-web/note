# 什么是vue?

 1. Vue是一个渐近式的javaScript框架

    渐近式：vue.js-->组件化--vue-router->vuex->构建工具webpack-->周边生态环境（element UI,mint ui,iview等）

 2. mvvm模式,mvc模式

```
    mvc:m:model(数据层)  v:view（视图层）c:controller(控制器)
    mvvm: m:model(数据层)  v:view（视图层） vm:viewmodel(视图模型)

```

 3.vue的核心特点：组件化，数据驱动，虚拟dom

  
 ```
    React:  this.setState()
    Vue:自动更新
    虚拟dom：本质上是一个JS对象，在内存中操作，提升性能

    把DOM结构映射为一个JS对象

 ```


```
 <div id="app" title="测试">
        hello
    </div>

```

映射成：

```
{
    tagName:'div',
    attr:{id:'app'，‘title’:'测试'}，
    children:[
        'text':'hello'
    ]

}

```



# vue实例


```
var vm=new Vue({
      el:'#app', //挂载点  相当于React中的ReactDOM.render(<App />,document.getElementById("app"))
      data:{  //数据源   相当于react中的this.state={  }
         msg:'vue.js',
         arr:['张三','李四','王五','马六'] 
      }
  });

```


# vue指令和修饰符

 常用指令：

 ```
   1. v-for:遍历  //相当于React中的map遍历
   2. v-if:判断
   3. v-show:
    
      注意：v-if和v-show区别？？看是否渲染dom结构

         v-show:切换频率高时用
         v-if:切换频率低时使用

   4.v-on:绑定事件  简称：@
   5.v-bind:绑定属性 简称：：
   6.v-model:双向绑定

   修饰符:

 ```