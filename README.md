# 使用Framework7-Vue重构的Framework7官网 Demo

Framwork7-Vue 将 Framework7 和 Vue 结合起来，但官方文档有些地方描述的不清楚，而且在实际开发中也可能会遇到各种各样的问题，所以我就使用Framework7-Vue 重构了官网的 Demo，同时对重构过程中遇到的问题和解决方案写了几篇博客，博客地址：http://blog.ywulin.com/tags/framework7/

## 运行程序

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```

## 项目结构

* `src/assets` - 静态资源（图片）目录
* `src/css` - css文件目录
* `src/pages` - app的页面目录
* `src/main.js` - 引入包并初始化App
* `src/routes.js` - App的路由控制
* `src/app.vue`

> 之前把Demo重构完后就以为工作结束了，后面一看，发现没有加上自己写的关于Framework7的博客地址，另外也没有很好地对这个项目做个简介，不好意思，现在才补上