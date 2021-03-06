TOPICS: CSS color
        rgb()
        rgba()
        hsl()
        hsla()
        aqua
        black
        blue
        fuchsia
        gray
        green
        lime
        maroon
        navy
        olive
        orange
        purple
        red
        silver
        teal
        white
        yellow

# CSS 颜色

CSS 颜色可以通过: **十六进制色**、**RGB 颜色**、**RGBA 颜色**、**HSL 颜色**、**HSLA 颜色** 以及 **颜色名** 来定义。

## 十六进制颜色

**十六进制 (hex)** 颜色是由 **RR (红色)**、**GG (绿色)**、**BB (蓝色)** 颜色值的结合。取值范围为 **`00`** - **`FF`**
之间，以 **`＃`** 符号开始。

| 参数 | 描述 |
| :--- | :--- |
| **RR** | 红色值。十六进制正整数。 |
| **GG** | 绿色值。十六进制正整数。 |
| **BB** | 蓝色值。十六进制正整数。 |

当取值范围最高值 `FF`出现在RR区域时为标准红色既: `#FF0000`，同理，绿色为 `#00FF00` , 蓝色 `#0000FF`。红加绿变黄所以为 `#FFFF00`,绿加蓝为天蓝既
`#00FFFF`,红加蓝为紫既 `#FF00FF`,白色为 `#FFFFFF`。还以红色为例我们只要保证 RR区域的值为FF，其他部分的值调整后会得到各种不同的红。
下诉的RGB的颜色取值规律也一样，当其他值为0时，最高值255出现在什么R、G、B那个位置处就我对应的标准色。

如果每个参数各自在**两位上的数字都相同**，那么本单位也可缩写为 **#RGB** 的方式。例如：**`#FF8800`** 可以缩写为 **`#F80`**。

```css
p {
  background: #FF8800;
}
```

## RGB 颜色: `rgb()`

**RGB 颜色** 是通过 **红(R)**、**绿(G)**、**蓝(B)** 来定义颜色的强度。

**RGB 颜色值**的三个参数

| 参数 | 描述 |
| :--- | :--- |
| **R** | 红色值。**正整数** 或 **百分数**。 |
| **G** | 绿色值。**正整数** 或 **百分数**。 |
| **B** | 蓝色值。**正整数** 或 **百分数**。|

- 正整数值的取值范围为：**`0`** - **`255`**。红，绿，蓝值从0到255的结合，给出了总额超过1600多万不同的颜色（256 × 256 ×256）。现代大多数显示器能够显示 *至少16384种颜色*。
- 百分数值的取值范围为：**`0.0%`** - **`100.0%`**。

!!! info ""
    如果超出范围的数值会自动取最接近的值。如：`rgb(300,0,0)` 会自动解析为 `rgb(255,0,0)`

```css
p {
  background: rgb(255, 0, 0);
}
```

## RGBA 颜色: `rgba()`

**RGBA 颜色值** 是 **RGB 颜色值** 的扩展，A表示带有一个 **alpha** 通道 - 它规定了对象的不透明度。

**alpha** 参数是介于 **`0.0`**（完全透明）与 **`1.0`**（完全不透明）的数字。

```css
p {
  background: rgba(255, 0, 0, 0.5);
}
```

## HSL 颜色: `hsl()`

**HSL** 是一种将 **RGB** 色彩模型中的点在柱面坐标表示法。指的是 **hue（色调）**、**saturation（饱和度）**、**lightness（亮度）**

**HSL 颜色值**的三个参数

| 参数 | 描述 |
| :--- | :--- |
| **H** | 是色彩的基本属性，就是平常所说的颜色名称，如红色、黄色等。取值为：**`0`** - **`360`**。 |
| **S** | 是指色彩的纯度，越高色彩越纯，低则逐渐变灰。取值为：**`0.0%`** - **`100.0%`**。 |
| **L** | 亮度。取值为：**`0.0%`** - **`100.0%`**。 |

```css
p {
  background: hsl(120, 65%, 75%);
}
```

## HSLA 颜色: `hsla()`

**HSLA 颜色值** 是 **HSL 颜色值**的扩展，A表示带有一个 **alpha** 通道 - 它规定了对象的不透明度。

**alpha** 参数是介于 **`0.0`**（完全透明）与 **`1.0`**（完全不透明）的数字。

```css
p {
  background: hsla(120, 65%, 75%, 0.3);
}
```

## 颜色名

CSS **颜色名**是由 **red**, **yellow**, **blue** 等 147 名颜色定义。

其中有 17 种标准色是: **aqua**, **black**, **blue**, **fuchsia**, **gray**, **green**, **lime**, **maroon**,
**navy**, **olive**, **orange**, **purple**, **red**, **silver**, **teal**, **white**, **yellow**

```css
p {
  background: red;
}
```
