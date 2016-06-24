# SCSS

All global / shared scss styles should be placed in `scss/styles`

All @mixins, variables, etc should be place in `scss/meta`

### 1) RESOURCES (mixins, variables, etc)
SCSS helpers are loaded via your component's main .scss file. This give you access to all our global mixins, variables, etc

EXAMPLE: `/app/scss/main.scss` should include `_core.scss` like so:
```
 @import '../../libs/core-styles/core';
```

### 2) STYLES (actual display styles)
Reference nanobox globals styles from your `stage.scss` file. These global styles will be loaded into the rails environment but will not be compiled into your library's scss file.

EXAMPLE: `/stage/stage.scss` should include `styles.scss` like so:
```
@import "../libs/core-styles/styles.scss";
```
