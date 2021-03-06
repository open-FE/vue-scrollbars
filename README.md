# vue-scrollbars

![GitHub](https://img.shields.io/github/license/mashape/apistatus.svg) ![Github file size](https://img.shields.io/badge/size-10kb-brightgreen.svg)
![npm](https://img.shields.io/badge/npm-6.4.1-red.svg)
![node.js](https://img.shields.io/badge/node.js-v10.9.0-blue.svg)

> 基于 Vue 的 PC 端滚动组件 简单 轻量 高效
> 仅对原生滚动组件进行滚动条样式统一化处理，并添加自动隐藏,拖动滚动等常用功能

## github

[github](https://github.com/zhangzhengyi12/vue-scrollbars)

if you like , click star , thanks!

## DEMO

[live-demo](http://yinode.tech/vue-scrollbars/)

使用示例请看 app.vue

## How to use

```bash
sudo npm i @zhangzhengyi12/vue-scrollbars --svae
```

global regisiter

```js
import Vue from 'vue'
import Scrollerbars from '@zhangzhengyi12/vue-scrollbars'
Vue.use(Scrollerbars)
```

OR in component

```js
import Scrollerbars from '@zhangzhengyi12/vue-scrollbars'

// in vue component

export default {
  components: { Scrollerbars }
}
```

```xml
<scrollbars style="height:200px" autoHide>
  <!-- you content -->
</scrollerbars>
```

## Props

| name               | type     | desc                                      | default |
| ------------------ | -------- | ----------------------------------------- | ------- |
| autoHide           | Boolean  | auto hide scrollbar                       | false   |
| hideTime           | Boolean  | auto Hide Time                            | 1000    |
| data               | Array    | on watch Data Change refresh Bar          | []      |
| displayBar         | Boolen   | display scrollbar                         | true    |
| listenScrollBottom | Function | Called when scrolling to the bottom       | false   |
| scrollBottomHeight | Number   | listenScrollBottom handler trigger height | 50      |
| listenScrollRight  | Function | Called when scrolling to the right        | false   |
| scrollBottomHeight | Number   | listenScrollRight handler trigger height  | 50      |

## APIS

| name      | params | desc              |
| --------- | ------ | ----------------- |
| refresh() | null   | refersh scrollbar |

> this.\$refs.scrollbars.refresh()

## Event

| name    | params              | desc                |
| ------- | ------------------- | ------------------- |
| @scroll | scroll event object | native scroll Event |
