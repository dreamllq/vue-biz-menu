# lc-vue-biz-menu

封装的菜单组件

## 安装

```bash
npm i lc-vue-biz-menu
```

## 依赖

- vue@3.x
- element-plus@2.x

## Demo

[demo](https://unpkg.com/lc-vue-biz-menu/docs/.vitepress/dist/index.html) 

## 基本使用

```vue
<template>
  <div>
    <biz-menu :menu-data='menuData' />
  </div>
</template>

<script setup lang="ts">

import { BizMenu } from 'lc-vue-biz-menu';

const menuData = [
  {
    'key': 'welcome',
    'label': '首页',
    'icon': 'House',
    'children': [
      {
        'key': 'welcome1-1',
        'icon': 'House',
        'label': '首页1-1',
        'children': null
      },
      {
        'key': 'welcome1-2',
        'icon': 'House',
        'label': '首页1-2',
        'children': null
      }
    ]
  },
  {
    'key': 'welcome1',
    'label': '首页1',
    'icon': 'House',
    'children': null
  },
  {
    'key': 'welcome2',
    'label': '首页2',
    'icon': 'House',
    'children': null
  },
  {
    'key': 'welcome3',
    'label': '首页3',
    'icon': 'House',
    'children': null
  }
];
</script>
```

## Api

### Attributes

| 属性名 | 说明 | 类型 | 默认值 |
| ---- | ---- | ---- | ---- |
| menuData | 菜单数据 | MenuItem[] | [] |
| menuIndex | 选中的菜单index | String | - |
| isCollapse | 是否折叠 | Boolean | false |
| model | 菜单展示模式 | horizontal / vertical | vertical |
| unique-opened | 是否只保持一个子菜单的展开 | boolean | false |

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