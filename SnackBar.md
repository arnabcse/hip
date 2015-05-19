SnackBar
=====================
![](https://github.com/rey5137/Material/raw/master/image/snackbar.png)

Usage
------------

You can add SnackBar to the layout:

```xml
<com.rey.material.widget.SnackBar 
    style="@style/SnackBarStyle"
    android:layout_width="match_parent"
    android:layout_height="wrap_content" />
```

Or initialize in code:

```java
    SnackBar.make(context)
        .applyStyle(styleId)

```

You can chain another methods to style SnackBar:

```java
    mSnackBar.text("This is a SnackBar")
        .singleLine(true)
        .actionText("CLOSE")
        .actionClickListener(new SnackBar.OnActionClickListener(){...})
        .duration(1000)
        ...
```

After apply style to SnackBar, you can show it by call one of following functions:

```java
    public void show(Activity activity);

    //parent should be FrameLayout or RelativeLayout so SnackBar can algin bottom.
    public void show(ViewGroup parent); 

    // It only work if SnackBar is already attached to a parent view.
    public void show(); 
```

Attributes
------------
* `sb_backgroundColor` - The background color of SnackBar.

* `sb_backgroundCornerRadius` - The corner's radius of SnackBar.

* `sb_horizontalPadding` - The horizontal padding between background and text.

* `sb_verticalPadding` - The vertical padding between background and text.

* `sb_width` - The width of SnackBar. Can be dimension value or `match_parent` or `wrap_content` enum.

* `sb_minWidth` - The minimum width of SnackBar.

* `sb_maxWidth` - The maximum width of SnackBar.

* `sb_height` - The height of SnackBar. Can be dimension value or `match_parent` or `wrap_content` enum.

* `sb_minHeight` - The minimum height of SnackBar.

* `sb_maxHeight` - The maximum height of SnackBar.

* `sb_marginStart` - The start margin of SnackBar with parent view.

* `sb_marginBottom` - The bottom margin of SnackBar with parent view.

* `sb_textSize` - The size of message text.

* `sb_textColor` - The color of message text.

* `sb_textAppearance` - The appearance setting of message text.

* `sb_text` - The message text.

* `sb_singleLine` - Indicate that message text should be show as single-line or not.

* `sb_maxLines` - The maximum lines of message text.

* `sb_lines` - The line number of message text.

* `sb_ellipsize` - The ellipsize setting of message text.

* `sb_actionTextSize` - The size of action text.

* `sb_actionTextColor` - The color of action text.

* `sb_actionTextAppearance` - The appearance setting of action text.

* `sb_actionText` - The action text. Empty text mean hide action button.

* `sb_actionRipple` - The ripple style for action button.

* `sb_duration` - The duration the SnackBar will be shown.

* `sb_inAnimation` - The animation when SnackBar is shown.

* `sb_outAnimation` - The animation when SnackBar is hided.

* `sb_removeOnDismiss` - Indicate that SnackBar should remove itself from parent view when hidding
