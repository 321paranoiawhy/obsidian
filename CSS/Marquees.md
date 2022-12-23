# `HTML`

```HTML
<marquee>This text will scroll from right to left</marquee>

<marquee direction="up">This text will scroll from bottom to top</marquee>
```

# `CSS`

```HTML
<div class="bounce">Bouncing text...</div>
```

```CSS
/* 水平滚动 */

/* 兼容处理 */
/* @-moz-keyframes */
/* @-webkit-keyframes */
@keyframes bouncing-text {
  0% {
    -moz-transform: translateX(50%); /* Browser bug fix */
    -webkit-transform: translateX(50%); /* Browser bug fix */
    transform: translateX(50%);
  }
  100% {
    -moz-transform: translateX(-50%); /* Browser bug fix */
    -webkit-transform: translateX(-50%); /* Browser bug fix */
    transform: translateX(-50%);
  }
}

div.bounce {
	animation: bouncing-text 2s linear infinite alternate;
}
```
