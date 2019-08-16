# Note
笔记
### 阻止冒泡和默认事件

```javascript
// 事件冒泡
function stopBubble(e) {
    if(e && e.stopPropagation) {
        e.stopPropagation();
    } else {
        window.event.cancaelBubble = true;
    }
}

// 阻止默认行为
function stopDefault(e) {
    if(e && e.preventDefault) {
        e.preventDefault();
    } else {
        window.event.returnValue = false;
    }
}
```

