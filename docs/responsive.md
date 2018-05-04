# Responsive mixin
Adjusting responsive breakpoints won't cause any headache anymore.

# Example
```scss
    @import 'helpers/responsive';

    // default syntax
    @include responsive($breakpointsList, $type: min|max);
    // by default, any call to mixin will be set to min-width by default 
    // unless you specify the second argument to the mixin

    section {
        h1 {
            color: white;
            @include responsive((
                0: (
                    background: red,
                ),
                320: (
                    background: green,
                ),
                480: (
                    background: blue,
                ),
                560: (
                    background: orange,
                ),
                768: (
                    background: black,
                ),
            ));
        }
    }
```
## Output
```css
    section h1 {
        color: white;
    }
    @media (min-width: 0px) {
        section h1 {
            background: red;
        }
    }
    @media (min-width: 320px) {
        section h1 {
            background: green;
        }
    }
    @media (min-width: 480px) {
        section h1 {
            background: blue;
        }
    }
    @media (min-width: 560px) {
        section h1 {
            background: orange;
        }
    }
    @media (min-width: 768px) {
        section h1 {
            background: black;
        }
    }
```