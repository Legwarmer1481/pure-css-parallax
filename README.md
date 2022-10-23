# pure-css-parallax

This a template where its contains the basics for making a parallax scrolling effet on a web page

## HTML part

All you have to do is to add a div tag with parallax class

Exemple

```
<div class="parallax-3"></div>
<div class="parallax-2"></div>
<div class="parallax-1"></div>
```

The numbers at the end allow to adjust the distance between objects with CSS

## CSS part

For each classes, you absolutly need those properties:

```
position: absolute;
inset: 0;
transform-style: preserve-3d;
```

Then, you add `z-index` and `transform` which allow to adjust the distance and stack in the right order. In `transform`, you need to translate to the back with `translateZ()`. It has to be in negative value like -1px. You add `scale()` to make it to the right size. The value assigned to `scale()` should be additionned from the `translateZ()` value. For exemple, if the value in `translateZ()` is -1px, then the `scale()` should be 2:

```
transform: translateZ(-1) scale(2);
```

In sum, you should have something like this:

```
.parallax{
  position: absolute;
  inset: 0;
  transform-style: preserve-3d;
  z-index: -1;
  transform: translateZ(-1px) scale(2);
}
```
