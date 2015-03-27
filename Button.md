Button
=====================

  `com.rey.material.widget.Button`is a custom view that extends from `android.widget.Button` and added support for ripple effect.

![](https://github.com/rey5137/Material/blob/master/image/button_raise_touch.gif)
![](https://github.com/rey5137/Material/blob/master/image/button_raise_wave.gif)

Attributes
------------

* `ripple` - The style of RippleDrawable will be used as this view's background.

* `delayClick` - If true, the view will wait for RippleDrawable finish animation before firing OnClickEvent.


RippleDrawable
--------------------------
  RippleDrawable is a Drawable that provide ripple effect.


##Attributes

* `rd_rippleType` - The type of ripple. There are 2 types: **TOUCH** and **WAVE**.

* `rd_background` - The background drawable for the view (needed if you want to use 9-patch drawable as button's background). The ripple effect will be draw over this drawable.

* `rd_backgroundColor` - The background color of ripple's layer (used in **TOUCH** ripple tyle).

* `rd_backgroundAnimDuration` - The animation's duration of background color.

* `rd_maxRippleRadius` - The maximum ripple radius (used in **TOUCH** ripple tyle). It can be dimension value or _full_ enum(ripple effect will cover all view).

* `rd_rippleColor` - The color of ripple.

* `rd_rippleAnimDuration` - The animation's duration of ripple.

* `rd_inInterpolator` - The interpolator for IN animation.

* `rd_outInterpolator` - The interpolator for OUT animation.

* `rd_maskType` - The mask's type of ripple. The mask is used to restrict ripple effect only show in a part of view. There are 2 type of mask: **RECTANGLE** and **OVAL**.

* `rd_cornerRadius` - The corner's radius of mask.

* `rd_topLeftCornerRadius` - The top left corner's radius of mask.

* `rd_topRightCornerRadius` - The top right corner's radius of mask.

* `rd_bottomLeftCornerRadius` - The bottom left corner's radius of mask.

* `rd_bottomRightCornerRadius` - The bottom right corner's radius of mask.

* `rd_padding` - The padding of mask.

* `rd_leftPadding` - The left padding of mask.

* `rd_topPadding` - The top padding of mask.

* `rd_rightPadding` - The right padding of mask.

* `rd_bottomPadding` - The bottom padding of mask.

Ripple Efftect for Custom View
-------------------------------

If you want to add ripple effect for your custom view.

1. Create a `RippleManager` object in your custom view.

    ```java
    RippleManager mRippleManager = new RippleManager();
    ```
2. Call onCreate() method of `RippleManager` in view's constructor.

    ```java
    mRippleManager.onCreate(this, context, attrs, defStyleAttr, defStyleRes);
    ```
3. Override setOnClickEvent() and onTouchEvent().

    ```java
    @Override
    public void setOnClickListener(OnClickListener l) {
        if(l == mRippleManager)
            super.setOnClickListener(l);
         else{
            mRippleManager.setOnClickListener(l);
            setOnClickListener(mRippleManager);
        }	
    }
	
    @Override
    public boolean onTouchEvent(@NonNull MotionEvent event) {
        boolean result = super.onTouchEvent(event);
        return  mRippleManager.onTouchEvent(event) || result;
    }
    ```