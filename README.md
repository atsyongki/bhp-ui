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

## Using the SCSS

The SCSS is designed so that it can be included and extended within the context
of an active project. Two major entry points in `scss/index-dark.scss` and
`scss/index-light.scss` which may be sufficient for your needs, and which are
also provided as simple examples of how to use the SCSS.

If you want to create new theme, you can create a new `scss` file in your
repository containing
ex. blue theme
```
@import 'base';
@import 'themes/blue-variables';

.blue-theme {
  @import 'components';
}

```

The order of the files is important and they are described below:

1. `themes/blue-variables`: specifies the variables for the light theme;
2. `components`: contains the bulk of styles.
