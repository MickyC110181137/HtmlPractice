Cursor效果介紹
![image](https://github.com/MickyC110181137/Index/tree/main/video/Cursor.gif)
```javascript
const cursor = document.querySelector('.cursor');
// 為整個文件綁定滑鼠移動事件
document.addEventListener('mousemove', function(e) {
    // 將游標元素的 left 設為滑鼠目前的 X 座標（以頁面為基準）
    cursor.style.left = e.pageX + 'px';
    // 將游標元素的 top 設為滑鼠目前的 Y 座標
    cursor.style.top = e.pageY + 'px';
    //e.pageX 與 e.pageY：取得滑鼠相對於整個網頁左上角的位置（不是相對視窗）。  
    //cursor.style.left/top：透過修改 CSS left/top 屬性，讓 .cursor 元素移動到滑鼠位置。  
    //因為 .cursor 是 position: fixed 且設了 transform: translate(-50%, -50%)，所以游標會自動以中心點對齊滑鼠。  
});

