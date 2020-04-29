### `mobile-text-selection` 介绍

移动端 h5 长按选择文本的工具， 屏蔽了安卓和 ios 系统选中文本后的弹窗。

返回选中的文本、起始点和终点的坐标

mobile terminal custom text selection, compatible width ios and android. long press pop-up window provided by the system are forbidden.

### 安装

```
npm i mobile-text-selection
```

### 使用

```js
import TextSelection from "mobile-text-selection";

const textWrapper = document.getElementById("textWrapper");
const textSelection = new TextSelection({
  container: textWrapper, // 容器 必须要传哦
  cursorColor: "#1788bd", // 左右指针颜色 可以不传  "red" || "#333333" || "rgba(125,125,125)"
  rectsColor: "rgba(23,136,189,0.35)", // 选中文字的颜色 可以不传  "#333333aa" || "rgba(125,125,125, 0.5)" 需要是个透明色哦
  longTapDuration: 400, // 长按的时间 默认是400
  selectCb: () => {}, // 开始选择的回调 可以不传
  finishCb: ({
    text, // 选中的文字
    startX, //  相对于容器 前指针右侧第一个字的左上角的x坐标
    startY, //  相对于容器 前指针右侧第一个字的左上角的y坐标
    endX, //  相对于容器 后指针左侧第一个字的右上角的x坐标
    endY, // 相对于容器 后指针左侧第一个字的右上角的y坐标
  }) => {}, // 选完的回调 也可以不传
});
// 初始化
textSelection.init();
```

### Demo

[demo](https://codesandbox.io/s/mobile-text-selection-example-zc9k3?file=/src/App.js)

### 第一次学着写 npm 包（紧张
