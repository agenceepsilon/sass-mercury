# Changelog

## 2.1.6

* Add ``.otf`` font format. (#19)

## 2.1.5

* Add ``sache.json`` for Sache.in manager.

## 2.1.4

* ``font-face`` fix `src` return *([#17](https://github.com/agenceepsilon/sass-mercury/issues/18))*

## 2.1.3

* Publish on NPM

## 2.1.2

* Helpers:
    * Add ``.ir`` class for image replacement

## 2.1.1

* Mixins:
    * ``breakpoint`` fix css syntax for Internet Explorer issue
    
## 2.1.0

* Mixins:
    * ``font-face`` add WOFF2 and news formats option *([#17](https://github.com/agenceepsilon/sass-mercury/issues/17))*
    * ``gradient`` change prefixes option
    * ``selection`` change prefixes option
    * ``retina`` clean code
* Normalize deleted

## 2.0.3

* ``bower.json`` update

## 2.0.2

* Mixins:
    * Fix retina names

## 2.0.1

* Mixins
    * ``retina`` rename to ``retina-compass`` ([#13](https://github.com/agenceepsilon/sass-mercury/issues/13))
    * ``retina-legacy`` rename to ``retina`` ([#13](https://github.com/agenceepsilon/sass-mercury/issues/13))
    * ``breakpoint``: fix prefix class ([#14](https://github.com/agenceepsilon/sass-mercury/issues/14))

## 2.0.0

* Sass 3.3.0 minimal request ([#7](https://github.com/agenceepsilon/sass-mercury/issues/7))
* Mixins:
    * Version deleted
    * ``placeholder();`` deleted ([#4](https://github.com/agenceepsilon/sass-mercury/issues/4))
    * ``box-sizing();`` deleted ([#3](https://github.com/agenceepsilon/sass-mercury/issues/3))
    * ``breakpoint();``:
        * Adding iPhone width ([#8](https://github.com/agenceepsilon/sass-mercury/issues/8))
        * Adjust pixel size if we choose two width between ``min-width`` and ``max-width``
    * ``retina();``:
        * Add ``$pixel-ratio`` option, ``1.5`` by default ([#12](https://github.com/agenceepsilon/sass-mercury/issues/12))
    * ``retina-legacy();``: ([#10](https://github.com/agenceepsilon/sass-mercury/issues/10))
        * Mixin dedicated to generating high definitions pictures for those who do not use the library to generate the Compass Sass.
* Helpers:
    * ``hidden`` class update ([#6](https://github.com/agenceepsilon/sass-mercury/issues/6))
* Normalize ``3.0.2``

## 1.1.1

* Comments update

## 1.1.0

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

## 1.0.1

* Mixin updated:
    * ``clearfix();`` 1.0.5
        * BEM class fix
* Helpers:
    * BEM class fix

## 1.0.0

* Initial release
