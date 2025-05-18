```javascript
const cursor = document.querySelector('.cursor');
// 為整個文件綁定滑鼠移動事件
document.addEventListener('mousemove', function(e) {
    // 將游標元素的 left 設為滑鼠目前的 X 座標（以頁面為基準）
    cursor.style.left = e.pageX + 'px';

    // 將游標元素的 top 設為滑鼠目前的 Y 座標
    cursor.style.top = e.pageY + 'px';
});
