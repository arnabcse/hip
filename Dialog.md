Dialog 
=====================

  `com.rey.material.app.Dialog` is a custom dialog that apply Material Design specification.

![](https://github.com/rey5137/Material/raw/master/image/dialog_1.png)
![](https://github.com/rey5137/Material/raw/master/image/dialog_2.png)


Usage
------------

Initialize in code:

```java
    Dialog mDialog = new Dialog(context);

    Dialog mDialog = new Dialog(context, styleId);
```

You can chain methods to style Dialog:
```java
    mDialog.applyStyle(styleId)
        .title("Dialog title")
        .positiveAction("OK")
        .negativeAction("CANCEL")
        .contentView(view)
        .cancelable(true)
        ...
        .show();
```

Attributes
------------
* `android:layout_width` - the width of dialog's layout params. Can be dimension value or `match_parent` or `wrap_content` enum (`match_parent` doesn't make dialog full screen due to some padding of Material Design Dialog's spec).

* `android:layout_height` - the height of dialog's layout params. Can be dimension value or `match_parent` or `wrap_content` enum (`match_parent` doesn't make dialog full screen due to some padding of Material Design Dialog's spec).

* `di_dimAmount` - The amount of dim applied to background outside dialog.

* `di_backgroundColor` - The background's color of dialog.

* `di_elevation` - The elevation of dialog.

* `di_layoutDirection` - The layout direction of dialog. There are 3 types: **ltr**, **rtl** and **locale**.

* `di_maxWidth` - the maximum width of dialog.

* `di_maxWidth` - the maximum width of dialog.

* `di_maxHeight` - the maximum height of dialog.

* `di_titleTextAppearance` - The appearance setting of title text.

* `di_titleTextColor` - The color of title text.

* `di_actionBackground` - The background drawable of action buttons.

* `di_actionRipple` - The ripple effect style of action buttons.

* `di_actionTextAppearance` - The appearance setting of action texts.

* `di_actionTextColor` - The color of action texts.

* `di_positiveActionBackground` - The background drawable of positive action button.

* `di_positiveActionRipple` - The ripple effect style of positive action button.

* `di_positiveActionTextAppearance` - The appearance setting of positive action text.

* `di_positiveActionTextColor` - The color of positive action text.

* `di_negativeActionBackground` - The background drawable of negative action button.

* `di_negativeActionRipple` - The ripple effect style of negative action button.

* `di_negativeActionTextAppearance` - The appearance setting of negative action text.

* `di_negativeActionTextColor` - The color of positive negative text.

* `di_neutralActionBackground` - The background drawable of neutral action button.

* `di_neutralActionRipple` - The ripple effect style of neutral action button.

* `di_neutralActionTextAppearance` - The appearance setting of neutral action text.

* `di_neutralActionTextColor` - The color of neutral action text.

* `di_dividerColor` - The color of divider (divider is shown between action buttons and content view when content view is scrollable).

* `di_dividerHeight` - The height of divider.

* `di_cancelable` - Indicate that dialog is cancelable.

* `di_canceledOnTouchOutside` - Indicate that dialog will be canceled when touch outside.

* `di_inAnimation` - The animation used when showing dialog.

* `di_outAnimation` - The animation used when hiding dialog.


SimpleDialog
------------

  `com.rey.material.app.SimpleDialog` is a dialog extends from `com.rey.material.app.Dialog` and provide some commond views as message, choices, multi-choices.


##Attributes

* `di_messageTextAppearance` - The appearance setting of message text.

* `di_messageTextColor` - The color of message text.

* `di_radioButtonStyle` - The style of RadioButtonDrawable will be used.

* `di_checkBoxStyle` - The style of CheckBoxDrawable will be used.

* `di_itemHeight` - The height of item.

* `di_itemTextAppearance` - The appearance setting of item's text.


DialogFragment
--------------
  If you want to use `com.rey.material.app.Dialog` as DialogFragment, you can use `com.rey.material.app.DialogFragment` class.

  To create `com.rey.material.app.DialogFragment` object, just call static method:

```java
    public static DialogFragment newInstance(DialogFragment.Builder builder);
```
  
  `DialogFragment.Builder` is an interface that will build Dialog when needed and pass the click event on action button.

```java
    public interface Builder{
        public com.rey.material.app.Dialog build(Context context);

        public void onPositiveActionClicked(DialogFragment fragment);

        public void onNegativeActionClicked(DialogFragment fragment);

        public void onNeutralActionClicked(DialogFragment fragment);
    }
```

  You don't need to write you own `Builder` class, `Dialog` and `SimpleDialog` already have static class `Dialog.Builder` and `SimpleDialog.Builder` for you to use.

  If you have to write you own `Builder` class, you should extends from `Dialog.Builder` class and override `onBuild` , `onReadFromParcel()` or `onWriteToParcel()` methods.
 