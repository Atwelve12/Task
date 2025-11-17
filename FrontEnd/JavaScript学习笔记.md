# JavaScript学习笔记

```javascript
var x=1//赋值
//javascript对末尾的;并不敏感
if(){

}

//与c语言类似
```

JavaScript不区分整数和浮点数，统一用Number表示.

`==`比较会自动转换数据类型

`===`比较不会转换数据类型



`NaN`

```javascript
NaN === NaN; // false

isNaN(NaN); // true
```

```javascript
Math.abs(1 / 3 - (1 - 2 / 3)) < 0.0000001; // true
//比较浮点数
```

```javascript
let s = 'Hello, world!';
s.length; // 13

s[0]; // 'H'
s[6]; // ' '
s[7]; // 'w'
s[12]; // '!'
s[13]; // undefined 超出范围的索引不会报错，但一律返回undefined


```

****

```javascript
//定义函数
function abs(x) {
    if (x >= 0) {
        return x;
    } else {
        return -x;
    }
}
```



****



```html
<ul>
        <li onclick="playSong('song1.mp3')">歌曲1</li>
        <li onclick="playSong('song2.mp3')">歌曲2</li>
        <li onclick="playSong('song3.mp3')">歌曲3</li>
    </ul>

```

`onclick`点击事件,执行playsong函数

```javascript
function playSong(url){
    const music = +
}
//与c语言类似
```

****


