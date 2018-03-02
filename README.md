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

If you want to customise the SCSS, you can create an `scss` file in your
repository containing

```
@import '~bhp-ui/scss/themes/light';
@import '~bhp-ui/scss/0-root';
@import '~bhp-ui/scss/1-base';

.light-theme {
  @import '~bhp-ui/scss/2-within-theme';
}

```

The order of the files is important and they are described below:

1. `themes/light`: specifies the variables for the light theme;
2. `0-root`: includes reboot styles. Does not depend on any theme variables;
3. `1-base`: contains mixings and variables (no styles);
4. `2-within-theme`: contains the bulk of styles.
