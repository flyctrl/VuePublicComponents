### notification组件
使用方法：

1.全局引用
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
