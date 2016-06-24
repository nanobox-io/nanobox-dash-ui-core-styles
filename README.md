## Use in a gulp project:

### 2) SHARED SCSS RESOURCES
Reference scss helpers via your component's main scss file. This give you access to all our global mixins, variables, etc

EXAMPLE: `/app/scss/main.scss` should include `_core.scss` like so:
```
 @import '../../libs/core-styles/core';
```

### 2) SHARED STYLES
Reference nanobox globals styles from your `stage.scss` file. These global styles will be loaded into the rails environment but will not be compiled into your library's scss file.

EXAMPLE: `/stage/stage.scss` should include `styles.scss` like so:
```
@import "../libs/core-styles/styles.scss";
```
