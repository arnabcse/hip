Button
=====================

  `com.rey.material.widget.Button`is a custom view that extends from `android.widget.Button` and added support for ripple effect.

![](https://github.com/rey5137/Material/raw/master/image/button_raise_touch.gif)
![](https://github.com/rey5137/Material/raw/master/image/button_raise_wave.gif)

Usage
------------
  Declare in XML:

```xml
    <com.rey.material.widget.Button
        style="@style/YourRippleDrawableStyle"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="BUTTON"
        app:rd_enable="true"/>
```

  `rd_enable` attribute have to be set to true to indicate that the view should look for RippleDrawable's attributes. If not, it'll simply ignore those attributes. Material Library already has some default RippleDrawable style you can use:

* `Material.Drawable.Ripple.Touch`.

* `Material.Drawable.Ripple.Touch.Light`.

* `Material.Drawable.Ripple.Touch.MatchView`.

* `Material.Drawable.Ripple.Touch.MatchView.Light`.

* `Material.Drawable.Ripple.Wave`.

* `Material.Drawable.Ripple.Wave.Light`.


In case you want to use `style` for your own style, not for RippleDrawable , then you can pass RippleDrawable style for `rd_style` attribute:

```xml
    <com.rey.material.widget.Button
        style="@style/YourOwnStyle"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="BUTTON"
        app:rd_style="@style/YourRippleDrawableStyle"/>
```
  
  Note that in this case, the view'll load the style from `rd_style` attribute and ignore all RippleDrawable atrributes you may set before.


Attributes
--------------------------

* `rd_rippleType` - The type of ripple. There are 2 types: **TOUCH** and **WAVE**.

* `rd_delayClick` - There are 3 types: **NONE** (fire click event immediately), **UNTILRELEASE** (wait until Ripple's release animation start then fire event) and **AFTERRELEASE** (wait until Ripple's release animation end then fire event).

* `rd_backgroundColor` - The background color of ripple's layer (used in **TOUCH** ripple tyle).

* `rd_backgroundAnimDuration` - The animation's duration of background color.

* `rd_maxRippleRadius` - The maximum ripple radius (used in **TOUCH** ripple tyle). It can be dimension value or `match_view` enum(ripple effect will cover all view).

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

Ripple Effect for Custom View
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
3. Override setBackgroundDrawable(), setOnClickEvent() and onTouchEvent().

    ```java
    @Override
    public void setBackgroundDrawable(Drawable drawable) {
        Drawable background = getBackground();
        if(background instanceof RippleDrawable && !(drawable instanceof RippleDrawable))
            ((RippleDrawable) background).setBackgroundDrawable(drawable);
        else
            super.setBackgroundDrawable(drawable);
    }
    
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


FloatingActionButton
=====================


![](https://github.com/rey5137/Material/raw/master/image/fab_image.gif)
![](https://github.com/rey5137/Material/raw/master/image/fab_line.gif)

Attributes
------------

* `fab_backgroundColor` - The background color of this view.

* `fab_radius` - The radius of this view.

* `fab_elevation` - The elevation of this view.

* `fab_iconSize` - The size of icon drawable.

* `fab_iconSrc` - The drawable used as icon.

* `fab_iconLineMorphing` - The style of LineMorphingDrawable will be used as icon.

* `fab_interpolator` - The interpolator of animation when switch icon drawable.

* `fab_animDuration` - The duration of animation when switch icon drawable.


LineMorphingDrawable 
--------------------
LineMorphingDrawable is a Drawable class that draw a series of line segments and can animate them between 2 states.

##Attributes
* `lmd_state` - The reference to XML resource defines states of this Drawable.

* `lmd_curState` - The current state of this Drawable.

* `lmd_padding` - The padding of this Drawable.

* `lmd_paddingLeft` - The left padding of this Drawable.

* `lmd_paddingTop` - The top padding of this Drawable.

* `lmd_paddingRight` - The right padding of this Drawable.

* `lmd_paddingBottom` - The bottom padding of this Drawable.

* `lmd_animDuration` - The duration of animation when it switches state.

* `lmd_interpolator` - The interpolator of animation when it switches state.

* `lmd_strokeSize` - The size of stroke.

* `lmd_strokeColor` - The color of stroke.

* `lmd_strokeCap` - The cap setting of stroke.

* `lmd_strokeJoin` - The join setting of stroke.

* `lmd_clockwise` - If true, the animation will rotate clockwise when switch state.

##State XML
  To define states for LineMorphingDrawable, you need to create a XML file with format:

```xml
<state-list>
    
    <state>			    <!-- the first state !-->
        <points>                    <!-- all value are fraction !-->
        	<item>0.5</item>    <!-- the x value of start point of first line segment !-->
        	<item>0</item>      <!-- the y value of start point of first line segment !-->
        	<item>0.5</item>    <!-- the x value of end point of first line segment !-->
        	<item>1</item>      <!-- the y value of end point of first line segment !-->
        	
        	<item>0</item>      <!-- the x value of start point of second line segment !-->
        	<item>0.5</item>    <!-- the y value of start point of second line segment !-->
        	<item>1</item>      <!-- the x value of end point of second line segment !-->
        	<item>0.5</item>    <!-- the y value of end point of second line segment !-->
            ...
        </points>     

        <links>               <!-- Each pair of values define the index of 2 line segment that are linked !-->
        	<item>0</item> 	
        	<item>1</item>
        </links>    
  
    </state>
    
</state-list>
```