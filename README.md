# Frontend Mentor - Order summary card solution with CUBECSS

This is a solution to the [Order summary card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/order-summary-component-QlPmajDUj) using [CUBECss](https://cube.fyi).

Live Demo: *coming soon*

## Table of contents

- [The process](#my-process)
- [The block is a specification](#what-i-learned)
- [Useful resources](#useful-resources)

### Screenshot

<figure>
<img src="./screenshots/desktop.png"  />
<figcaption>Desktop</figcaption>
</figure>
<figure>
<img src="./screenshots/mobile.png" width="50%"  />
<figcaption>Mobile</figcaption>
</figure>

## The process

### Built with

- [CUBECss](https://cube.fyi)
- Semantic HTML5 markup
- CSS custom properties

### The block is a specification

The block which in other context would be called a _component_ do very little implementation. Instead it's a specification for the underlying _composition_ and _utlities_. The following is the declaration for the _card_ block. It sets some generic css custom properties that other declarations set by the _composition_ and _utlities_ make use off. It's an specification not an implementation.

```css
[c\:b="card"] {
  max-width: 440px;
  overflow: hidden;

  background-color: white;

  --gap: 2rem;

  --softness: 1rem;

  --shadow-o: 0.1;
  --shadow-y: 2rem;
}
[c\:b="card"] ol {
  --gap: 1rem;
}
[c\:b="card"] ol li {
  --softness: 0.5rem;
}
@media screen and (max-width: 440px) {
  [c\:b="card"] {
    flex-grow: 1;
    --padding-mult: 0.5;
    --softness: 0;
  }
}
```

```html
<div class="soft shadow" c:b="card"></div>
```

Use of custom attribute to identify a block element instead of mixing it with the classes, the attribute name is arbitraty but the use of "_name_ : _name_" makes it separate from the HTML spec. In this case the _c_ stands for _CUBE_ and _b_ stands for _block_, it's the block identifier with a value of _card_

```css
[c\:b="card"]
```

**:** is an ileagal identifier so we need to escape it with a \

### Useful resources

- [CUBECss from piccalil](https://piccalil.li/blog/cube-css/) - This is the original post from Andy Bell outlining the thinking behind CUBECss
- [CUBECss docs](https://cube.fyi/) - The docs behind the methodology
- [MDN Attribute Selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors)

## Author

- Website - [m-aldrin](https://m-aldrin.space)
