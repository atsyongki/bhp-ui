# BHP UI

BHP UI library. A customised Bootstrap deployment with two themes, along with
some extra components.

## Getting started: NPM

If you are using `npm` or `yarn` in your project, run

```
yarn add bhp-ui
```

to install this library. The required peer dependencies for the package
(currently bootstrap and material-design-icons) will be listed, so install
those too.

You can now reference the compiled CSS files in the `css` directory, or access
the SCSS directly via the `scss` directory.

## Getting started: no NPM

Download the `css/index-dark.css` or `css/index-light.css` files and add them
to your static site. You need to add `class="light-theme"` or
`class="dark-theme"` to the root `html` element of your project.

## Structure

In order to support multiple themes is important that files are loaded as described below:

```
@import 'base';
@import 'themes/light/light-colors';
@import 'themes/light/light-variables';

.light-theme {
  @import 'components';
}
```

1. `base`: loads the core base functions, variables and mixins;
1. `themes/light/light-color`: specifies the colour pattern for the theme;
1. `themes/light/light-variables`: specifies the styling variables for the theme;
2. `components`: contains the bulk component styles
