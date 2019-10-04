# learnvue
## 单页面程序

- Single Page Application 简称SPA

### 网站交互方式

- 经典的多页面

  - 用户体验一般，点击刷新跳转，等待时间过长
  - 每个页面都需要重新加载渲染，速度慢
  - 有利于SEO搜索引擎搜搜

- 现代式的单页面

  - 单页面应用程序的最主要的目的是为了让你的前后端开发能够分离

  - 开发方式好，前后端分离，开发效率高，可维护性好
    - 服务端不关心页面，只关心数据
    - 客户端不关心数据库及数据操作，只关心接口拿数据和服务端交互，处理页面

  - 用户体验好，就像一个原生的客户端软件一样，
  - 只需要加载渲染局部视图即可，不需要整页刷新
  - 单页面应用技术开发技术复杂，所以诞生了一堆的开发框架
    - Angular.js
    - React.js
    - Vue.js
  - 单页面技术虽然成熟，但是无法兼顾低版本浏览器
  - 单页面由于数据都是异步加载过来的，所以不会被搜索引擎搜索到，不利于SEO

### 多页面：以服务端为主导，前后端回合

- 前端人员也能接触到服务端代码，服务端的人也能接触到前端，管理起来非常混乱，代码提交容易发生冲突

  

### 单页面：前后端分离，各司其职

- 服务端只处理数据
- 前端只处理页面（两者通过接口来交互

### 模拟前后端分离开发模式

- 项目立项
- 需求分析
- 服务端的工作
  - 需求分析
  - 设计数据库
  - 接口设计（有时候也需要前端参与其中）
  - 接口（处理数据）开发
- 前端的工作
  - 需求分析
  - 写页面
  - 页面写好写功能
  - 通过接口和服务端进行交互


## 前端三大开发框架
  - 单页开发其实是比较复杂的，需要有一定的技术支撑
  - 所以有了我们现在需要学习的三大框架
  + angular
    - 09年诞生
    - Google
    - 它的目的是为了让我们开发单页应用程序更方便了
    - 但是它最主要是为前端带来了MVVM开发模式
    - MVVM一句话：数据驱动视图，不操作DOM
  + react
    - facebook公司自己也开发了一个web框架
    - 组件化
  + vue
    - Vue作者： 尤雨溪
    - 早期由个人开发
    - Vue借鉴了angular和React之所长，自己做了一个，后起之秀
  + 单页应用程序（交互方式）
    - 单页应用肯定是要使用一些框架的:vue,Augular,React,使用vue,angular,react也不一定是做单页
    - 但是做单页肯定是会选择其中一种框架，做单页一定是前后端分离的方式
    - 如果有SEO需求，则不要做成单页
## Vue特点
  + 轻松构建spa应用程序
  + 通过指令扩展HTML，通过表达式绑定数据到html
  + 最大程度上解放了DOM操作
  + 它能让你更加的享受编程的乐趣
  + 是为了克服HTML在构建应用上的不足而设计的，Vue有很多特性：MVVM、双向数据绑定、组件化、渐进式vue

## 前端三大开发框架
  - 单页开发其实是比较复杂的，需要有一定的技术支撑
  - 所以有了我们现在需要学习的三大框架
  + angular
    - 09年诞生
    - Google
    - 它的目的是为了让我们开发单页应用程序更方便了
    - 但是它最主要是为前端带来了MVVM开发模式
    - MVVM一句话：数据驱动视图，不操作DOM
  + react
    - facebook公司自己也开发了一个web框架
    - 组件化
  + vue
    - Vue作者： 尤雨溪
    - 早期由个人开发
    - Vue借鉴了angular和React之所长，自己做了一个，后起之秀
  + 单页应用程序（交互方式）
    - 单页应用肯定是要使用一些框架的:vue,Augular,React,使用vue,angular,react也不一定是做单页
    - 但是做单页肯定是会选择其中一种框架，做单页一定是前后端分离的方式
    - 如果有SEO需求，则不要做成单页
## Vue特点
  + 轻松构建spa应用程序
  + 通过指令扩展HTML，通过表达式绑定数据到html
  + 最大程度上解放了DOM操作
  + 它能让你更加的享受编程的乐趣
  + 是为了克服HTML在构建应用上的不足而设计的，Vue有很多特性：MVVM、双向数据绑定、组件化、渐进式vue
  
  
## Vue实例

- 每个vue应用都是通过Vue函数创建一个新的Vue实例开始的

  ```javascript
  const vm = new Vue({
    //选项
    el:
    data:
    methods:
  })
  ```

