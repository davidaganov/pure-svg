# Pure SVG

## Examples

- [GitHub](https://github.com/davidaganov21/pure-svg)
- [CodeSandbox](https://codesandbox.io/s/pure-svg)

## Install

#### NPM / Yarn

```
git clone https://github.com/davidaganov21/pure-svg
cd pure-svg
npm install
```

## Usage

Simply use it like so:

```html
<Base-Icon 
  name="Title" 
  color="green" 
  box="0 0 24 24" 
  :sizes="24" 
  :rotate="90" 
  :stroke="false"
>
  <Icon-Email/>
<Base-Icon>
```

## Props

- `name: String` - A tooltip that pops up on hover, the name of the icon for accessibility
- `stroke: Boolean` - Color for stroke instead of fill
- `color: String` - Icon color (default "currentColor")
- `box: String` - Visible area of the icon
- `sizes: Number` - The height and width of the icon (can be set separately)
- `width: Number` - Icon width
- `height: Number` - Icon height
- `rotate: Number` - Icon rotation angle

## Credits

Author: [David Aganov](https://github.com/davidaganov21)