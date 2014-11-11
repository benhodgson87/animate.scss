# animate.scss

A powerful, highly customisable SCSS port of Dan Eden's animate.css library.

http://daneden.github.io/animate.css/

Offers feature parity to version 3.2


## Installing

Clone this repo, or use [Bower](http://bower.io):

```bower install animate-scss```

Once installed, import the main animate SCSS file from wherever it's been saved (eg. ```bower_components```) into your own project. Be sure to define your settings variables beforehand (see below).

```scss
$enable-zoom-in: true;
$enable-zoom-out: true;

@import '{{path_to_animate}}/_animate.scss';
```

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

You can find available name variables [in the name settings file](https://github.com/benhodgson87/animate.scss/blob/master/src/settings/_names.scss).

##### Example

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

A .editorconfig file is included, please make use of it if your code editor supports it.
