BottomSheetDialog
=====================

BottomSheetDialog is a custom full screen Dialog that slide in from bottom.


![](https://github.com/rey5137/Material/raw/master/image/bottomsheet.gif)


Usage
------------
  Initialize in code:

```java
    BottomSheetDialogmDialog = new BottomSheetDialog(context);

    BottomSheetDialogmDialog = new BottomSheetDialog(context, styleId);
```

You can chain methods to style BottomSheetDialog:
```java
    mDialog.applyStyle(styleId)
        .contentView(view)
        .heightParam(ViewGroup.LayoutParams.WRAP_CONTENT)
        .inDuration(500)
        .cancelable(true)
        ...
        .show();
```

Attributes
------------

* `bsd_inDuration` - The duration of animation when dialog slide in.

* `bsd_inInterpolator` - The interpolator of animation when dialog slide in.

* `bsd_outDuration` - The duration of animation when dialog slide out.

* `bsd_outInterpolator` - The interpolator of animation when dialog slide out.

* `bsd_cancelable ` - Indicate that dialog is cancelable.

* `bsd_canceledOnTouchOutside ` - Indicate that dialog will be canceled when touch outside.

* `bsd_dimAmount` -  The amount of dim applied to background outside dialog.

* `android:layout_height` -  The height of dialog's layout params. Can be dimension value or match_parent or wrap_content enum.