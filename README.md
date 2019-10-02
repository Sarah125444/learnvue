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
