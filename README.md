# DOMtest
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        .ct {
            width: 100%;
            height: 120px;
            border: 2px solid #ccc;
            box-shadow: 1px 1px 2px 2px rgba(0,0,0,0.14);
        }
        h1,p {
            margin: 15px;
        }
        button {
            padding: 8px;
            margin-top: 20px;
            margin-left: 20px;
        }
        .ct.active {
            background-color: black;
            color: #fff;
        }
    </style>
</head>
<body>
    <div class="ct">
        <h1>I love you thousand</h1>
        <p>More than</p>
    </div>
    <button class="add">add</button>
    <button class="remove">remove</button>
    <button class="toggle1">t1</button>
    <button class="toggle2">t2</button>
    <script>
        var addBtn = document.querySelector('.add')
        var remBtn = document.querySelector('.remove')
        var t1Btn = document.querySelector('.toggle1')
        var t2Btn = document.querySelector('.toggle2')
        var ctDiv = document.querySelector('.ct')
        addBtn.onclick = function(){
            ctDiv.classList.add('active')
        }
        remBtn.onclick = function(){
            ctDiv.classList.remove('active')
        }
        t1Btn.onclick = function(){
            if(ctDiv.classList.contains('active')){
                ctDiv.classList.remove('active')
            }else{
                ctDiv.classList.add('active')
            }
        }
        t2Btn.onclick = function(){
            ctDiv.classList.toggle('active')
        }
    </script>
</body>
</html>
```
