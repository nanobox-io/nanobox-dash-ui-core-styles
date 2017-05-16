# SCSS

All global / shared scss styles should be placed in `scss/styles`

All @mixins, variables, etc should be place in `scss/meta`

### 1) RESOURCES (mixins, variables, etc)
SCSS helpers are loaded via your component's main .scss file. This give you access to all our global mixins, variables, etc

EXAMPLE: `/app/scss/main.scss` should include `_core.scss` like so:
```
 @import '../../lib/assets/core-styles/scss/utils';
```

### 2) STYLES (actual display styles)
Reference nanobox globals styles from your `stage.scss` file. These global styles will be loaded into the rails environment but will not be compiled into your library's scss file.

EXAMPLE: `/stage/stage.scss` should include `styles.scss` like so:
```
@import "../libs/core-styles/styles.scss";
```

### Usage

#### Adding to a project

```bash
git submodule add git@github.com:nanobox-io/nanobox-dash-ui-core-styles.git
```

NOTE: in all Nanobox projects the submodule is added in `/lib/assets/core-styles` so the above command would look like this:

```bash
git submodule add git@github.com:nanobox-io/nanobox-dash-ui-core-styles.git /lib/assest/core-styles
```

#### Existing Submodule

```bash
git submodule init
git submodule update
```

#### Updating

```bash
git submodule foreach pull git origin master
```
