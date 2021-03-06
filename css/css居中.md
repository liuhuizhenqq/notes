### 垂直水平居中
#### 1. margin: auto
```
<style>
.parent {
    background: green;
    width: 100px;
    height: 100px;
    position: relative;
}
.child {
    background: yellow;
    width: 50px;
    height: 50px;
    position: absolute; // 1
    top: 0; // 2
    left: 0; // 3
    right: 0; // 4
    bottom: 0; // 5
    margin: auto; // 6
}
</style>
</head>
<body>
<div class="parent">
<div class="child"></div>
</div>
</body>
```

#### 2. left: 50%; margin-left: -二分之一元素的宽度
```
<style>
.parent {
    background: green;
    width: 100px;
    height: 100px;
    position: relative;
}
.child {
    background: yellow;
    width: 50px;
    height: 50px;
    position: absolute; 
    top: 50%;
    left: 50%;
    margin-left: -25px;
    margin-top: -25px;
}
</style>
</head>
<body>
<div class="parent">
<div class="child"></div>
</div>
</body>
```
#### 3. transform: translate(距离)
```
<style>
.parent {
    background: green;
    width: 120px;
    height: 100px;
    position: relative;
}
.child {
    position: absolute;
    background: yellow;
    width: 60px;
    height: 50px;

    top: 50%; /* child 垂直居中 */
    left: 50%;
    /* transform: translateY(-50%) translateX(-50%); child 垂直居中 */
    transform: translate(-50%, -50%); /* child 垂直居中 */
</style>
</head>
<body>
<div class="parent">
<div class="child"></div>
</div>
</body>
```

#### 4. padding
```
<style>
.parent1 {
    background: green;
    width: 100px;
    height: 100px;

    padding: 25px; /* child 水平、垂直居中 */
}
.child1 {
    background: yellow;
    width: 50px;
    height: 50px;
}
</style>
</head>
<body>
<div class="parent1">
<div class="child1"></div>
</div>
</body>
```

#### 5. line-height、text-align
```
<style>
.child1 {
    background: yellow;
    width: 100px;
    height: 50px;
    line-height: 50px; /* child 垂直居中 */
    text-align: center; /* child 水平居中 */
}
</style>
</head>
<body>
<div class="child1">abcdefg</div>
</body>
```

#### 6. flex、主轴为水平轴（默认）
默认 flex 主轴为水平轴，justify-content 为主轴的排列方式，align-items 为交叉轴的排列方式

```
<style>
.parent1 {
    background: green;
    width: 100px;
    height: 100px;

    display: flex;
    align-items: center; /* child 垂直居中 */
    justify-content: center; /* child 水平居中 */
}
.child1 {
    background: yellow;
    width: 50px;
    height: 50px;
}
</style>
</head>
<body>
<div class="parent1">
<div class="child1"></div>
</div>
</body>
```

#### 7. flex、flex-direction
通过用 ```flex-direction: column;```改变主轴的方向

```
<style>
.parent {
    background: green;
    width: 100px;
    height: 100px;

    display: flex;
    flex-direction: column;
    align-items: center; /* child 水平居中 */
    justify-content: center; /* child 垂直居中 */
}
.child {
    background: yellow;
    width: 50px;
    height: 50px;
}
</style>
</head>
<body>
<div class="parent">
<div class="child"></div>
</div>
</body>
```

#### 8. display: table-cell
```
<style>
.parent {
    background: green;
    width: 100px;
    height: 100px;

    display: table-cell;
    vertical-align: middle; /* child 垂直居中 */
    text-align: -webkit-center; /* child 水平居中 */
}
.child {
    background: yellow;
    width: 50px;
    height: 50px;
}
</style>
</head>
<body>
<div class="parent">
<div class="child"></div>
</div>
</body>
```