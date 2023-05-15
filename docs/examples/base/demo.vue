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

<style scoped>

</style>