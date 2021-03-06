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

# CSS Color

CSS colors can be obtained by: **Hex color**, **RGB color**, **RGBA color**, **HSL color**,
**HSLA color**, and **color name** definition.

## Hex Color

**Hex** color is a combination of **RR (red)**, **GG (green)**, **BB (blue)** color values. The value
range is **`00`** - **`FF`** Between, starting with the **`#`** symbol.

| Parameter | Description |
| :--- | :--- |
| **RR** | Red value. Hexadecimal positive integer. |
| **GG** | Green value. Hexadecimal positive integer. |
| **BB** | Blue value. Hexadecimal positive integer.|

When the highest value of the range of values `FF` appears in the RR area, it is standard red:
`#FF0000`. Similarly, green is `#00FF00`, and blue is `##0000FF`.
Red plus green turns yellow so it is `#FFFF00` , green plus blue is sky blue
`#00FFFF`, red plus blue is purple both`#FF00FF`, white is `#FFFFFF`. Taking red as an example, we
only need to ensure that the value of the RR area is FF, and after adjusting the values of other
parts, we will get various reds.

The RGB color value law of the complaint is the same. When the other values are 0, the R, G, and B
positions where the highest value 255 appears are my corresponding standard colors.

If each parameter is on its own **the numbers in both digits are the same**, the unit can also be
abbreviated as **#RGB**. For example: **`#FF8800`** can be abbreviated to **`#F80`**.

```css
p {
  background: #FF8800;
}
```

## RGB Color: `rgb()`

**RGB color** defines the intensity of the color through **red (R)**, **green (G)**, and **blue (B)**.

Three parameters for **RGB color values**

| Parameter | Description |
| :--- | :--- |
| **R** | Red value. **Positive integer** or **percentage** |
| **G** | Green value. **Positive integer** or **percentage** |
| **B** | Blue value. **Positive integer** or **percentage** |

- Positive integer values can range from **`0`** to **`255`**.The combination of red, green, and blue
  values from 0 to 255 gives a total of more than 16 million different colors (256 × 256 ×256).
  Most modern monitors are capable of displaying *at least 16,384 colors*.
- The percentage value ranges from **`0.0%`** to **`100.0%`**.

!!! info ""
    If the value is out of range, it will automatically take the nearest value. For example:
    `rgb(300,0,0)` will be automatically parsed as `rgb(255,0,0)`

```css
p {
  background: rgb(255, 0, 0);
}
```

## RGBA Color: `rgba()`

The **RGBA color value** is an extension of the **RGB color value** with an **alpha** channel-it
specifies the opacity of the object.

The **alpha** parameter is a number between **`0.0`** (fully transparent) and **`1.0`** (fully opaque).

```css
p {
  background: rgba(255, 0, 0, 0.5);
}
```

## HSL Color: `hsl()`

**HSL** is a cylindrical coordinate representation of points in the **RGB** color model. Refers to
**hue**, **saturation**, **lightness**

Three parameters for **HSL color values**

| Parameter | Description |
| :--- | :--- |
| **H** | It is the basic attribute of color, which is usually the color name, such as red, yellow and so on. Values: **`0`** - **`360`** |
| **S** | Refers to the purity of the color. The higher the color, the purer, and the lower the color will gradually become gray. Values: **`0.0%`** - **`100.0%`** |
| **L** | brightness. Values: **`0.0%`** - **`100.0%`** |

```css
p {
  background: hsl(120, 65%, 75%);
}
```

## HSLA Color: `hsla()`

The **HSLA color value** is an extension of the **HSL color value** with an **alpha** channel-it
specifies the opacity of the object.

The **alpha** parameter is a number between **`0.0`** (fully transparent) and **`1.0`** (fully opaque).

```css
p {
  background: hsla(120, 65%, 75%, 0.3);
}
```

## Color Name

CSS **color names** are defined by 147 colors, such as **red**, **yellow**, **blue**, etc.

There are 17 standard colors: **aqua**, **black**, **blue**, **fuchsia**, **gray**, **green**,
**lime**, **maroon**, **navy**, **olive**, **orange**, **purple**, **red**, **silver**, **teal**,
**white**, **yellow**

```css
p {
  background: red;
}
```
