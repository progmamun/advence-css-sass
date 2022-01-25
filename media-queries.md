# media-queries
- Media queries don't add any importance or specificity to selectors, so code order matters- **media queries at the end.**
- min-width: | minimum width at which media query starts to apply.

# Mobile-first | pros and cons
|PROS | CONS |
|-----|-------|
|100% optimised for the mobile experience;|The desktop version might feel overly empty and simplistic;|
| Reduces websites and apps to the absolute essentials;|More difficult and counterintuitive to develop;|
| Results in smaller, faster and more efficient products;|Less creative freedom, making it more difficult to create distinctive products;|
| Prioritizes content over aesthetic design, which may be desirable.|Clients are used to see a desktop version of the site ass a prototype; Do your users even use the mobile internet? What's the purpose of your website?|
---
# Selecting our Breakpoints: A Good Approach
0 - 600px : Phone
600 - 900px : Table portrait
900 - 1200px : Table landscape
1200 - 18000px: is where our normal style apply
1800px +: Big desktop
## ORDER: Base + typography > general layout > grid > page layout > components
```
// 1em = 16px; em work every browser but rem not

@mixin respond($breakpoint) {
  @if $breakpoint == phone {
    @media (max-width: 37.5em) {
      @content; // 600px
    }
  }
  @if $breakpoint == tab-port {
    @media (max-width: 56.25em) {
      @content; // 900px
    }
  }
  @if $breakpoint == tab-land {
    @media (max-width: 75em) {
      @content; // 1200px
    }
  }
  @if $breakpoint == big-desktop {
    @media (max-width: 112.5em) {
      @content; // 1800px
    }
  }
}
```
---
```
html {
  // This defines what 1rem is
  font-size: 62.5%; // 1rem = 10px; 10px/16px = 62.5%

  // @include respond(phone) {
  //   font-size: 50%; //
  // } not need it because tab-port also do the same job
  @include respond(tab-land) {
    // width < 1200px
    // width < 900
    font-size: 56.25%; // 1 rem = 9px, 9/16 = 56.25%
  }
  @include respond(tab-port) {
    // width < 600
    font-size: 50%; //1 rem = 8px, 8/16 = 50%
  }

  @include respond(big-desktop) {
    font-size: 75%; //1 rem = 12, 12/16= 75%
  }
}
```

# When to use responsive imgage: The 3 use cases
1. Resolution switching | Decrease image resolution on smaller screen
2. Density Switching |@2x screen(high-res) @1x screen(low-res) |Half the image resolution on @1x screen
3. Art Direction | Different image on smaller screen

```
 <picture class="footer__logo">
        <source
          srcset="
            dist/img/logo-green-small-1x.png 1x,
            dist/img/logo-green-small-2x.png 2x
          "
          media="(max-width: 37.5em)"
        />
        <img
          srcset="dist/img/logo-green-1x.png 1x, dist/img/logo-green-2x.png 2x"
          alt="full logo"
          src="dist/img/logo-green-2x.png"
        />
 </picture>
```
- css responsive background imgage
```
 @media (min-resolution: 192dpi) and (min-width: 37.5em),
 (-webkit-min-device-pixel-ratio: 2) and (min-width: 37.5em), (min-width: 125em) {
    background-image: linear-gradient(
        to right bottom,
        rgba($color-tertiary-light, 0.8),
        rgba($color-tertiary-dark, 0.8)
      ),
      url(/dist/img/hero.jpg);
  }
```
