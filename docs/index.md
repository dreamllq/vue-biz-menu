# lc-vue-biz-menu

封装的菜单组件

## 安装

```bash
npm i lc-vue-biz-menu
```

## 依赖

- vue@3.x
- element-plus@2.x

## DEMO

<Demo c="base/demo"/>

## Api

### Attributes

| 属性名 | 说明 | 类型 | 默认值 |
| ---- | ---- | ---- | ---- |
| menuData | 菜单数据 | MenuItem[] | [] |
| menuIndex | 选中的菜单index | String | - |
| isCollapse | 是否折叠 | Boolean | false |
| model | 菜单展示模式 | horizontal / vertical | vertical |

### Events

| 事件名 | 说明 | 类型 |
| ---- | ---- | ---- |
| select | 菜单激活回调 | index: 选中菜单项的 index | 


## Type

### MenuItem

```ts
interface MenuItem {
  key: string,
  label: string,
  icon?: string,
  subPages?: string[],
  children?: MenuItem[]
}
```