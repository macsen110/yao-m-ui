# yao-m-ui 简单常用的ui组件

## Installation && Use

```bash
npm i yao-m-ui --save

import * as ui form 'yao-m-ui' 

ui.Dialog({})
```

或者使用require加载

```bash
npm i yao-m-ui --save

var ui = require('yao-m-ui')

ui.Dialog({})
```

或者直接script 标签引入 npm包目录下的index.js

```js

<script src="./index.js"></script>

window.yaoMUI.Dialog({})

```


## Document

### 弹框提示


ui.Dialog(options)

- `className` 最为组件root 标签下传入的css class名称, 业务中定制化组件需要在此重写

- `afterOpen` 代码片段render到body中就调用

- `afterClose` 一般是点击关闭, 取消等行为,会首先调用,

- `afterOk` 一般是点击确定

- `destory` 摧毁组件,将此组件中的代码从body中remove掉

- `canMaskClose` 点击蒙层是否可关闭

- `isMask` 是否需要蒙层

- `maskAction` 定制蒙层点击事件

- `close` 点击关闭,取消

>
### totast提示  

ui.showPrompt(options)

- 一般便捷用法, `ui.showPrompt('hello, world')`, 三秒后消失

- `msg`  弹出的消息

- `cb`   弹框消失后调用,一般是一个callBack function;

- `duration` 弹框显示的时长,默认为3秒

- `className` 定制化用到的class name

### 滑动组件

ui.easyMove(element, options) 滑动组件,类似于swiper

- `element` 滚动目标dom 节点

- options 滑动的配置信息
    - `parentEle` 手指touch目标元素 默认为 element

    - `focusIndex` 默认定位到那个item

    - `speed` 滚动速率

    - `limitBorder` 滑动后是否会回顶到边界

    - `showNum` 显示的滑动的item数量

    - `distance` 自定义滑动距离

    - `orientation` 滑动方向 1为横向,2为纵向

    - `touchMoveCb` 监听动画滑动回调

    - `callback` 动画完成后的回调

    - `autoMove` 是否需要自动播放
    - `paginationList` 底部导航dom,当前滚动下标对应的class为active


### Tab切换 
ui.tab(options)
* `tabNavContainer`  //default as '.tab-nav-container'

* `tabConContainer`  //default as '.tab-con-container'

使用了事件代理,异步添加的nav 也会默认增加切换事件

Demo地址 
Contact 

* email 839945193@qq.com or liangyusen1202@gmail.com
