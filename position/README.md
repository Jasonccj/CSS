
目前整理了position定位相关内容

###文档流
 以下均在标准流中,无特殊的定位
**块级元素**: 
> 一般各占一行 .例如:div , H1-H6 , table ,有序,无需列表(ol,ul,li) , p段落

**内联元素**:
> 一般同行,只有一行满才被挤到下一行 .例如:a , span , img ,input

------

###position=relative(未脱离标准文档流)
当设置为relative相对定位时,才可以使用top,right,bottom,left,
> top: 下移   right:左移 bottom:上移 left:右移

------
###position=absolute(脱离标准文档流)
相对于当前窗口的绝对定位
例如: 
``` css
position: absolute;
left: 50px;
bottom: 50px;
```
相当于屏幕左下角的绝对定位
虽然我们是相对于屏幕定位的,但是我们依然也是可以屏幕以下定位的
例如:
``` css
position: absolute;
left: 50px;
bottom: -150px;
```
相当于屏幕左下角向下定位150px
当出现父div无定位元素postion定位时,此时依然按照屏幕定位
```html
<div class="pre">
    <div class="test"></div>
</div>
```
------

###position=fixed(脱离标准文档流)
固定定位

定位类似于absolute,以当前窗口进行定位.不过fixed定位不受其他任何定位元素影响

###position=inherit(脱离标准文档流)
规定应该从父元素继承 position 属性的值   


