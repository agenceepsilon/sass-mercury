# Mercury

[![GitHub version](http://img.shields.io/github/release/agenceepsilon/sass-mercury.svg?style=flat-square)](https://github.com/agenceepsilon/sass-mercury/releases)

Sass mixins & functions library!

## Requirements

| Requirements                 | Versions |
| ---------------------------- | -------- |
| [Sass](http://sass-lang.com) | ^3.3.0   |

## Functions

| Functions |
| --------- |
| em        |
| rem       |

## Mixins

| Mixins     | Functions dependencies |
| ---------- | ---------------------- |
| breakpoint | No                     |
| font-face  | No                     |
| gradient   | No                     |
| grid       | **breakpoint**         |
| opacity    | No                     |
| rem-size   | **rem**                |
| retina     | No                     |
| selection  | No                     |

## Placeholders

| Placeholder | Functions dependencies |
| ----------- | ---------------------- |
| ellipsis    | No                     |
| hyphens     | No                     |

## Variables

| Variables          | Default   | Mixins dependencies        |
| ------------------ | --------- | -------------------------- |
| ``$oldie``         | ``false`` | All mixins config use this |
| ``$media-queries`` | ``true``  | breakpoint                 |

### $oldie

This variable is used to distinguish the global settings and those dedicated solely to Internet Explorer. She created an alternative version of the parameters and write them in a different file. File that should only be called by Internet Explorer.

Variable ``$oldie: false;`` is required in the file ``_mercury.scss``.

#### Config

In your Sass folder at the root, create a file ``oldie.scss`` or any other name. This generated a new ``.css`` file, called only by Internet Explorer.

The file, ``oldie.css``, is a copy of your main CSS file, except that the parameters dedicated to Internet Explorer will be written to the file. In it, import the main CSS file ``@import "name";``, which already contains all the libraries.

On top of the file place the variable ``$oldie: true;``.

Call the file with conditional comments.

#### Syntax

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

### $media-queries

This variable is used to decide whether the parameters placed in a breakpoint is generated or not.

The main use is for Internet Explorer 7 and 8. It takes place in the false option in a dedicated IE file. Only parameters desktop will be generated in the CSS file.
