# WOW.js 增强版

Language: [中文](README.md) | [English](README.en.md)

[Forked From Github graingert/WOW](https://github.com/graingert/wow)

# ⚠ 原项目已经废弃

本项目为山东远山科技有限公司为特殊需求修改的增强版，不建议个人项目使用，原项目建议使用[AOS](https://github.com/michalsnik/aos)进行替代

---

根据页面滚动展示css动画, WOW.js Plus 在原项目的基础上增加了部分功能，以适配某些特殊场景使用。

### [在线预览 (原项目官网) ➫](https://graingert.co.uk/WOW/)


## 使用文档

### 增强版功能

#### 动画展示顺序

使用数字来定义动画展示的顺序，并且可以通过配置修改展示间隔

- Demo

```html
<section class="animation__animated animation__fadeIn wow" data-wow-order="1"></section>
<section class="animation__animated animation__fadeIn wow" data-wow-order="2"></section>
<section class="animation__animated animation__fadeIn wow" data-wow-order="3"></section>
```

上述案例可以将三个模块顺序加入动画展示

- 配置间隔

```js
new WOW({
  orderDuration: 400
}).init()
```

修改动画间隔为400ms

### 依赖的库
- [animate.css](https://github.com/daneden/animate.css)

### 安装方式

- Bower

```bash
   bower install wow-mit
```

- NPM

```bash
   npm install wow.js
```

### 快速开始

- HTML

```html
  <section class="wow animate__animated animate__slideInLeft"></section>
  <section class="wow animate__animated animate__slideInRight"></section>
```

- JavaScript

```javascript
new WOW().init();
```

### 高级使用方式

- HTML

```html
  <section class="wow animate__animated animate__slideInLeft" data-wow-duration="2s" data-wow-delay="5s"></section>
  <section class="wow animate__animated animate__slideInRight" data-wow-offset="10"  data-wow-iteration="10"></section>
  <section class="wow animate__animated animate__slideInRight" data-wow-order="1"  data-wow-iteration="10"></section>
  <section class="wow animate__animated animate__slideInRight" data-wow-order="2"  data-wow-iteration="10"></section>
```

- JavaScript

```javascript
var wow = new WOW(
  {
    boxClass:     'wow',      // 应用wow的class
    animateClass: 'animated', // 动画加载的类属性
    offset:       0,          // 触发动画的距离 默认为0
    mobile:       true,       // 在移动设备上应用触发器 (默认开启)
    live:         true,       // 异步加载内容 (默认开启)
    callback:     function(box) {
      // Callback  将会在每次动画执行时运行
    },
    scrollContainer: null,    // 手动选择滚器， null时为监听window
    resetAnimation: true,     // 在最后重置动画 (默认开启)
    orderDuration: 200,       // 排序展示动画间隔
  }
);
wow.init();
```

## 开发者

原开发者为Matthieu Aussaguel, [mynameismatthieu.com](http://mynameismatthieu.com)

[Thomas Grainger](https://graingert.co.uk)进行二次维护，并于2016年启用

增强版为山东远山数字科技有限公司维护