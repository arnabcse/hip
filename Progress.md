Progress
=====================

  To show progress indicator, add the`com.rey.material.widget.ProgressView`to the layout.

Attributes
------------

* `pv_progressMode` - The mode of progress indicator. There are 4 modes: **INDETERMINATE**, **DETERMINATE**, **QUERY** and **BUFFER** (Circular progress has only 2 modes: **INDETERMINATE** and **DETERMINATE**).

* `pv_circular` - Set true to show circular progress, false to show linear progress.

* `pv_autostart` - If true, the progress will auto start when it becomes visible and stop when it's hided (only work in **INDETERMINATE** mode).

* `pv_progress` - The progress value in [0..1]

* `pv_secondaryProgress` - The secondary progress value in [0..1] (use in **BUFFER** mode).

* `pv_progressStyle` - The style of progress drawable. Depend on "pv_circular" attribute, it'll create a CircularProgressDrawable or LinearProgressDrawable.


CircularProgressDrawable
--------------------------
  CircularProgressDrawable has support only 2 modes: **INDETERMINATE** and **DETERMINATE**.

##Attributes

* `cpd_padding` - The padding of progress with the boundary. The size of progress = min(width, height) - padding * 2.

* `cpd_initialAngle` - The start angle of progress [0..360]

* `cpd_maxSweepAngle` - The maximum sweep angle of progress.

* `cpd_minSweepAngle` - The minimum sweep angle of progress.

* `cpd_strokeSize` - The stroke's size of progress.

* `cpd_strokeColor` - The stroke's color of progress.

* `cpd_strokeSecondaryColor` - The stroke's color of secondary progress.

* `cpd_strokeColors` - The list of stroke's color (for **INDETERMINATE** mode).

* `cpd_reverse` - If true, progress will rotate counter-clockwise.

* `cpd_rotateDuration` - The duration 


