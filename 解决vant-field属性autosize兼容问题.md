### 解决了vant-field属性autosize在iOS上的兼容问题

1、van-field type 为textarea autosize设置boolean无效，代码如下：

```html
<van-field
      readonly
      type="textarea"
      autosize
      class="custom-field"
      value="{{text}}"
      name="{{fieldName}}"
      label="{{cLabel}}"
      disabled="{{ isDisabled }}"
      right-icon="{{ !isDisabled ? 'arrow' : ''}}"
      placeholder="{{ isDisabled ? '' : '请选择' }}"
      bind:click-input="handleClick"
    >
    </van-field>

```



2、iOS系统下的截图如下：

![image-20250207193113560](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250207193113560.png)

3、添加了autosize属性设置如下：

```js
autosize="{{ { maxHeight: 100, minHeight: 45} }}"
```



4、效果如下截图：

![image-20250207193321101](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250207193321101.png)