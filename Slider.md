Slider
=====================

![](https://github.com/rey5137/Material/raw/master/image/slider_continuous.gif)
![](https://github.com/rey5137/Material/raw/master/image/slider_discrete.gif)

Usage
------------
  Declare in XML:

```xml
    <!-- use Material.Widget.Slider.Discrete style for discrete mode -->
    <com.rey.material.widget.Slider
        style="@style/Material.Widget.Slider"  
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:gravity="center"
        app:sl_minValue="0"
        app:sl_maxValue="100"
        app:sl_value="50"/>
```
   

Attributes
------------

* `sl_trackSize` - The stroke's width of the track bar.

* `sl_trackCap` - The cap setting of track bar.

* `sl_primaryColor` - The foreground color of track bar and thumb.

* `sl_secondaryColor` - The background color of track bar.

* `sl_thumbBorderSize` - The border's width of thumb.

* `sl_thumbRadius` - The radius of thumb.

* `sl_thumbFocusRadius` - The radius of thumb when focused.

* `sl_thumbTouchRadius` -  The radius of touch region. if not set will use `sl_thumbRadius`.

* `sl_travelAnimDuration` - The max time the thumb takes to move from left to right side.

* `sl_transformAnimDuration` - The duration of animation when thumb switch to focused state.

* `sl_interpolator` - The interpolator of animations.

* `sl_minValue` - The min value of slider.

* `sl_maxValue` - The max value of slider.

* `sl_stepValue` - The step value of slider (used in **discrete** mode).

* `sl_value` - The current value of slider.

* `sl_discreteMode` - If true, slider is in **discrete** mode, false and slider is in **continuous** mode

* `sl_fontFamily` - The fontFamily of text (used in **discrete** mode).

* `sl_textStyle` - The style of text (used in **discrete** mode).

* `sl_textSize` - The size of text (used in **discrete** mode).

* `sl_textColor` - The color of text (used in **discrete** mode).

* `sl_alwaysFillThumb` - Indicate that should always fill thumb at min value or not.