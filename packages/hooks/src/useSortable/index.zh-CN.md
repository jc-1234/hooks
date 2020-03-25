---
title: useSortable
nav:
  title: Hooks
  path: /hooks
group:
  title: UI
  path: /ui
  order: 9
legacy: /ui/use-sortable
---

# useSortable

一个帮助你生成可拖拽排序的列表的 hook.

## 代码演示

### 基础用法

<code src="./demo/demo1.tsx" />

## API

```javascript
const { list } = useSortable<T>({
  initialValue: T[],
  onSort: (oldIndex, newIndex, oldList, newList) => void,
});

// in render
{
  list.map((e, index) => (<div {...e.props}>sortable</div>))
}
```

### Result

| 参数     | 说明                                 | 类型                 |
|----------|-------------------------------------------|-------------------------|
| list  | 完整的待排序列表 | { type: 'dummy' \| 'item', content: T, props: PropsType }[] |

### useDrop Params

| 参数    | 说明                                         | 类型                   | 默认值 |
|---------|----------------------------------------------|------------------------|--------|
| initialValue | 列表的初始值 | T[] | -      |
| onSort | 元素被拖动后的回调 | (oldIndex: number, newIndex: number, oldList: T[], newList: T[]) => void | -      |