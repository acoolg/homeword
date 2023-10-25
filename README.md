# homeword
---
**這是我的無聊網站:https://acoolg.github.io/homeword/**  
備註:跟課程相關  
index.html  
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>分數評級</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <input type="text" placeholder="分數" id="i">
    <button onclick="submit()">提交</button>
    <br>
    <div id="v">
    </div>
    <script>
        console.log('h')
        var i = document.getElementById('i')
        var v = document.getElementById('v')

        function tolog(text) {
            v.innerHTML = text
        }

        function submit() {
            var score = parseFloat(i.value);
            if (!isNaN(score)) {
                if (score >= 90) {
                    tolog('優等')
                } else if (score >= 80) {
                    tolog('甲等')
                } else if (score >= 70) {
                    tolog('乙等')
                } else if (score >= 60) {
                    tolog('丙等')
                } else {
                    tolog('丁等')
                }
            } else {
                tolog('請輸入有效的分數')
            }
        }
    </script>
</body>
</html>

```
style.css  
```css
body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    text-align: center;
}

input[type="text"] {
    padding: 10px;
    font-size: 16px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

button {
    padding: 10px 20px;
    font-size: 16px;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}

#v {
    margin-top: 20px;
    font-size: 24px;
    color: #333;
}
```
