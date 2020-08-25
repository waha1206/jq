### 01-jquery 入口函數

```javascript
        $(function() {
            var btn = document.getElementById('btn')
            btn.onclick = function(e) {
                alert('哈嚕')
            }
        })
```

### 02-jquery 選擇器

第一種用法：可以接受一個回調函數，回調就是，在頁面加載完成後執行該函數

```javascript
$(function(){ ... })
```

第二種用法：接受一個 css 的選擇器 (  string )，返回選擇器對應 dom 節點的 jQuery 包裝對象

```javascript
var $btn = $(#btn)
```

第三種用法：

```javascript
var btn2 = $(btn[0]) // jQuery → DOM
var $btn = $(btn2) // 接受一個 dom 對象，轉成 jQuery 對象$(btn)
```

轉成 jQuery 的包裝對象後，就擁有了 jQuery .fn 上的方法

### 03-jquery 其他選擇器

```javascript
<body>
    <p>我是一個p</p>

    <div class="cd">我是第一個div</div>
    <div class="cd">我是第二個div</div>

    <script>
        $(function() {
            var $all = $('*')
            console.dir($all)

            var $dv = $('.cd') //取得所有 class = 'cd' 的標籤
            console.dir($dv)

            var dv = $dv[0] // 取得第一個選擇器
            console.log(dv.innerHTML)

        })
    </script>
</body>
```



