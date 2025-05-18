# 此專案為純html練習，包含 CursorEffect, ScrollBar Effect, SliderImg  

## 1.Cursor效果  

![image](https://github.com/MickyC110181137/Index/blob/main/video/Cursor.gif)

```javascript
const cursor = document.querySelector('.cursor');
document.addEventListener('mousemove', function(e) {
    // 將游標元素的 left 設為滑鼠目前的 X 座標（以頁面為基準）
    cursor.style.left = e.pageX + 'px';
    // 將游標元素的 top 設為滑鼠目前的 Y 座標
    cursor.style.top = e.pageY + 'px';
    //e.pageX 與 e.pageY：取得滑鼠相對於整個網頁左上角的位置（不是相對視窗）。  
    //cursor.style.left/top：透過修改 CSS left/top 屬性，讓 .cursor 元素移動到滑鼠位置。  
    //css .cursor 是 position: fixed 且設了 transform: translate(-50%, -50%)，所以游標會自動以中心點對齊滑鼠。  
});
```

## 2.ScrollBar效果  

![image](https://github.com/MickyC110181137/Index/blob/main/video/ScrollBar.gif)

```javascript
let bg = document.getElementById("bg");
let moon = document.getElementById("moon");
let mountain = document.getElementById("mountain");
let road = document.getElementById("road");
let text = document.getElementById("text"); 

window.addEventListener('scroll',function(){
    let value = window.scrollY;

    bg.style.top = value*0.5 +'px'
    moon.style.left = -value*0.5 +'px'
    mountain.style.top = -value*0.15 +'px'
    road.style.top = value*0.15 +'px'
    text.style.top = value*1 +'px'
})

let progress = document.getElementById('progressbar');
let totalHeight = document.body.scrollHeight - window.innerHeight;
window.onscroll = function(){
    let progressHeight = (window.pageYOffset/totalHeight) * 100;
    progress.style.height = progressHeight + "%"
}
```


## 3.SliderImg效果  

![image](https://github.com/MickyC110181137/Index/blob/main/video/SliderImg.gif)