- 当创建一个Vue实例时，可以传入一个选项对象。

### el选项

- 提供一个在页面上已存在的DOM元素作为Vue实例的挂载对象，可以是css选择器，也可以是一个HTMLElement实例。
  - 不能作用到htm/body上
  - 也可以通过实例.$mount()手动挂载

### data选项

- 响应式数据

- 可以通过vm.$data访问原始的数据对象

- Vue实例也代理了data对象上所有的属性，因此访问vm.a等价于访问vm.$data.a

- 视图中绑定的数据必须是显式的初始化到data中

  ```javascript
  <div id="app"> {{ message }} </div>
  const vm = new Vue({
    el: '#app',
    data: { #视图中绑定的成员只能显式的初始化到data中
      message:'hello'
    }
  })
  # 这种方式只能修改，不能动态添加
  app.$data.message = 'haha'
  ```

  

### methods选项

- methods将被混入到Vue实例中，可以直接通过VM实例访问这些方法，或者在指令表达式中使用，方法中的this自动绑定为Vue实例

- 注意，不应该使用箭头函数来定义methods函数（例如：plus: ( ) =>this.a++）。理由是箭头函数绑定了父级作用域的上下文，所以this将不会按照期望执行Vue实例，this.a将是undefined

  ```javascript
  <div id="app"> {{ message }} </div>
  <button v-on:click="handleclick">点我</button>
  const vm = new Vue({
    el: '#app',
    data: {  
      message:'hello'
    },
      #注意：不要使用箭头函数 传统的函数
      handleClick: function(){
        window.alert(this.message)
      }
       # 推荐使用es6的对象属性函数简写方式
      handleClick (){
         window.alert(this.message)
     }
    }
  })
  ```

  

## 数据绑定

### 文本

- 数据绑定最常见的形式就是使用"Mustache"语法（双括号)的文本插值：

  ```javascript
  <span>{{ msg }}</span>
  ```

  Mustache标签将会被替代为对应数据对象上msg属性的值。无论何时，绑定的数据对象上msg属性发生了改变，插值处的内容都会更新。

  

### 一次性绑定

- 通过使用v-once指令，你也能执行一次性的插值。

- 当数据改变时，插值处的内容不会更新。但是请留心这会影响到该节点上所有的数据绑定

  ```javascript
  <span v-once>这个将不会改变：{{ msg }}</span>
  ```

### 输出HTML

- 双大括号会将数据解释为普通文本，而非HTML代码。为了输出真正的HTML，你需要使用HTML指令：

  ```javascript
  # 转译输出 即rawHtml:'<h1>hello world</h1>'会在页面上直接输出<h1>hello world</h1>
  <div>{{ rawHtml }}</div> 
  #这个会把rawHtml:'<h1>hello world</h1>'变成h1大小的hello world，即渲染后的rawHtml
  <div v-html="rawHtml"></div>
  ```

- 站点上的动态渲染的任意HTML可能会非常危险，因为很容易导致XSS攻击，所以只对可信的使用HTML插值，绝不要对用户提供的内容使用插值

### 属性绑定

- Mustache语法不能作用在HTML特性上，遇到这种情况应该使用`v-bind`指令:

  ```javascript
  # 这样写会报错，显示编译错误
  <a href="/todos?id={{ item.id }}">{{ item.title }}</a>
  # v-bind只能用于属性，它的值是一个Javascript表达式，和{{}}里面的语法一致
  # 唯一的区别是：{{}}用于标签文本绑定，v-bind用于标签属性绑定
  <a v-bind:href="item.id">{{ item.title }}</a>
  ```

- 在布尔特性的情况下，它们的存在即暗示为true , v-bind工作起来略有不同，在这个例子中：

  ```javascript
  <button v-bind:disabled="isButtonDisabled">Button</button>
  ```

  如果isButtonDisabled的值是null、undefined或者false ，则disabbled特性甚至不会被包含在渲染出来的<button>元素中

### 使用javascript表达式

- Vue.js都提供了完全的javascript表达式支持

  ```javascript
  {{ number + 1 }}
  {{ ok ? 'YES' : 'NO'}}
  {{ message.split('').reverse().join('') }}
  ```

- 有个限制就是，每个绑定都只能包含单个表达式，所以下面的例子都不会生效

  ```javascript
  # 这是语句 不是表达式
  {{ var a = 1 }}
  
  #流控制也不会生效，请使用三元表达式
  {{ if(ok) {return message} }}
  ```

- 模板表达式都被放在沙盒中，只能访问全局变量的一个白名单，如Math和Date，你不应该在模板表达式中试图访问用户定义的全局变量

