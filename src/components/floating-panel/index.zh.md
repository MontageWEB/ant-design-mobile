# FloatingPanel 浮动面板

<code src="./demos/demo1.tsx"></code>

### 属性

| 属性                    | 说明                                                       | 类型                                           | 默认值 |
| ----------------------- | ---------------------------------------------------------- | ---------------------------------------------- | ------ |
| anchors                 | 可拖拽至哪些高度，单位为 `px`                              | `number[]`                                     | -      |
| onHeightChange          | 当高度变化时触发，`animating` 参数表示是否处于动画过程中   | `(height: number, animating: boolean) => void` |        |
| handleDraggingOfContent | 是否会处理面板内容区域的拖拽事件，禁用后则只能拖拽头部区域 | `boolean`                                      | `true` |

### Ref

FloatingPanel 的 ref 上提供了 `setHeight` 方法，你可以通过它来指令式地控制 `FloatingPanel` 的高度：

```ts
type FloatingPanelRef = {
  setHeight: (
    height: number,
    options?: {
      immediate?: boolean // 是否跳过动画
    }
  ) => void
}
```

```jsx
<FloatingPanel ref={ref}>...</FloatingPanel>

ref.current.setHeight(100)
```
