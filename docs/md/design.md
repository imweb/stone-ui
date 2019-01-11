### 颜色使用

#### 黑白灰色

一般来说，颜色使用遵循规则如下：

- 文字色：black、gray、grayLight、white。
- 边框色：grayLine。
- 背景色：grayBg、grayBgLight。

在实际开发中，除了 black 和 white 之外，其余的都已经定义为颜色变量，如 `var(--gray)`，表示使用 `#777777`。

![](md/img/color1.png)

#### 主色、成功失败色等

浅色用于图标或背景，深色用于文字。

实际开发中，purple 和 blueDeep 不会用到，所以不用定义。其余的 6 个颜色只定义了浅色的三个变量（blue、red、green），深色的都是通过颜色函数转换过来的，转换规则为：将浅色降低透明度10%得到深色。如要得到 blueDark，则转换规则为：`color(var(--blue) l(-10%))`。

默认主色为 blue

![](md/img/color2.png)
