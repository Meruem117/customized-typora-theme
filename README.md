# Customized Theme

> Typora 客制化主题



## Q & A



Q: 客制化主题解决的主要矛盾是什么?

A: 虽然现在Typora的主题很多，但总不能满足所有程序员的需求，每个人都有自己喜欢的样式和风格，而修改现有的主题又需要花费时间去了解markdown和html的对应关系，以及markdown的样式与css选择器的对应关系，客制化主题正是为了减少这段时间而存在的。



Q: 如何实现客制化?

A: 使用css变量，将常用的一些属性抽象出来，供用户统一修改，简单可行且方便。



## 参数



### 背景

| name               |        css         |        description |                 default |
| ------------------ | :----------------: | -----------------: | ----------------------: |
| `--bg-img`         |    `background`    |       html背景图片 | `url(./mystyle/bg.jpg)` |
| `--write-bg-color` | `background-color` | 可书写部分背景颜色 |               `oldlace` |

> 侧边栏来自Typora自带主题中的 `Github` 主题



### 文字

| name           | css     | description | default          |
| -------------- | ------- | ----------- | ---------------- |
| `--text-size` | `font-size` | 文字大小    | `18px`          |
| `--text-color` | `color` | 文字颜色    | `black`          |
| `--a-color`    | `color` | 链接颜色    | `cornflowerblue` |

> 文字样式来自于Typora自带主题中的 `Newsprint` 主题



### 标题

| name                   | css            | description        | default   |
| ---------------------- | -------------- | ------------------ | --------- |
| `--h1-underline-style` | `border-style` | 一级标题下划线样式 | `double`  |
| `--h1-underline-color` | `border-color` | 一级标题下划线颜色 | `dimgray` |

> 默认只有 `h1` 标签有下划线，不需要下划线就设置颜色为 `transparent`，如果想要其他标题也有下划线则可以搜索 `h2-h6` 标签，复制 `h1` 标签的样式修改即可



### 分割线

| name           | css             | description | default   |
| -------------- | --------------- | ----------- | --------- |
| `--line-size`  | `border-bottom` | 分割线宽度  | `2px`     |
| `--line-style` | `border-style`  | 分割线样式  | `dashed`  |
| `--line-color` | `border-color`  | 分割线颜色  | `dimgray` |



### Markdown符号

| name           | css     | description      | default |
| -------------- | ------- | ---------------- | ------- |
| `--meta-color` | `color` | markdown符号颜色 | `red`   |

> Markdown符号具体指 # , *, -, +, `等，在鼠标点击标题，加粗的文字，代码段等元素时显示的符号



### 引用

| name                      | css                | description    | default       |
| ------------------------- | ------------------ | -------------- | ------------- |
| `--blockquote-bar-size`   | `border-left`      | 引用条粗细     | `3px`         |
| `--blockquote-bar-color`  | `border-color`     | 引用条颜色     | `limegreen`   |
| `--blockquote-bg-color`   | `background-color` | 引用背景颜色   | `transparent` |
| `--blockquote-text-color` | `color`            | 引用中文字颜色 | `darkgray`    |
| `--blockquote-a-color`    | `color`            | 引用中链接颜色 | `orangered`   |

> 引用的 `“` 符号来自于少数派主题 `sspai.css`



### 代码

| name                       | css                | description    | default    |
| -------------------------- | ------------------ | -------------- | ---------- |
| `  --code-bg-color`        | `background-color` | 代码段背景颜色 | `seashell` |
| `--code-border-style`      | `border-style`     | 代码段边框样式 | `dashed`   |
| `--code-border-color`      | `border`           | 代码段边框颜色 | `brown`    |
| `--codeblock-bg-color`     | `background-color` | 代码块背景颜色 | `seashell` |
| `--codeblock-border-style` | `border-style`     | 代码块边框样式 | `dashed`   |
| `--codeblock-border-color` | `border`           | 代码块边框颜色 | `brown`    |



### 表格

| name                     | css                | description        | default        |
| ------------------------ | ------------------ | ------------------ | -------------- |
| `--table-border-size`    | `border`           | 表格边框粗细       | `1px`          |
| `--table-border-style`   | `border-style`     | 表格边框样式       | `solid`        |
| `--table-border-color`   | `border-color`     | 表格边框颜色       | `lightgray`    |
| `--table-title-bg-color` | `background-color` | 标题行背景颜色     | `antiquewhite` |
| `--table-odd-bg-color`   | `background-color` | 奇数行背景颜色     | `ghostwhite`   |
| `--table-even-bg-color`  | `background-color` | 偶数行背景颜色     | `whitesmoke`   |
| `--table-hover-bg-color` | `background-color` | 鼠标悬停时背景颜色 | `bisque`       |



### 图片

| name                  | css             | description      | default         |
| --------------------- | --------------- | ---------------- | --------------- |
| `--img-border-size`   | `border`        | 图片边框粗细     | `1px`           |
| `--img-border-radius` | `border-radius` | 图片边框圆角大小 | `8px`           |
| `--img-border-style`  | `border-style`  | 图片边框样式     | `solid`         |
| `--img-border-color`  | `border-color`  | 图片边框颜色     | `burlywood`     |
| `--img-shadow-color`  | `box-shadow`    | 图片阴影颜色     | `darkslategray` |

> 图片部分没有修改多少样式，整个css部分也只有一个 `img` 选择器，如需diy样式可自行修改

-----

> 如需更多样式可自行diy



## 如何使用

首先，下载主题文件

```shell
git clone https://github.com/Meruem117/customized_typora_theme
```

将下载的文件拷贝到Typora主题文件下

> 快速打开主题文件夹
>
> 打开Typora --> 文件 --> 偏好设置 --> 外观 --> 打开主题文件夹

**修改参数**

修改 `customized.css` 最上方的变量即可



TODO:  添加更多可配置项

