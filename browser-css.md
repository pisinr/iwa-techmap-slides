## How do you do Style them?

* Inline styling
* Plain CSS
* SCSS
* Hybrid

^^^

## Plain CSS

* Good for multiple frontend.
* Use Naming Convention to avoid collision.
  * Use BEM

```css
  .Header__title {
    /* style */
  }
  .Header__title--alert {
    /* style */
  }
```

^^^

## SCSS

* Preprocessor to CSS.
* Allow nested definition, functions, variables, etc.

```scss
$brand-color: #ff0000;
.Button {
    background-color: $brand-color;

    &:hover {
        background-color: lighten($brand-color, 10%);
    }

    &__text {
        // Use BEM
    }
}
```

^^^

## Hybrid

* CSS Modules, Angular Style scope
* (Usually) Require JS
* Generate Unique class name.
* (Usually) more dynamic.

```jsx
import styled from 'styled-components';
const Header = styled.div`
  margin: 40px;
  border: 5px outset ${themes.brandColor};
  &:hover {
   background-color: yellow;
 }
`
```