# transform
This is transform's note
transform 旋转、平移、缩放、扭曲
旋转   
rotate(？deg); Z轴旋转
rotateX(？deg); X轴旋转
rotateY(？deg); Y轴旋转
                                                        deg 是度；
平移
translate(x,y);                  x轴和y轴平移
translateZ(px); Z轴平移    在这z轴就不解释了，z轴就是垂直你电脑画面，不理解的话想想当你写代码写烦了，用手砸穿了你的显示器的画面，你的手臂就是那条z轴；

缩放
scale(x,y); 默认是1  缩放原大小的多少陪，缩放到0 的时候是消失了，负值时是颠倒了元素，这里解释的不是很                                                         清楚，自己改变值看效果更好些！
                 scale(-1,1);                     x -1时相当于是把元素扣在了页面   负值越大时，相当于扣在页面后又把他拉伸了绝对值陪
原样：                                                                                                             scale(-1,1); 后：
图片          图片
扭曲(拉伸)
skew(xdeg,ydeg);   

transform 在工作中用的非常多
 优点：性能高。不会改变盒子模型。
不会触发重排。重绘。

注意： **
1.行元素操作不了。
2.transform中的值，有先后顺序。
后写的先执行，先写的后执行。
      这里是说 transform：扭曲，缩放  ； 效果是先执行的缩放，在执行的扭曲

透视
perspective(px);数值越小越明显
推荐 800-1200

开启3D模式
-webkit-transform-style:preserve-3d;
            只有操作translateZ的时候才可以开启3D模式
 
正反面
父级 开启3D
正反  translateZ(1px);
反面 translateZ(-1px) scale(-1,1);
