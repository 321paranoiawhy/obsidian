# `overflow-y: auto;`

```css
div {
	position: relative;
	max-height: 200px;
	overflow-y: auto;
	--triangle-size: 10px;
	--triangle-background-color: red;
}

div::before {
	position: absolute;
	transform: translate(-100%, 100%);
	content: " ";
	border-top: var(--triangle-size) solid transparent;
	border-left: var(--triangle-size) solid transparent;
	border-right: var(--triangle-size) solid var(--triangle-background-color);
	border-bottom: var(--triangle-size) solid transparent;
}
```

须修改为:

```css
div::before {
	position: fixed;
}
```