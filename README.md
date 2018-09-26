Lets say that ```#container``` is your container.

Add to your js:

```
let gallery = $(#container);
let elementsToCurate = <Array of elements>; //[<div class="curatedElement"></div><div class="curatedElement"></div>...]
gallery.append(elementsToCurate);

gallery.curate();
```

...then add to your css:

```
.curatedElement {
    position: relative;
    display: inline-block;
    vertical-align: top;
    z-index: -1;
    opacity: 0;
    margin-right: 12px;
    margin-left: 0;
}

///On bigger devices, the feed floats right.
@media (min-width: 500px) {
    .curatedElement {
        margin-left: 24px;
        margin-right: 0;
    }
}

///on smaller devices, swap the left and right padding.

```

Check joaoritter.com to see it in action. 
