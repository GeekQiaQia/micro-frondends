[Vue-CLI4](https://cli.vuejs.org/zh/guide/creating-a-project.html)

# micro-frontend
## 项目框架
### 微前端（[qiankun官网](https://qiankun.umijs.org/)）
### 微前端[FAQ](https://qiankun.umijs.org/faq#error-here-is-no-fetch-on-the-window-env-you-need-to-polyfill-it)

**微前端** 类似于微服务架构，主要面向浏览器端，能将一个庞大的单体应用拆分为多个功能模块清晰且独立的子应用，且共同服务同一个主应用。
* 各个子应用可以独立运行、独立开发和独立部署；
#### 项目扩展
* 考虑到后期**业务的扩展**(如：证券业务)，以及**技术栈的升级**（如：vue3的落地、reactJS技术栈的应用）；
* 将按照业务的不同划分不同的子应用microApp

        // main.js导入qiankun所需方法
        import {
            registerMicroApps, // 注册子应用
            runAfterFirstMounted,// 本地一个子应用装载完毕
            setDefaultMountApp, // 设置默认装载的子应用
            initGlobalState, // 微前端之间的通信	
            start // 启动

        } from 'qiankun'

## 团队协作规约
### 变量命名规则：
小驼峰式命名法（Camel-Case）
* 在后缀为.ts文件或者.js文件中，变量命名以小驼峰式命名法（Camel-Case）如：homePageNews  //代表首页新闻
* 为了便于团队协作，变量名要求以有意义的单词，不可以中文拼音缩写如：hpg  //代表首页新闻

### 类名命名规则：
短横线命名（-）
* 当class或者ID包含多个单词时，应使用连字符（-）如：page-transition-enter
* 采用英文字母、数字以及"-"和命名
* 以小写字母开头，不能以数字和“-”、“_”开头
* 同样，CSS中也不建议使用下划线连接的命名方式。


### 前端技术栈
   
    {
    "vue-cli3":@3.8.2,
    "vue": "^2.6.11",
    "vue-router": "^3.3.4",
    "vuex": "^3.5.1",
    "axios": "^0.19.2",
     
    }


## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
