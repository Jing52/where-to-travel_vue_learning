# where-to-travel_vue_learning
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
(点击进入官网)[https://www.iconfont.cn/]
图标管理->我的项目->新建项目