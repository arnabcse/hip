ThemeManager
=====================

All widgets in `com.rey.material` package have `applyStyle(int)` method so you can change the style dynamically at runtime. But to support dynamic theme, you still have to do a lot of works, like save and restore current theme, and apply new style to all widgets when theme is changed. And that is what ThemeManager will do for you.

![](https://github.com/rey5137/Material/raw/master/image/theme.gif)

Usage
------------

First, you have to initialize ThemeManager via `init(Context context, int totalTheme, int defaultTheme, @Nullable EventDispatcher dispatcher)` method. It should be done in `onCreate()` method of Application. For example:

```java

public void onCreate() {
    super.onCreate();
    ThemeManager.init(this, 2, 0, null);
}

```

Next, declare the list of styles for each widget. Here is an example for Button:

```xml

<array name="button_flat">
    <item>@style/LightFlatButtonRippleStyle</item>
    <item>@style/DarkFlatButtonRippleStyle</item>
</array>

```
The order of styles in list must be same for all widgets. Now, we can set the style for Button via `v_styleId` attribute in XML:

```xml
<com.rey.material.widget.Button
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="BUTTON"
    android:background="@null"
    app:v_styleId="@array/button_flat"/>
```
Note that you can use both `style` and `v_styleId` attribute to style the widget, but the style of `v_styleId` attribute will override the style of `style` attribute.

It's done. We can change the theme of app simply by calling `setCurrentTheme(int)` method.

```java
ThemeManager.getInstance().setCurrentTheme(theme);
```