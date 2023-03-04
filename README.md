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

## CSS Box Model

- Content: Text, images, etc.
- Border: A line around the element, still inside of the element.
- Padding: Invisible space around the content, inside of the element. (between content and border).
- Margin: Space outside of the element, between elements.
- Fill area: Area that gets filled with background color or background image.

## Element Height and Width Calculation

- Final element width = left border + left padding + width + right padding + right border
- Final element height = top border + top padding + height + bottom padding + bottom border

#### Shorthand notation

- `padding: 20px 40px;`
  - top and bottom, left and right

## Collapsing Margins

- Affects how vertical margins between adjacent elements are handled.
- When 2 adjacent elements have margins that touch or overlap, the margins collapse into a single margin, which is equal to the **larger** of the 2 margins.

# CSS: Types of Boxes

### Inline Elements

- Occupies only the space **necessary for its content**.
- Causes **no line-breaks** after or before the element.
- Box model applies in a different way: **heights and widths do not apply**.
- **Padding and margins** are applied **only horizontally** (left and right).
- These elements are typically used to wrap small bits of text or other inline content, such as icons or images.
- `<span>, <a>, <em>, and <strong>`
- **With CSS: `display: inline`**

### Block-Level Elements

- Elements are formatted visually as blocks.
- Elements occupy **100% of parent element's width, no matter the content**.
- Elements are **stacked vertically** by default, one after another.
- `<div>, <p>, <h1>-<h6>, and <ul>/<ol>`
- **With CSS: `display: block`**
  - Changing inline elements to block level elements

### Inline-Block Elements

- Inline-block elements are a hybrid of inline and block-level elements.
- They take up only as much space as their content needs but they can also have padding, margin, and border set on them, just like block-level elements.
- `<button>, <input>, <img> and <label>`
- **With CSS: `display: inline-block`**
