EditText
=====================

  `com.rey.material.widget.EditText`is a custom view that wrapped a `android.widget.EditText` and provide many features like Material Design style, floating label, char counter, ...

![](https://github.com/rey5137/Material/raw/master/image/textfield.gif)


Attributes
------------

  It accepts all default attributes for `android.widget.EditText` beside custom attributes.

* `et_inputId` - The Id of wrapped `android.widget.EditText`. It should be different with this view's Id so input view can restore state.

* `et_labelEnable` - Indicate that it should show a floating label or not. The label's text will be the hint text of input view.

* `et_labelPadding` - The padding of label with the input view.

* `et_labelTextSize` - The size of label's text.

* `et_labelTextColor` - The color of label's text.

* `et_labelTextAppearance` - The appearance setting of label's text.

* `et_labelEllipsize` - The ellipsize setting of label's text.

* `et_labelInAnim` - The animation when label is shown.

* `et_labelOutAnim` - The animation when label is hided.

* `et_supportMode` - The mode of support text that show below the input view. There are 4 modes: **none**, **helper**, **helperWithError** and **charCounter**.

* `et_supportMaxChars` - The maximum character for input view (used in **charCounter** mode). 0 mean it will only show the char counter.

* `et_helper` - The helper text.

* `et_error` - The error text.

* `et_supportPadding` - The padding of support text with input view.

* `et_supportTextSize` - The size of the support text.

* `et_supportTextColor` - The color of the support text.

* `et_supportTextErrorColor` - The color of the support text when has error.

* `et_supportTextAppearance` - The appearance setting of the support text.

* `et_supportSingleLine` - Indicate that support text should be shown as single-line.

* `et_supportMaxLines` - The maximum lines of the support text.

* `et_supportLines` - The lines of the support text.

* `et_supportEllipsize` - The ellipsize setting of the support text.

* `et_dividerColor` - The color of divider. Accept Color value or ColorStateList resource.

* `et_dividerErrorColor` - The color of divider when has error.

* `et_dividerHeight` - The height of divider.

* `et_dividerPadding` - The padding of divider with input view.

* `et_dividerAnimDuration` - The duration of divider's animation.

* `et_dividerCompoundPadding` - If true, divider should include the padding of compound drawables.

* `et_autoCompleteMode` - Indicate which input view is wrapped. There are 3 modes: **none** (`android.widget.EditText`), **single** (`android.widget.AutoCompleteEditText`) and **multi** (`android.widget.MultiAutoCompleteTextView`)