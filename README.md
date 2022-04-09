1.<br>
**问题：**![image](https://user-images.githubusercontent.com/85120764/162559796-7dd4abc9-d309-45e0-8657-41333f87caf2.png)Uncaught SyntaxError: Unexpected end of JSON input<br>
**原因：** json不能解析空字符串<br>
**解决：**<br>
2.<br>
**问题：** 在使用反向否定查找（/(?<!)/）正则时，webpack构建报错SyntaxError: Invalid regular expression<br>
**原因：** 可能是babel无法解析反向否定查找这种规则<br>
**解决：** 不要用字面量创建正则，使用构造函数，例如 new RegExp('(?<!)')<br>
3.<br>
**问题：** 如何刷新vue子组件<br>
**原因：**<br>
**解决：** 使用key方式，改变key来刷新子组件，例如 
```js
<ChlidrenComponent :key="refreshComponentKey" />
export defaults{
  methods:{
    changeKey(){
    this.refreshComponentKey +=1
    }
  }
}
```
