# css note

- clip-path: polygon(0 0, 100% 0, 100% 75vh, 0 100%);
- backface-visibility: hidden; | shrink animation or something gone.
- background-clip into text.

```
display: inline-block;
background-image: linear-gradient(
   to right,
   $color-primary-light,
   $color-primary-dark
 );
 background-clip: text;
 -webkit-background-clip: text;
 color: transparent;
```

`&:not(:last-child) { margin-bottom: 3rem; }` | pseudo class
 - [CSS Glyphs UNICODE code snippets](https://css-tricks.com/snippets/html/glyphs/) | css unicode html
 ---
 ```
 outline-offset: 2rem; 
 &:hover {
 outline: 1.5rem solid $color-primary;
 transform: scale(1.05) translateY(-.5rem);
  box-shadow: 0 2.5rem 4rem rgba($color-black, 0.5);
      z-index: 20;
 } 
 
 &:hover &__photo:not(:hover) {
 	transform: scale(.95);
 // composition:hover composition__photo:not(:hover){}
 }
 ```
 - direct childs selector | .section-features > * |all child has been selected
