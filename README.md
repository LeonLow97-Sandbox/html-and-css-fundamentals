## Packages

- Auto Rename Tag (For HTML)
- Color Highlight (For CSS)
- Image Preview (For HTML)
- One Monokai Theme (For VSCode theme)

## Semantic HTML

- Semantic is giving some meaning to the HTML elements.
- Important for screen readers.

```html
<strong></strong>
<em></em>
<nav></nav>
<article></article>
<header></header>
<footer></footer>
```

## HTML Glyphs

- [HTML Glyphs](https://css-tricks.com/snippets/html/glyphs/)

## Colors in CSS

- White: RGB(255, 255, 255)
- Black: RGB(0,0,0)

#### RGB Notation

- Regular RGB Model
  - rgb(0, 255, 255)
- RGB with transparency ('alpha')
  - rgb(0, 255, 255, 0.3)

#### Hexadecimal Notation

- Instead of using a scale from 0 to 255, we go from **0 to ff** (255 in hexadecimal numbers).
  - #00ffff
- Shorthand, when all colors are identical pairs.
  - #0ff
- In practice, we use hexadecimal Notation unless we need transparency then use rgb

#### Shades of grey

- When colors in all 3 channels are the same, we get a **grey color**.
- There are 256 pure grays to choose from.
  - rgb(0,0,0), #000000, #000
  - rgb(69,69,69), #444444, #444
  - rgb(183,183,183), #b7b7b7
  - rgb(255,255,255), #ffffff, #fff

# Conflicts between Selectors

- When there are multiple selectors targeting the same element, all of them are applied but which has the highest priority?

```
Highest Priority
  1. Declarations marked !important
  2. Inline style (style attribute in HTML)
  3. ID (#) Selector
  4. Class (.) or pseudo-class (:) selector
  5. Element selector (p, div, li, etc.)
  6. Universal selector (\*)
Lowest Priority
```

# How Inheritance Works?

- Not all properties get inherited. It is mostly the ones **lated to text**: font-family, font-size, font-weight, font-size, ...

```css
body {
  color: #444444;
}

/* Overrides the inherited style of #444 */
h1 {
  color: #1098ad;
}
```

```html
<body>
  <h1>My Website</h1>
</body>
```