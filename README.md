# automatic-broccoli
做一篇博客样式的网页，描述自己最喜欢的人

我最喜欢的人是超模Karlie Elizabeth Kloss
具体展现效果见https://codepen.io/candice666/project/full/XqEzqQ/

DIV里面的图片水平与垂直居中的方法


```
<div class=“box”>

　　<img />

</div>

```
1.水平居中：

- box设置text-align:center;    text-align:center可以实现子元素字体，图片的水平居中。

- img设置margin:0 auto;display:block;            margin:0 auto是针对块元素的水平居中方法，所以要加上display：block。

2.垂直居中：

- 图片使用padding，用box的高度减去图片的高度再除以2，就是padding-top的值，这样也可以实现图片在div里居中。也可以在设置margin：0 auto时，把0改为刚才padding-top的值也可以。

　　    
```
img{

　　　　position:relative;

　　　　top:50%;

　　　　left:50%;

　　　　margin-top:  负图片height的一半；

　　　　margin-left：负图片width的一半；

　　}

```

- box设置display: table-cell;vertical-align: middle;                      display: table-cell 相当于是把标签元素当作一个单元格来处理。但是唯一的缺点就是IE6/7不兼容。

 

3.垂直居中的另外中方法：table的宽高自己设置

　　　　html:
　　　　
```

　　　　<table class="img_meng_show">
　　　　　　<tr>
　　　　　　　　<td>
　　　　　　　　　　<img src="">
　　　　　　　　</td>
　　　　　　</tr>
　　　　</table>

```


　　　　css:　
　　　　
```
.img_meng_show td{
　　　　　　vertical-align: middle;
　　　　　　text-align: center;
　　　　}
```


　　　　
　　

　　这样图片就在table里面垂直居中了

 

 

DIV垂直居中的方法：

```
<div class="box></div>

　　.box{

　　position:absolute(或者是fixed);

　　top:0;

　　left:0;

　　bottom:0;

　　right:0;

　　margin:auto;

　　width:100px;

　　height:200px;

}
```




　这个能实现div垂直居中，如果要图片也垂直居中的话，也可以把图片放进div里，但是必要条件就是宽高必须加上，margin也必须加上；

　　如果只想垂直居中，只要top与bottom，然后margin:auto 0;

　　同理，只想水平居中，只要top与bottom，然后margin: 0 auto;

　但是这种方法不支持ie8以下，可考虑用于手机端。
