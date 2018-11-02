# nuxt-demo

> My majestic Nuxt.js project

## Build Setup

``` bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm start

# generate static project
$ npm run generate
```
For detailed explanation on how things work, checkout [Nuxt.js docs](https://nuxtjs.org).

##     目录结构
.
├── .nuxt                       Nuxt自动生成,临时用于编辑的文件,build
├── assets                      资源文件。放置需要经过 webpack 打包处理的资源文件，如 scss，图片，字体等。
├── components                  组件。这里存放在页面中，可以复用的组件。
├── layouts                     布局。用于组织应用的布局组件,不可更改.
├── middleware                  中间件。存放中间件。可以在页面中调用： middleware: 'middlewareName' 。
├── node_modules
├── pages                       页面。一个 vue 文件即为一个页面。index.vue 为根页面。
├── plugins                     插件。用于组织那些需要在 根vue.js应用 实例化之前需要运行的 Javascript 插件
├── server                      本地服务
├── static                      静态文件。放置不需要经过 webpack 打包的静态资源。如一些 js, css 库。
├── store                       状态管理。具体使用请移步至 [官网](https://zh.nuxtjs.org/guide/vuex-store/)。
├── nuxt.config.js              用于组织Nuxt.js 应用的个性化配置，以便覆盖默认配置。具体配置请移步至 [官网](https://zh.nuxtjs.org/guide/configuration/)。
├── nuxt.config.js              npm自动生成,用于帮助package统一性设置的.
└── package.json                npm包管理配置


##      入坑记录

###     1.基于官方生成步骤,起本地服务一直报错.
        node>=8.3.0

###      2.路由
            a.在pages目录下,新建.vue文件,nuxt.js会自动生成路由配置(详见.nuxt文件中router.js).
            b.在该目录下,再新建文件夹,如果新建的文件以index.vue命名,等同于步骤a.
            c.如果文件另命名,就默认为该目录下的二级路由(子路由).
            d.跳转路由,官方推荐<nuxt-link to="/account">账号</nuxt-link>.[官方](https://zh.nuxtjs.org/api/components-nuxt-link).
