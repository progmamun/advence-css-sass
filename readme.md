# advence-css-sass

## There Pillars to write good html and css... and build good websites

1. Responsive design

- Fluid layouts
- Media queries
- Responsive images
- Correct units
- Desktop-first vs mobile-first

2. Maintainable and scalable code

- Clean
- Easy-to-understand
- Growth
- Reusable
- How to organize files
- How to name classes
- How to structure html

3. Web performance

- Less HTTP requests
- Less code
- Compress code
- Use a CSS preprocessor
- Less images
- compress images

# cascade and specificity:

- CSS declarations marked with !important have the highest priority.
- But, only use !important as a last resource. It's better to use correct specificities -- more maintainable code!
- Inline styles will always have priority over styles in external stylesheets.
- A selector that contains 1 ID is more specific than one with 1000 classes.
- A selector that contains 1 class is more specific than one with 1000 elements.
- The universal selector \* has no specificity value (0, 0, 0, 0).
- Rely more on **specificity** than on the order of selectors.
- But, rely on order when using 3rd-party stylesheets -always put your author stylesheet last.
