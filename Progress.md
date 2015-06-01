Progress
=====================

  To show progress indicator, add the`com.rey.material.widget.ProgressView` to the layout.

Usage
------------
  Declare in XML:

```xml
    <com.rey.material.widget.ProgressView
        android:layout_width="48dp"
        android:layout_height="48dp"
        app:pv_autostart="true"
        app:pv_circular="true"
        app:pv_progressStyle="@style/Material.Drawable.CircularProgress"
        app:pv_progressMode="indeterminate"/>
```

Attributes
------------

* `pv_progressMode` - The mode of progress indicator. There are 4 modes: **indeterminate**, **determinate**, **query** and **buffer** (Circular progress has only 2 modes: **indeterminate** and **determinate**).

* `pv_circular` - Set true to show circular progress, false to show linear progress.

* `pv_autostart` - If true, the progress will auto start when it becomes visible and stop when it's hided.

* `pv_progress` - The progress value in [0..1]

* `pv_secondaryProgress` - The secondary progress value in [0..1] (use in **buffer** mode).

* `pv_progressStyle` - The style of progress drawable. Depend on "pv_circular" attribute, it'll create a CircularProgressDrawable or LinearProgressDrawable.


CircularProgressDrawable
--------------------------
  CircularProgressDrawable has support only 2 modes: **indeterminate** and **determinate**.

![](https://github.com/rey5137/Material/raw/master/image/progress_circular_indeterminate.gif)  ![](https://github.com/rey5137/Material/raw/master/image/progress_circular_determinate.gif)

##Attributes

* `cpd_padding` - The padding of progress with the boundary. The size of progress = min(width, height) - padding * 2.

* `cpd_initialAngle` - The start angle of progress [0..360]

* `cpd_maxSweepAngle` - The maximum sweep angle of progress.

* `cpd_minSweepAngle` - The minimum sweep angle of progress.

* `cpd_strokeSize` - The stroke's size of progress.

* `cpd_strokeColor` - The stroke's color of progress.

* `cpd_strokeSecondaryColor` - The stroke's color of secondary progress.

* `cpd_strokeColors` - The array of colors will be used as stroke's color (for **indeterminate** mode).

* `cpd_reverse` - If true, progress will rotate counter-clockwise.

* `cpd_rotateDuration` - The time it take to rotate a cycle.

* `cpd_transformDuration` - the time it take to animate the sweep angle from minSweepAngle to maxSweepAngle.

* `cpd_keepDuration` - the time it keep the sweep angle at minSweepAngle and maxSweepAngle.

* `cpd_transformInterpolator` - The interpolator of transform animation.

* `cpd_inAnimDuration` - the duration of animation when progress start running.

* `cpd_outAnimDuration` - the duration of animation when progress stop running.

* `cpd_inStepColors` - The array of colors will be shown in start animation.

* `cpd_inStepPercent` - the percent each step color will take.


LinearProgressDrawable
--------------------------

![](https://github.com/rey5137/Material/raw/master/image/progress_linear_indeterminate.gif)  
![](https://github.com/rey5137/Material/raw/master/image/progress_linear_determinate.gif)
![](https://github.com/rey5137/Material/raw/master/image/progress_linear_query.gif)
![](https://github.com/rey5137/Material/raw/master/image/progress_linear_buffer.gif)

##Attributes

* `lpd_maxLineWidth` - The maximum width of progress (can be dimension or fraction).

* `lpd_minLineWidth` - The minimum width of progress (can be dimension or fraction).

* `lpd_strokeSize` - The stroke's size of progress.

* `lpd_strokeColor` - The stroke's color of progress.

* `lpd_strokeSecondaryColor` - The stroke's color of secondary progress.

* `lpd_strokeColors` - The list of stroke's color (for **indeterminate** mode).

* `lpd_reverse` - If true, progress will run from right to left.

* `lpd_travelDuration` - The time it take to run.

* `lpd_transformDuration` - the time it take to animate the progress's width from minLineWidth to maxLineWidth.

* `lpd_keepDuration` - the time it keep the progress's width at minLineWidth and maxLineWidth.

* `lpd_transformInterpolator` - The interpolator of transform animation.

* `lpd_inAnimDuration` - the duration of animation when progress start running.

* `lpd_outAnimDuration` - the duration of animation when progress stop running.

* `lpd_verticalAlign` - the vertical align of progress with boundary. There're 3 values: **top**, **center** and   **bottom**.
