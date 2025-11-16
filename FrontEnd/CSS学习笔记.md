# CSS学习笔记

****

## 一些CSS设置

```css
//定义全局变量
:root {
    --pink： #ff726b;
    card-bg: rgba(255, 255, 255, 0.9);

}
body {
    color: var(--pink);
//使用变量，定义字体颜色
}
```

```css
rgba(红色, 绿色, 蓝色, 透明度)

z-index:数值；
/*控制元素在z轴上的堆叠顺序*/

border-radius: 5px /*添加圆角*/

margin: 25px 50px 75px 100px;
/*上外边距是 25px
右外边距是 50px
下外边距是 75px
左外边距是 100px*/

box-shadow: 水平偏移 垂直偏移 模糊半径 扩散半径 颜色 内/外阴影;

animation: name 15s infinite ease-in-out; /* name 动画时间 重复次数无限  慢速开始和结束*/
```

```css
@keyframes name {

}
```

****

## @keyframes动画设置

```css
0%{

}
100%{
    transform:  /*旋转*/
}
```

```css
animation-duration: 3s;
animation-name:name;
animation-timing-function: ease-in-out;
animation-delay: 1s;
animation-iteration-count: 3;
animation-direction: alternate;
```

****

## 悬停设置

```css
.name:hover {
    /*悬停后的效果*/
     transform: ;

}
```

`transition: all 0.3s ease;`:设置过度效果

`cursor: pointer;`让鼠标变成小手





****



## 添加卡片跳出效果

`opacity: 0`:设置初始隐藏

设置相对定位和绝对定位

```css
/* 初始状态：隐藏卡片 */
.musiclist {
    opacity: 0;
    visibility: hidden;
    transform: translateX(-20px);
    transition: all 0.4s ease-in-out;
}

/* 悬停时显示卡片 */
.photo-container:hover .musiclist {
    opacity: 1;
    visibility: visible;
    transform: translateX(0);
}
```



****



## 如何在网页添加图片

```css
<img src="你的图片地址.jpg" alt="图片描述">
```









****



## 渐变背景的一种实现方法

* **背景设置**
  
  ```css
  body {
            margin:  0;
            padding: 0;
            height: 100vh;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45b7d1, #96ceb4);
            background-size: 400% 400%;
          background-attachment: fixed;/*让背景固定*/
            animation: gradientBG 15s ease infinite;
        }
  ```

> * `margin: 0; padding: 0;` - 清除默认边距，让背景充满整个屏幕
> 
> * `height: 100vh;` - 设置高度为100%视口高度（viewport height）
> 
> * `background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45b7d1, #96ceb4);` - 创建45度角的多色线性渐变

> * `background-size: 400% 400%;` - **关键技巧**：将背景放大4倍，为动画创造移动空间

> * `animation: gradientBG 15s ease infinite;` - 应用动画：

> * `gradientBG` - 动画名称

> * `15s` - 动画时长15秒

> * `ease` - 缓动函数，让动画更自然

> * `infinite` - 无限循环

**效果**

![效果](https://github.com/Atwelve12/Task/blob/e48946905ef712a1454ae6ea075e2c319bb2803c/photo/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-11-11%20195505.png)

* **@keyframes动画**

```css
@keyframes gradientBG { 
    0% {
     background-position: 0% 50%;
     } 
    50% {     
    background-position: 100% 50%;
     }
     100% {
     background-position: 0% 50%; 
    }
}
```

> `background-position: 0% 50%;`-背景位置,水平位置,垂直位置[^位置]

****

* 
  
  ```css
  .divname {
    padding: 50px;
    color: white;
    text-align: center;
    font-family: Arial, sans-serif;
  }
  ```

> * `padding: 50px;` - 内边距，让内容有呼吸空间
> 
> * `color: white;` - 白色文字，在彩色背景上保持可读性
> 
> * `text-align: center;` - 文字居中对齐
> 
> * `font-family: Arial, sans-serif;` - 设置字体族



****















[^位置]: 水平位置：0% 表示背景图像的左边缘与容器的左边缘对齐，100% 表示背景图像的右边缘与容器的右边缘对齐。  
垂直位置：50% 表示背景图像的垂直中心与容器的垂直中心对齐。
