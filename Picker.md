TimePickerDialog
=====================

  `com.rey.material.app.TimePickerDialog` is a dialog extends from `com.rey.material.app.Dialog` and provide a time picker view.

![](https://github.com/rey5137/Material/raw/master/image/dialog_3.png)

Attributes
------------

   It accepts all attributes for `com.rey.material.app.Dialog` beside custom attributes.

* `tp_backgroundColor` - The color of background circle.

* `tp_selectionColor` - The color of selection circle.

* `tp_selectionRadius` - The radius of selection circle.

* `tp_tickSize` - The size of tick's stroke.

* `tp_fontFamily` - The fontFamily of text.

* `tp_textStyle` - The style of text.

* `tp_textSize` - The size of text.

* `tp_textColor` - The color of text.

* `tp_textHighlightColor` - The color of text when is highlighted.

* `tp_animDuration` - The duration of animations.

* `tp_inInterpolator` - The interpolator of in animation.

* `tp_outInterpolator` - The interpolator of out animation.

* `tp_mode` - The current select mode of time picker. There're 2 modes: **HOUR** and **MINUTE**.

* `tp_24Hour` - Indicate should show hour in 24 hours format or not.

* `tp_hour` - The current hour (in 24 hours format).

* `tp_minute` - The current minute.

* `tp_headerHeight` - The height of header view that shows the time text.

* `tp_textTimeColor` - The color of time text.

* `tp_textTimeSize` - The size of time text.

* `tp_am` - The custom label for AM button.

* `tp_pm` - The custom label for PM button.

* `tp_leadingZero` - Indicate that should show hour value in leading zero format.

DatePickerDialog
=====================

  `com.rey.material.app.DatePickerDialog` is a dialog extends from `com.rey.material.app.Dialog` and provide a date picker view.

![](https://github.com/rey5137/Material/raw/master/image/dialog_4.png)

Attributes
------------

   It accepts all attributes for `com.rey.material.app.Dialog` beside custom attributes.

* `dp_yearMin` - The year value of minimum date.

* `dp_monthMin` - The month value in [0..11] of minimum date.

* `dp_dayMin` - The day value in [1..) of minimum date.

* `dp_yearMax` - The year value of maximum date.

* `dp_monthMax` - The month value in [0..11] of maximum date.

* `dp_dayMax` - The day value in [1..) of maximum date.

* `dp_year` - The year value of selected date.

* `dp_month` - The month value in [0..11] of selected date.

* `dp_day` - The day value in [1..) of selected date.

* `dp_yearTextSize` - The size of item's text in year picker.

* `dp_yearItemHeight` - The height of item in year picker.

* `dp_dayTextSize` - The size of day text in month view.

* `dp_textLabelColor` - The color of label text in month view.

* `dp_textDisableColor` - The color of day text that's out of current date range.

* `dp_textHighlightColor` - The color of text when is highlighted.

* `dp_textColor` - The color of text.

* `dp_selectionColor` - The color of selection circle.

* `dp_animDuration` - The duration of animations.

* `dp_inInterpolator` - The interpolator of in animation.

* `dp_outInterpolator` - The interpolator of out animation.

* `dp_fontFamily` - The fontFamily of text.

* `dp_textStyle` - The style of text.

* `dp_headerPrimaryHeight` - The height of header view that show the date text.

* `dp_headerPrimaryColor` - The color of header view that show the date text.

* `dp_headerSecondaryHeight` - The height of header view that show the day of week text.

* `dp_headerSecondaryColor` - The color of header view that show the day of week text.

* `dp_headerPrimaryTextSize` - The size of text in primary header view.

* `dp_headerSecondaryTextSize` - The size of text in secondary header view.

* `dp_textHeaderColor` - The color of text in header view.
