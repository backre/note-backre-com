

[setState and forceUpdate](https://legacy.reactjs.org/docs/react-component.html#other-apis-1)

这两个方法可以从组件中调用（其他方法多是由 React 调用）。

## setState()

格式：

    setState(updater[, callback])

此方法的作用是更改组件状态，并让React更新该组件及其子组件的显示。因此，在收到事件消息或响应之后，常常用它来刷新界面。


Think of setState() as a request rather than an immediate command to update the component. For better perceived performance, React may delay it, and then update several components in a single pass. In the rare case that you need to force the DOM update to be applied synchronously, you may wrap it in flushSync, but this may hurt performance.

...

