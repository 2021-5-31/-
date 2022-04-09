1.**问题：**![image](https://user-images.githubusercontent.com/85120764/162559796-7dd4abc9-d309-45e0-8657-41333f87caf2.png)Uncaught SyntaxError: Unexpected end of JSON input
**原因：** json不能解析空字符串
**解决：**
2.**问题：** 在使用反向否定查找（/(?<!)/）正则时，webpack构建报错SyntaxError: Invalid regular expression
**原因：** 可能是babel无法解析反向否定查找这种规则
**解决：** 不要用字面量创建正则，使用构造函数，例如 new RegExp('(?<!)')
3.**问题：** 如何刷新vue子组件
**原因：**
**解决：** 使用key方式，改变key来刷新子组件，例如 
```
<chlidrenComponent :key="refreshComponentKey" />
export defaults{
  methods:{
    changeKey(){
    refreshComponentKey +=1
    }
  }
}
```
