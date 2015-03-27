Progress
=====================

  To show progress indicator, add the`com.rey.material.widget.ProgressView`to the layout.

Attributes
------------

* `pv_progressMode` - The mode of progress indicator. There are 4 modes: **INDETERMINATE**, **DETERMINATE**, **QUERY** and **BUFFER** (Circular progress has only 2 modes: **INDETERMINATE** and **DETERMINATE**).

* `pv_circular` - Set true to show circular progress, false to show linear progress.

* `pv_autostart` - If true, the progress will auto start when it becomes visible and stop when it's hided (only work in **INDETERMINATE** mode).

* `pv_progress` - The progress value in [0..1].

* `pv_secondaryProgress` - The secondary progress value in [0..1] (use in **BUFFER** mode).

* `pv_progressStyle` - The style of progress.


Circular Progress Style
----------------------