# Vivid Typing

[online](http://vivid-typing.hejian.club/)


# start

```bash

 npm i vivid-typing # 安装依赖

# main.ts 引入
  import { createApp } from 'vue'
  import { VividTyping } from 'vivid-typing'

  const app = createApp(App)
  app.component('VividTyping', VividTyping)
  app.mount('#app')
```

# usage

```markdown
  <vivid-typing :interval="100" :delay="0" h-10 content="hi"></vivid-typing>
```
 ## 更多使用技巧可以参考[github](https://github.com/Simon-He95/vivid-typing/blob/master/playground/src/App.vue)

# api guide

```markdown

type defaultProps = {
  interval: number  // 文字间隔
  delay: number    // 延迟多久开始
  infinity: boolean | undefined // 是否无限循环
  finish: Function | undefined  // 完成后的回调
  spiltTag: string | undefined  // 将文本以spiltTag标签分割
  spiltClass: string | undefined  // 分割的Tag加上spiltClass类
  spiltStyle: string | Function | undefined // 分割的Tag加上spiltStyle样式，支持函数可以正对每个分割的Tag独立的style 
  content: string | string[] // 渲染的内容
  stable: boolean // 默认在finish之后content会被清空在重新渲染，如果为true，会在清空后立即展示content的第一个元素
  scrollX: boolean // 实现一个横向通知栏的效果(注意实现demo效果需要外层嵌套一个div加上overflow:hidden)
  scrollY: boolean // 实现一个纵向通知栏的效果(注意实现demo效果需要外层嵌套一个div加上overflow:hidden)
  speed: number // 控制滚动的速度
  reverse: boolean // 翻转scrollX和scrollY的方向默认false,向下或向左
}

```
