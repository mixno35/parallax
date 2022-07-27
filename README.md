# Parallax - Tilt Effect - CSS, JS
### Tilt effect (parallax) when the mouse hovers over the element.

[Demo](https://mixno35.github.io/parallax)
#### The code is based on: https://www.cssscript.com/parallax-tilt-effect-on-hover/ (My changes: Renamed the function, added a new function "outIn").

#

> ### Source
### JS File -> [parallax.js](/parallax.js)
#
> ### Docs
#### Add script file to the document.
```HTML
<script type="text/javascript" src="assets/js/parallax.js"></script>
```

#### Add tilt elements to the document.
```HTML
<div class="parallax">
  <h2 class="card">Parallax Effect</h2>
</div>
```

#### Initialize the parallax.js on the element and done.
```JS
window.addEventListener('load', () => {
  setParallax('.card', {
    fx3d: true, // enables fx3d class.
    fxDistance: 70, // distance in px (optional).
  });
});
// .card - the class of your element to which the effect will be applied.
```

#### Config the tilt effect perspective. Default: 400.
```JS
setParallax('.card', {
  perspective: 600,
});
```

#### Determine the tilt size. Default: 4.
```JS
setParallax('.card', {
  maxTilt: 5,
});
```

#### Determine whether to maintain the tilt after mouse leave. Default: false.
```JS
setParallax('.card', {
  mantain: true,
});
```

#### Tilt type: true - farther from the mouse, false - closer to the mouse. Default: false. 
```JS
setParallax('.card', {
  outIn: true,
});
// my function.
```