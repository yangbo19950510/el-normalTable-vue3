<template>
  <div>
    <NormalTable :data="tableData"></NormalTable>
    <!-- <NormalTables /> -->
  </div>
</template>

<script lang="ts" setup>
import { reactive } from 'vue'
import NormalTable from '@/components/NormalTable'

const tableData = reactive({
  filter: [
    {
      tag: 'Select',  // 驼峰方式
      label: '状态',
      prop: 'status',
      bind: {
        options: [{label: '测试1', value: 1}]
      }
    },
    {
      tag: 'Input',
      label: '状1态',
      prop: 'statu1s',
    },
    {
      tag: 'Select',  // 驼峰方式
      label: '状态',
      prop: 'stat1us',
      bind: {
        options: [{label: '测试1', value: 1}]
      }
    },
    {
      tag: 'Input',
      label: '姓名',
      prop: 'name',
    },
  ],
  colums: [
    {
      prop: 'ddd',
      label: '测12222试',
      width: '140px',
    },
    {
      prop: 'img',
      label: '测12222试',
      type: 'Img'
    }
  ],
  onSearch: async({ filterValue, pagination }) => {
    return {
      ...pagination,
      page: 1,
      total: 1000,
      pageSize: 100,
      list: [{
        ddd: '测试',
        img: '呵呵'
      }]
    }
  }
})
</script>

<style>

</style>
