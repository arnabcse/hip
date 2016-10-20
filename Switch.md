CheckBox
=====================

![](https://github.com/rey5137/Material/raw/master/image/cb.gif)  

Usage
------------
  Declare in XML:

```xml
    <com.rey.material.widget.CheckBox
        style="@style/Material.Drawable.CheckBox"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Check box"/>
```

Attributes
------------

* `cbd_width` - The width of the CheckBoxDrawable.

* `cbd_height` - The height of the CheckBoxDrawable.

* `cbd_boxSize` - The size of square box.

* `cbd_cornerRadius` - The corner radius of box.

* `cbd_strokeSize` - The size of stroke.

* `cbd_strokeColor` - The color of stroke. Accept Color value or ColorStateList resource.

* `cbd_tickColor` - The color of tick mark.

* `cbd_animDuration` - The duration of animation when switch checked state.

RadioButton
=====================

![](https://github.com/rey5137/Material/raw/master/image/rb.gif)  

Usage
------------
  Declare in XML:

```xml
    <com.rey.material.widget.RadioButton
        style="@style/Material.Drawable.RadioButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Radio Button"/>
```

Attributes
------------

* `rbd_width` - The width of the RadioButtonDrawable.

* `rbd_height` - The height of the RadioButtonDrawable.

* `rbd_radius` - The radius of the box.

* `rbd_innerRadius` - The radius of tick box.

* `rbd_strokeSize` - The size of stroke.

* `rbd_strokeColor` - The color of stroke. Accept Color value or ColorStateList resource.

* `rbd_animDuration` - The duration of animation when switch checked state.

Switch
=====================

![](https://github.com/rey5137/Material/raw/master/image/switch.gif)  


Usage
------------
  Declare in XML:

```xml
    <com.rey.material.widget.Switch
        style="@style/Material.Widget.Switch"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:gravity="center"
        android:checked="false"/>
```

Attributes
------------

*默认选中状态的sw_trackColor与sw_thumbColor为colorAccent
*单纯更改sw_trackColor与sw_thumbColor，其颜色都被改变，不受状态的影响

* `sw_trackSize` - The stroke's width of track bar.

* `sw_trackColor` - The color of track bar. Accept Color value or ColorStateList resource.

* `sw_trackCap` - The cap setting of track bar. There're 3 types: **butt**, **round** and **square**.

* `sw_thumbColor` - The color of thumb. Accept Color value or ColorStateList resource.

* `sw_thumbRadius` - The radius of thumb.

* `sw_thumbElevation` - The elevation of thumb.

* `sw_animDuration` - The duration of animation when switch checked state.

* `sw_interpolator` - The interpolator of animation when switch checked state.