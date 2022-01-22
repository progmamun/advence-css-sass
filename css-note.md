# css note

- clip-path: polygon(0 0, 100% 0, 100% 75vh, 0 100%);
- backface-visibility: hidden; | shrink animation or something gone.
- background-clip into text.

```
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
 } 
 
 &:hover &__photo:not(:hover) {
 	transform: scale(.95);
 // composition:hover composition__photo:not(:hover){}
 }
 ```
