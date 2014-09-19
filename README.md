# Mercury [![GitHub version](https://badge.fury.io/gh/agenceepsilon%2Fsass-mercury.png)](http://badge.fury.io/gh/agenceepsilon%2Fsass-mercury) [![Bower version](https://badge.fury.io/bo/sass-mercury.png)](http://badge.fury.io/bo/sass-mercury)

Sass mixins & functions library!

## Functions

| Functions | Versions |
| --------- | -------- |
| em        | N/A      |
| rem       | N/A      |

## Mixins

| Mixins      | Versions | Functions dependencies | helpers.scss dependencies |
| ----------- | -------- | ---------------------- | ------------------------- |
| box-sixing  | 1.3.1    | None                   | No                        |
| breakpoint  | 2.0.0    | None                   | No                        |
| font-face   | 1.0.0    | None                   | No                        |
| gradient    | 1.6.1    | None                   | No                        |
| grid        | 1.0.0    | **breakpoint**         | No                        |
| opacity     | 1.1.0    | None                   | No                        |
| placeholder | 1.0.0    | None                   | No                        |
| rem-size    | 1.2.1    | **rem**                | No                        |
| retina      | 1.1.0    | None                   | No                        |
| selection   | 1.3.1    | None                   | No                        |

## Variables

| Variables        | Default   | Mixins dependencies        |
| ---------------- | --------- | -------------------------- |
| ``$oldie``       | ``false`` | All mixins config use this |
| ``$media-query`` | ``true``  | breakpoint                 |

### $oldie

This variable is used to distinguish the global settings and those dedicated solely to Internet Explorer. She created an alternative version of the parameters and write them in a different file. File that should only be called by Internet Explorer.

Variable ``$oldie: false;`` is required in the file ``_mercury.scss``.

#### Config

In your Sass folder at the root, create a file ``oldie.scss`` or any other name. This generated a new ``.css`` file, called only by Internet Explorer.

The file, ``oldie.css``, is a copy of your main CSS file, except that the parameters dedicated to Internet Explorer will be written to the file. In it, import the main CSS file ``@import "name";``, which already contains all the libraries.

On top of the file place the variable ``$oldie: true;``.

Call the file with conditional comments.

#### Synthax

    .module {
        // For all browsers
        background: blue;
        height: 50px;
        width: 50px;
        @if $oldie {
            // For Internet Explorer only
            background: red;
            height: 100px;
            width: 100px;
        }
    }

### $media-query

This variable is used to decide whether the parameters placed in a breakpoint is generated or not.

The main use is for Intenet Explorer 7 and 8. It takes place in the false option in a dedicated IE file. Only parameters desktop will be generated in the CSS file.

## Helpers

The ``_helpers.scss`` depends on the ``_mercury.scss`` file because some helpers use variables or mixins.

### Hidden class

| Hide...             | Class                |
| ------------------- | -------------------- |
| ...for all          | ``.hidden``          |
| ...for mobile only  | ``.hidden--mobile``  |
| ...for tablet only  | ``.hidden--tablet``  |
| ...for desktop only | ``.hidden--desktop`` |

## Normalize.css

The ``_normalize.scss`` file is completely independent and does not require any functions or mixins the main library. It can be used independently or simply not used!

## Credits

Projects inspirations and forking:

* [Nicolas Gallagher (Normalize.css)](http://necolas.github.io/normalize.css/)
* [Hinerangi Courtenay (Skymaiden)](https://github.com/skymaiden)

## Changelog

### Next release - 2.0.0-beta.7

* Sass 3.3.0 minimal request [#7](https://github.com/agenceepsilon/sass-mercury/issues/7)
* Mixins:
    * Version tag deleted
    * ``placeholder();`` deleted [#4](https://github.com/agenceepsilon/sass-mercury/issues/4)
    * ``box-sizing();`` deleted [#3](https://github.com/agenceepsilon/sass-mercury/issues/3)
    * ``breakpoint();``:
        * Adding iPhone width [#8](https://github.com/agenceepsilon/sass-mercury/issues/8)
    * ``retina-legacy();``: [#10](https://github.com/agenceepsilon/sass-mercury/issues/10)
        * Mixin dedicated to generating high definitions pictures for those who do not use the library to generate the Compass Sass.
* Helpers:
    * ``hidden`` class update [#6](https://github.com/agenceepsilon/sass-mercury/issues/6)

### 1.1.1

* Comments update

### 1.1.0

* Mixins updated:
    * ``box-sizing();`` 1.3.1
        * Delete ``$oldie``
    * ``gradient();`` 1.6.1
            * Delete ``$oldie``
    * ``retina();`` 1.1.0
            * Add ``postfix`` option
            * Variables new names
    * ``selection();`` 1.3.1
            * Delete ``$oldie``
* Mixin deleted:
    * ``clearfix();``

### 1.0.1

* Mixin updated:
    * ``clearfix();`` 1.0.5
        * BEM class fix
* Helpers:
    * BEM class fix

### 1.0.0

* Initial release