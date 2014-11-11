# animate.scss

A powerful, highly customisable SCSS port of Dan Eden's animate.css library.

http://daneden.github.io/animate.css/

Offers feature parity to version 3.2


## Installing

```bower install animate-scss```

Once installed, ```@import 'src/_animate'``` from your bower_components folder into your own project (adjusting the path to the import as necessary). Be sure to set any variable overrides beforehand.


## Customisation Options

#### Optional Modules

All of the animations are optional, and easily switched on and off using Sass
variables. This should result in smaller end file sizes, as you only need to enable the modules
you are using.

Set your enable variables _before_ importing Animate into your own stylesheet. The available module variables can be found [in the modules settings file](https://github.com/benhodgson87/animate.scss/blob/master/src/settings/_modules.scss).

##### Enabling Modules
```scss
$enable-flip-out-y: true;
$enable-hinge: true;
$enable-zoom-out: true;
```

##### Enable All Modules
While developing, it may be useful to have every module enabled. To do this you can set:
```scss
$enable-all-modules: true;
```


#### Vendor Prefixes

Vendor prefixes can be enabled or disabled through a single Sass variable, that
can be set either within the core Animate.scss code, or in any file that includes
the library.

Vendor prefixes are switched off by default, allowing you to use tools such as
Autoprefixer to handle prefixing.

When enabled, all necessary CSS declarations include vendor prefixes for Webkit,
Mozilla, and Opera browsers.


#### Class Naming

All animation class names are defined through a single config file, allowing you
to alter how the output CSS classes are named.

You can also prefix a namespace to all class names, giving you flexibility to use
methods such as BEM, prefixing the animation class with your choice of modifier.
eg. ```.animation--bounce-in```
_(Note that this only affects class names, not animation names)_

```scss
// Namespace animations
$name-prefix: 'anim--';

// Change an animation name
$name-bounce-in: 'tigger-enter';

// The output CSS for .bounce-in will become:
.anim--tigger-enter {
  animation-name: "tigger-enter";
}
```


## Contributing

Contributions are greatly appreciated, and Pull Requests are always welcome!

When contributing, please take note of existing coding style, particularly the
use of 4-space soft tabs for indentation, and a trailing linebreak at the end of
files.