## 指令

### 概念和语法

- 指令(Directives)是带有V-前缀的特殊属性。

- 指令属性的值预期是单个javascript表达式（v-for是例外情况）

- 指令的职责是当表达式的值改变时，将其产生的连带影响，响应式的作用于DOM

  ```javascript
  v-if #条件渲染
  v-for #列表渲染
  v-on #注册事件
  v-bind #属性绑定
  v-once #只绑定一次
  v-html #绑定输出HTML
  ```

  

  - 例如

    ```javascript
    <div id="app">
        <p v-if="true">你能看见我</p> #true表示能在页面看见这句话
      	<p v-if=”false“>你看不见我</p>  #false在页面中看不到这句话
    </div>
    ```

    这里的v-if指令将根据表达式seen的值的真假来插入或者移除P元素



#### 指令参数

- 一些指令能够接受一些参数，在指令名称后面以冒号表示。

- 例如，v-bind 指令可以用于响应式更新HTML属性，v-on 指令，它用于监听DOM事件：

  ```javascript
  # 这里的href是参数，告知v-bind指令将该元素的href属性与表达式url的值绑定
  <a v-bind:href="url">......</a>
  ```

  ```javascript
  #在这里参数是监听的事件名，
  <a v-on:click="dosomething">....</a>
  
  ```

#### 指令修饰符

- 一些指令还可以添加指令修饰符，修饰符（Modifies）是以半角句号`.`指明的特殊后缀，用于指出一个指令应该以特殊方式绑定。例如：`.prevent`修饰符告诉v-on指令对于触发的事件调用`event.preventDefault()`。

  ```javascript
  <form v-on:sumit.prevent="orSubmit">......</form>
  ```

#### 指令缩写

- `v-`前缀作为一种视觉提示，用来识别模板中Vue特定的特性。

- 当在使用vue.js为现有标签添加动态行为（dynamic behavior）时，`v-`前缀很有帮助，然而，对于一些频繁用到的指令来说，就会感到使用繁琐。

- 同时，在构建由Vue.js管理所有模板的单页面应用程序（SPA-single page application）时，`v-`前缀也会变得没那么重要了。

- 因此，vue.js为**V-bind**和**v-on**这两个最常用的指令，提供了特定简写：

  - `v-bind`缩写：

    ```javascript
    # 完整语法
    <a v-bind:href="url">。。。。</a>
    # 缩写
    <a :href="url"></a>
    ```

    

  - `v-on`缩写:

    ```javascript
    # 完整语法
    <a v-on:click="dosomething">....</a>
    #缩写
    <a @:click="dosomething">....</a>
    ```

    

    

- vue实例的生命周期
  - 什么是生命周期：从Vue实例创建，运行，到销毁期间，总是伴随着各种各样的事件，这些事件，统称为生命周期！
  - 生命周期钩子：就是生命周期事件的别名
  - 生命周期钩子 = 生命周期函数 = 生命周期事件
- 主要生命周期函数分类：
  - 创建期间的生命周期函数：
    + beforeCreate：实例刚在内存中被创建出来，此时，还没有初始化好data和methods属性
    + created:实例已经在内存中创建ok,此时data和methods已经创建ok,此时还没有开始编译模板
    + beforeMount:此时已经完成了模板的编译，但是还没有挂载到页面中
    + mounted:此时，已经将编译好的模板，挂载到了页面指定的容器中显示
  - 运行期间的生命周期函数：
    + beforeUpdate:状态更新之前执行此函数，此时data中的状态值是最新的，但是界面上显示的数据还是旧的，因为此时还没有开始重新渲染节点
    + updated：实例更新完毕之后调用此函数，此时data中的状态值和界面上显示的数据，都已经完成了更新，界面已经被重新渲染好了
 - 销毁期间的生命周期函数：
    + beforeDestory：实例销毁之前调动，在这一步，实例仍然完全可用
    + destroyed:Vue实例销毁之后调动。调用后，Vue实例指示的所有东西都会解绑定，所有的事件监听器都会被销毁，所有的子实例也会被销毁。 
    
# VUE组件

## 定义Vue组件

- 什么是组件：组件的出现，就是为了拆分Vue实例的代码量的，能够让我们以不同的组件，来划分不同的功能模块，将来我们需要什么样的功能，就可以去调用对应的组件即可

- 组件化和模块化的不同：

  - 模块化：是从代码逻辑的角度进行划分的，方便代码分层开发，保证每个功模块的职能单一

  - 组件化：是从UI界面的角度进行划分的: 前端的组件化，方便UI组件的重用

    
