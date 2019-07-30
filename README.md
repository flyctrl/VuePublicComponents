### notification组件
使用方法：

1.引用
```
import Notification from './components/notification'
Vue.use(Notification)
```
2.场景使用
```
.....
  methods: {
    notify () {
      this.$notify({
        content: 'test notify',
        btn: 'close'
      })
    }
  }
.....
 ```
 3.参数说明
 * content： 弹框的内容 String
 * btn：关闭按钮的文字描述 String
 
 ### tabs组件
 使用方法
 
 1.用法一
 ```
<template>
...
 <tabs :value="tabValue" @change="handleChangeTab">
  <tab label="tab1" index="1">
    <span>tab content 1</span>
  </tab>
  <tab index="2">
    <span slot="label" style="color: red">tab2</span>
    <span>tab content 2</span>
  </tab>
  <tab label="tab3" index="3">
    <span>tab content 3</span>
  </tab>
 </tabs>
 ...
 </template>
 <script>
 ...
  methods: {
    handleChangeTab (value) {
      this.tabValue = value
    }
  }
 ...
 </script>
 ```
 2.用法二
 ```
 <template>
...
 <tabs :value="filter" @change="handleChangeTab">
   <tab :label="tab" :index="tab" v-for="tab in stats" :key="tab" />
 </tabs>
 ...
 </template>
 <script>
 ...
 data () {
    return {
      filter: 'all',
      stats: ['all', 'active', 'completed']
    }
  },
  methods: {
      this.filter = value
    }
  }
 ...
 </script>
 ```
 3.参数说明
 * value 当前选中的选卡的值 String/Number
 * change 点击tab头部的时候触发事件，点击选卡的值在回调函数内部 Function
 * label tab头部的显示的文字 String
 * index 当前选卡的值 String/Number
 
