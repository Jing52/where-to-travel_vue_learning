# where-to-travel_vue_learning

## Build Setup
```
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```
For a detailed explanation on how things work, check out the guide and docs for vue-loader.

## 多页应用
页面跳转->返回HTML
. 优点：首屏时间快，SEO效果好
. 缺点：页面切换快

## 单页应用
页面跳转-> JS渲染
. 优点：页面切换快
. 缺点：首屏时间稍慢，SEO效果差

## 所需样式
. border.css
. reset.css

## 下载fastclick
```
//手机端点击事件会出现300ms的延迟，下载fastclick可解决问题
//必须在项目目录下安装
//引用：import faskClick from 'faskclick'
//使用：fastClick.attach(document.body)
npm install fastclick --save
```

## iconfont

![点击进入官网](https://www.iconfont.cn/)
图标管理->我的项目->新建项目

## 首页开发
### 首页轮播插件
[vue-awesome-swiper](https://github.com/surmon-china/vue-awesome-swiper)
```
##我这边使用了老版本的v2.6.7
npm install vue-awesome-swiper@2.6.7 --save
```
```
import Vue from 'vue'
import VueAwesomeSwiper from 'vue-awesome-swiper'

// require styles
import 'swiper/dist/css/swiper.css'

Vue.use(VueAwesomeSwiper, /* { default global options } */)
```
如此，Swiper插件已经可以使用了
```
<!-- The ref attr used to find the swiper instance -->
<template>
  <swiper :options="swiperOption" ref="mySwiper" @someSwiperEvent="callback">
    <!-- slides -->
    <swiper-slide>I'm Slide 1</swiper-slide>
    <swiper-slide>I'm Slide 2</swiper-slide>
    <swiper-slide>I'm Slide 3</swiper-slide>
    <swiper-slide>I'm Slide 4</swiper-slide>
    <swiper-slide>I'm Slide 5</swiper-slide>
    <swiper-slide>I'm Slide 6</swiper-slide>
    <swiper-slide>I'm Slide 7</swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
    <!-- 左右箭头 -->
    <div class="swiper-button-prev" slot="button-prev"></div>
    <div class="swiper-button-next" slot="button-next"></div>
    <!-- 滚动条 -->
    <div class="swiper-scrollbar"   slot="scrollbar"></div>
  </swiper>
</template>
<script>
  export default {
    name: 'carrousel',
    data() {
      return {
        swiperOption: {
          // some swiper options/callbacks
          // 所有的参数同 swiper 官方 api 参数
          // ...
        }
      }
    },
    computed: {
      swiper() {
        return this.$refs.mySwiper.swiper
      }
    },
    mounted() {
      // current swiper instance
      // 然后你就可以使用当前上下文内的swiper对象去做你想做的事了
      console.log('this is current swiper instance object', this.swiper)
      this.swiper.slideTo(3, 1000, false)
    }
  }
</script>
```