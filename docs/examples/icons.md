# Icons

PyWaffle supports [Font Awesome icons](https://fontawesome.com/). Blocks could be icons instead of squares.

```python
fig = plt.figure(
    FigureClass=Waffle,
    rows=5,
    columns=10,
    values=[48, 46, 3],
    colors=["#232066", "#983D3D", "#DCB732"],
    icons='child',
    icon_size=12,
)
```
    
<img class="img_middle" alt="Icons" src="https://raw.githubusercontent.com/gyli/PyWaffle/master/examples/docs/icons.svg?sanitize=true">

Categories could have different icon settings by passing parameter `icons` a list or tuple of icon names. The length must be the same as `values`.

In Font Awesome Icons, there are different icon sets in different styles, including Solid, Regular and Brands. It can be specified through parameter `icon_set`.

With `icon_legend`=`True`, the symbol in legend would be the icon. Otherwise, it would be a color bar.

```python
fig = plt.figure(
    FigureClass=Waffle,
    rows=5,
    values=[48, 46, 3],
    colors=["#FFA500", "#4384FF", "#C0C0C0"],
    icons=['sun', 'cloud-showers-heavy', 'snowflake'],
    icon_size=12,
    icon_set='solid',
    icon_legend=True,
    legend={
        'labels': ['sun', 'shower', 'snow'], 
        'loc': 'upper left', 
        'bbox_to_anchor': (1, 1)
    }
)
```

<img class="img_middle" alt="Icons per category" src="https://raw.githubusercontent.com/gyli/PyWaffle/master/examples/docs/icons_different_per_category.svg?sanitize=true">