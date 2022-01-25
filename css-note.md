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
 - [class^='col-'] attribute selector this is select start with col- class
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
 - perspective | 1500px much value good work to perspective
  .card {
  perspective: 150rem;
  -moz-perspective: 150rem;
  position: relative;
  height: 50rem;
   &__side {
   
   height: 50rem;
    transition: all 0.8s ease;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    backface-visibility: hidden;
   }
 - background-blend-mode: screen; | work as img
 - box-decoration-break: clone; | one element two boxes, both styled like margin, padding| add prefix top of this value|
-float| work only height and width if value set| 
- shape-outside: circle(50% at 50% 50%);  
---
- blockquote::before | [open-quote close-quote](https://css-tricks.com/almanac/properties/q/quotes/)

- object-fit | The object-fit CSS property sets how the content of a replaced element, such as an <img> or <video>, should be resized to fit its container.
- backdrop-filter:
```
@supports (-webkit-backdrop-filter: blur(10px)) or (backdrop-filter: blur(10px)) {
	-webkit-backdrop-filter: blur(10px);
	backdrop-filter: blur(10px);
	background-color: rgba($color-black, .3);
}
```

- 
```
::selection {
	background-color: $color-primary;
	color: $color-white;
}

```
