使用伪类写边框部分三角
右上角三角形

1 border-top:6px solid #c1ddf7
2 border-left:6px solid transparent

右下角三角形

1 border-bottom:6px solid #c1ddf7
2 border-left:6px solid transparent

左上角三角形

1 border-top:6px solid #c1ddf7
2 border-right:6px solid transparent

左下角三角形

1 border-bottom:6px solid #c1ddf7
2 border-right:6px solid transparent

圆形边框
border-radius:以百分比定义圆角的形状。-webkit-border-radius是chrome，Safari私有属性。
img{
    border-radius: 100%;
    -webkit-border-radius: 100%;
}

手机密度比
设备最小宽度321px到最大宽度1080px之间且最大密度比为2
1 @media (min-width:321px) and (max-width:1080px) and (-webkit-max-device-pixel-ratio: 2) {
2 }

设备最小宽度321px到最大宽度1080px之间且最小密度比为2
1 @media (min-width:321px) and (max-width:1080px) and (-webkit-min-device-pixel-ratio: 2) {
2 }

设备最小宽度321px到最大宽度1080px之间且最小密度比为1到最大密度比为2
1 @media (min-width:321px) and (max-width:1080px) and (-webkit-min-device-pixel-ratio: 1) and(-webkit-max-device-pixel-ratio: 2) {
2 }

设备最小宽度321px到最大宽度1080px之间且密度比为2
1 @media (min-width:321px) and (max-width:1080px) and (-webkit-device-pixel-ratio: 2) {
2 }


规定段落中的文本单行且溢出部分显示...

1 p{
2     white-space:nowrap;text-overflow:ellipsis;overflow:hidden;
3 }

文本控制显示行
1 p{
2     /*这个是想显示几行就写几*/-webkit-line-clamp:3;overflow:hidden;text-overflow:ellipsis;-webkit-box-orient:vertical;
3 }

英文字体允许换行
1 p{word-break:break-word;}

box-sizing盒子宽度
1 div{  
2     box-sizing:border-box;-moz-box-sizing:border-box;/* Firefox */-webkit-box-sizing:border-box;/* Safari */ 
3 } 
4 /*content-box: 
5     这是由 CSS2.1 规定的宽度高度行为。 
6     宽度和高度分别应用到元素的内容框。 
7     在宽度和高度之外绘制元素的内边距和边框 
8 border-box: 
9     为元素设定的宽度和高度决定了元素的边框盒。
10     就是说，为元素指定的任何内边距和边框都将在已设定的宽度和高度内进行绘制。
11     通过从已设定的宽度和高度分别减去边框和内边距才能得到内容的宽度和高度。*/

css3旋转角度
div{
	transform:rotate(90deg);-webkit-transform:rotate(90deg);-o-transform:rotate(90deg);-moz-transfomr:rotate(90deg);
}

css3渐变
1 /*最简单的写法:*/
2 background:-webkit-linear-gradient(left,#ffffff,#ffffff);
3 /*渐变颜色*/
4 -webkit-linear-gradient(left,startColor,endColor);
5 /*left位置,startColor起始颜色,endColor结束颜色background-image:-webkit-linear-gradient(left,rgba(255,255,255,0),rgba(255,255,255,1));*/

css3阴影shadow
1 img{
2     -moz-box-shadow:2px 2px 5px e69696;/*firefox*/-webkit-box-shadow:2px 2px 5px e69696;/*webkit*/box-shadow:2px 2px 5px e69696;/*opera或ie9*/    
3 }
4 /*语法box-shadow: h-shadow v-shadow blur spread color inset;*/

段落的行缩进
1 p{
2     text-indent:20px;
3 }
4 /*这是兼容写法与text-indent一样*/
5 p:empty{
6     padding-left:2%;
7 }

盒子模型分布，与自适应占位
1 /* 
2 box-flex: 
3     子容器将父容器的宽度等份分,有几个li就几个等份宽度的li; 
4     如果其中一个li设置了固定的宽度而别的li没有设置,则父容器的宽度减去固定li的宽度后在进行等份分; 
5 */ 
6 ul li{ 
7     box-flex:1;-webkit-box-flex:1;-moz-box-flex:1;display:block; 
8 } 
9 ul{
10     display:box;display:-webkit-box;display:-moz-box;
11 }

未完待续...
