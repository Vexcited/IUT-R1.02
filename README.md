# R1.02

> <https://class.cloudschool.org/M1105/m1105>

## CLI for TailwindCSS

### Installation

```bash
# on windows
npm install -g tailwindcss

# on linux
sudo npm install -g tailwindcss
```

### Configuration

Create a `tailwind.config.js` file in the root directory of the web project. This file will be used to configure TailwindCSS. The following is an example of a `tailwind.config.js` file.

```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./index.html"],

  // Whenever we need responsive.
  theme: {
    screens: {
      tablet: '700px', // Usage with "tablet:" prefix.
      desktop: "1000px" // Usage with "desktop:" prefix.
    }
  },

  // No need to configure the following.
  plugins: []
}
```

### Usage

Inside the `index.html` page, you should have...

```html
<link href="./output.css" rel="stylesheet">
```

In the `input.css` file, you should have...

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Then finally, you can run the following command to generate the `output.css` file. Use `--watch` to automatically update the `output.css` file when you save the `input.css` or `index.html` file.

```bash
tailwindcss -i ./input.css -o ./output.css --watch
```
