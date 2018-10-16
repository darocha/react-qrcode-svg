# React svg qrcode component

Install:
```sh
npm install react-qrcode-svg
```

Import:
```js
import QrCode from 'react-qrcode-svg';
```

Use:
```js
const App = () => (
  <QrCode
    data="https://github.com/dral/react-qrcode-svg"
    height="300"
    width="300"
    fgColor="#A1B2C3"
    bgColor="#123456"
  />
);
```

## Options

- `data`: the data to encode
- `ecLevel`: Error correction level, any of `L`, `M`, `Q`, `H` (default 'L');
- `fgColor`: Foreground color (default: `#000`)
- `bgColor`: Background color (default: `none`, transparent background)
- `margin`: Margin or _quiet zone_ arround code in number of modules (default `4`).
- other: Any other properties (`height`, `width`, …) will be passed to the underlying `svg` component.

## Gradient fills

Children elements can be used to define more advanced svg attributes such as [gradient fills](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Gradients):

```js
const App = () => (
  <QrCode
    data="https://github.com/dral/react-qrcode-svg"
    height="300"
    width="300"
    fgColor="url(#gradientFill)"
  >
    <linearGradient id="gradientFill" x1="0" y1="0" x2="1" y2=".7">
      <stop offset="0%" stopColor="#f857a6"/>
      <stop offset="100%" stopColor="#ff5858"/>
    </linearGradient>
  </QrCode>
);
```

Produces:
```xml
<svg height="300" width="300" viewBox="-4 -4 37 37">
  <linearGradient id="gradientFill" x1="0" y1="0" x2="1" y2=".7">
    <stop offset="0%" stop-color="#f857a6"></stop>
    <stop offset="100%" stop-color="#ff5858"></stop>
  </linearGradient>
  <rect x="-4" y="-4" width="37" height="37" fill="none"></rect>
  <path d="..." fill="url(#gradientFill)"></path>
</svg>
```

<svg height="300" width="300" viewBox="-4 -4 37 37"><linearGradient id="gradientFill" x1="0" y1="0" x2="1" y2=".7"><stop offset="0%" stop-color="#f857a6"></stop><stop offset="100%" stop-color="#ff5858"></stop></linearGradient><rect x="-4" y="-4" width="37" height="37" fill="none"></rect><path d="M0 0h7v7h-7zM10 0h1v2h-1zM12 0h2v1h-2zM17 0h4v2h-1v-1h-3zM22 0h7v7h-7zM1 1v5h5v-5zM8 1h1v1h-1zM14 1h3v2h-1v1h-1v1h-1v-1h-2v-2h1v1h1zM23 1v5h5v-5zM2 2h3v3h-3zM18 2h1v2h2v1h-3v1h-1v-1h-1v-1h1v-1h1zM24 2h3v3h-3zM8 3h3v1h-1v2h-1v1h-1v-2h1v-1h-1zM11 5h3v1h-1v1h-1v-1h-1zM15 5h1v1h-1zM10 6h1v1h1v2h-1v-1h-1v1h-4v-1h3v-1h1zM14 6h1v1h1v-1h1v2h-1v1h-1v1h1v-1h1v1h2v2h-1v-1h-1v1h-1v-1h-3v-1h1v-1h-1v-1h1zM18 6h1v1h-1zM20 6h1v1h-1zM19 7h1v1h-1zM0 8h5v1h-1v4h-1v-1h-1v1h1v1h-1v1h-1v1h-1v-2h1v-1h-1v-1h1v-1h-1v-1h2v-1h-2zM17 8h1v1h-1zM20 8h2v1h-1v1h-2v-1h1zM23 8h1v1h1v2h-1v-1h-2v-1h1zM25 8h1v1h-1zM27 8h1v1h-1zM5 9h1v1h2v1h-2v1h-1zM10 9h1v2h-1zM12 9h1v1h-1zM28 9h1v1h-1zM8 11h1v1h2v1h-1v1h-1v-1h-3v-1h2zM12 11h1v1h2v1h-3zM20 11h1v1h-1zM25 11h1v1h1v1h-2zM27 11h1v1h-1zM17 12h1v1h-1zM16 13h1v2h-2v1h-1v-1h-2v2h-1v-3h5zM18 13h7v1h2v1h-2v1h-1v1h1v2h-2v1h2v1h1v-1h1v-1h1v1h1v2h-2v1h-2v2h-4v1h4v-1h1v-1h1v-1h1v1h1v2h-1v2h-1v-1h-1v1h-1v-1h-1v1h1v1h-3v-1h1v-1h-1v1h-2v-1h-1v-2h1v-1h-1v-1h-3v1h2v1h-1v3h-2v-1h-1v1h-1v1h-1v-2h1v-1h-1v-1h3v1h1v-1h-1v-1h-1v-1h1v-1h1v-1h-2v-1h4v1h-1v1h1v-1h1v1h1v-1h-1v-1h1v-2h1v1h1v-1h-1v-2h-1v2h-1v1h-1v-2h1v-2h1v-1h-2zM28 13h1v1h-1zM6 14h1v1h-1zM22 14v1h2v-1zM2 15h1v1h-1zM4 15h1v2h1v1h1v1h-1v1h1v1h-2v-1h-1v-1h1v-1h-2v-1h1zM8 15h2v1h-1v1h1v1h1v2h-2v-1h-1zM27 15h1v1h-1zM6 16h1v1h-1zM15 16h1v1h-1zM17 16h1v1h-1zM22 16v1h1v-1zM25 16h2v3h-1v-2h-1zM0 17h2v1h-1v3h-1zM12 17h2v1h2v1h-2v1h-1v1h-1v-2h1v-1h-1zM16 17h1v1h-1zM28 17h1v1h-1zM2 19h1v1h-1zM3 20h1v1h-1zM8 20h1v2h1v1h-2zM21 21v3h3v-3zM0 22h7v7h-7zM11 22h2v1h-1v2h-2v1h-1v3h-1v-5h2v-1h1zM22 22h1v1h-1zM1 23v5h5v-5zM2 24h3v3h-3zM10 27h1v1h-1zM18 27h1v1h1v1h-3v-1h1zM14 28h1v1h-1zM26 28h1v1h-1z" fill="url(#gradientFill)"></path></svg>
