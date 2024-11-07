### Bootstrap 5 &mdash;

1. CDN Link

```html
<link
  href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
  rel="stylesheet"
  integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH"
  crossorigin="anonymous"
/>
<script
  src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
  integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
  crossorigin="anonymous"
></script>
```

OR

```html
<script
  src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.8/dist/umd/popper.min.js"
  integrity="sha384-I7E8VVD/ismYTF4hNIPjVp/Zjvgyol6VFvRkX/vR+Vc4jQkC+hVqc2pM8ODewa9r"
  crossorigin="anonymous"
></script>
<script
  src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.min.js"
  integrity="sha384-0pUGZvbkm6XF6gxjEnlmuGrJXVbNuzT9qBBavbLwCsOGabYfZo0T0to5eqruptLy"
  crossorigin="anonymous"
></script>
```

2. NPM Package

```sh
    npm install bootstrap@5.3.3
```

### Browserslist &mdash;

```
# https://github.com/browserslist/browserslist#readme

>= 0.5%
last 2 major versions
not dead
Chrome >= 60
Firefox >= 60
Firefox ESR
iOS >= 12
Safari >= 12
not Explorer <= 11
```

#### Mobile devices &mdash;

Generally speaking, Bootstrap supports the latest versions of each major platform’s default browsers. Note that proxy browsers (such as Opera Mini, Opera Mobile’s Turbo mode, UC Browser Mini, Amazon Silk) are not supported.

|         | Chrome    | Firefox   | Safari    | Android Browser & WebView |
| ------- | --------- | --------- | --------- | ------------------------- |
| Android | Supported | Supported | —         | v6.0+                     |
| iOS     | Supported | Supported | Supported | —                         |

#### Desktop browsers &mdash;

Similarly, the latest versions of most desktop browsers are supported.

|         | Chrome    | Firefox   | Microsoft Edge | Opera     | Safari    |
| ------- | --------- | --------- | -------------- | --------- | --------- |
| Mac     | Supported | Supported | Supported      | Supported | Supported |
| Windows | Supported | Supported | Supported      | Supported | —         |

#### Internet Explorer &mdash;

Internet Explorer is not supported. If you require Internet Explorer support, please use Bootstrap v4.

### WORKING WITH SASS &mdash;

#### File structure

Whenever possible, avoid modifying Bootstrap’s core files. For Sass, that means creating your own stylesheet that imports Bootstrap so you can modify and extend it. Assuming you’re using a package manager like npm, you’ll have a file structure that looks like this:

```
your-project/
├── scss/
│   └── custom.scss
└── node_modules/
│   └── bootstrap/
│       ├── js/
│       └── scss/
└── index.html
```

If you’ve downloaded our source files and aren’t using a package manager, you’ll want to manually create something similar to that structure, keeping Bootstrap’s source files separate from your own.

```
your-project/
├── scss/
│   └── custom.scss
├── bootstrap/
│   ├── js/
│   └── scss/
└── index.html
```

### Importing

In your custom.scss, you’ll import Bootstrap’s source Sass files. You have two options: include all of Bootstrap, or pick the parts you need. We encourage the latter, though be aware there are some requirements and dependencies across our components. You also will need to include some JavaScript for our plugins.

```scss
// Custom.scss
// Option A: Include all of Bootstrap

// Include any default variable overrides here (though functions won't be available)

@import "../node_modules/bootstrap/scss/bootstrap";

// Then add additional custom code here
```

OR

```scss
// Custom.scss
// Option B: Include parts of Bootstrap

// 1. Include functions first (so you can manipulate colors, SVGs, calc, etc)
@import "../node_modules/bootstrap/scss/functions";

// 2. Include any default variable overrides here

// 3. Include remainder of required Bootstrap stylesheets (including any separate color mode stylesheets)
@import "../node_modules/bootstrap/scss/variables";
@import "../node_modules/bootstrap/scss/variables-dark";

// 4. Include any default map overrides here

// 5. Include remainder of required parts
@import "../node_modules/bootstrap/scss/maps";
@import "../node_modules/bootstrap/scss/mixins";
@import "../node_modules/bootstrap/scss/root";

// 6. Optionally include any other parts as needed
@import "../node_modules/bootstrap/scss/utilities";
@import "../node_modules/bootstrap/scss/reboot";
@import "../node_modules/bootstrap/scss/type";
@import "../node_modules/bootstrap/scss/images";
@import "../node_modules/bootstrap/scss/containers";
@import "../node_modules/bootstrap/scss/grid";
@import "../node_modules/bootstrap/scss/helpers";

// 7. Optionally include utilities API last to generate classes based on the Sass map in `_utilities.scss`
@import "../node_modules/bootstrap/scss/utilities/api";

// 8. Add additional custom code here
```

### Compiling &mdash;

In order to use your custom Sass code as CSS in the browser, you need a Sass compiler. Sass ships as a CLI package, but you can also compile it with other build tools like Gulp or Webpack, or with a GUI applications. Some IDEs also have Sass compilers built in or as downloadable extensions.

We like to use the CLI to compile our Sass, but you can use whichever method you prefer. From the command line, run the following:

```sh
# Install Sass globally
npm install -g sass

# Watch your custom Sass for changes and compile it to CSS
sass --watch ./scss/custom.scss ./css/custom.css
```
