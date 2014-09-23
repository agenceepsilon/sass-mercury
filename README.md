# Mercury [![GitHub version](https://badge.fury.io/gh/agenceepsilon%2Fsass-mercury.png)](http://badge.fury.io/gh/agenceepsilon%2Fsass-mercury) [![Bower version](https://badge.fury.io/bo/sass-mercury.png)](http://badge.fury.io/bo/sass-mercury)

Sass mixins & functions library!

## Requirements

| Requirements                        | Versions |
| ----------------------------------- | -------- |
| [Sass](http://sass-lang.com)        | ~3.3.0   |
| [Compass](http://compass-style.org) | ~1.0.0   |

## Functions

| Functions | Versions |
| --------- | -------- |
| em        | N/A      |
| rem       | N/A      |

## Mixins

| Mixins        | Functions dependencies | helpers.scss dependencies | Compass dependencies |
| ------------- | ---------------------- | ------------------------- | -------------------- |
| box-sixing    | None                   | No                        | No                   |
| breakpoint    | None                   | No                        | No                   |
| font-face     | None                   | No                        | No                   |
| gradient      | None                   | No                        | No                   |
| grid          | **breakpoint**         | No                        | No                   |
| opacity       | None                   | No                        | No                   |
| placeholder   | None                   | No                        | No                   |
| rem-size      | **rem**                | No                        | No                   |
| retina        | None                   | No                        | **Yes**              |
| retina-legacy | None                   | No                        | No                   |
| selection     | None                   | No                        | No                   |

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

If you want to hide several resolutions but keep other, add more classes to the same element.

For example: if you want hide mobile and desktop, just put the classes on the element :

    <div class="hidden--mobile hidden--desktop">My div</div>

## Normalize.css

The ``_normalize.scss`` file is completely independent and does not require any functions or mixins the main library. It can be used independently or simply not used!