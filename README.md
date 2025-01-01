# CSS Counters and Custom Properties #

[Demo](http://MERNCraft/CSS_properties)

A demonstration of using the state of a checkbox to set the initial value of a CSS custom property

In this case, the order in which the HTML places the checkboxes...


... is not the 
```html
    <label>
      Add 10: <input id="add10" type="checkbox">
    </label>
    <label>
      Add 100: <input id="add100" type="checkbox">
    </label>
    <label>
      Add 1000: <input id="add1000" type="checkbox">
    </label>
```

... is different from the order in which the CSS treats the checkboxes.

```css
body:has(#add1000:checked)  {
  --start: 1000
}

body:has(#add10:checked)  {
  --start: 10
}

body:has(#add100:checked)  {
  --start: 100
}
```

This demonstration shows that the order of the CSS rules takes priority over the order of the HTML elements.