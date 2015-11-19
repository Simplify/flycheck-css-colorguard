# flycheck-css-colorguard

[![License GPL 3][https://img.shields.io/badge/license-GPL_3-green.svg?dummy]][https://github.com/simplify/flycheck-css-colorguard/blob/master/COPYING]

This is extension for [Flycheck][http://www.flycheck.org/].
It uses [CSS Colorguard][https://github.com/SlexAxton/css-colorguard] and
warns you when colors you've added are too similar to ones that already exist
in your css file.

*Use CSS Colorguard 1.0.0 or higher!*

If you for some reason need to support CSS Colorguard older then 1.0.0, take oldest revision of
`flycheck-css-colorguard.el` and uncomment `:error-parser` and comment
`:error-patterns` code.

![flycheck-irony screenshot](screenshot-flycheck-css-colorguard.png)

## Installation

I'm working om Melpa...

### Manual install

Untill Melpa is sorted out place flycheck-css-colorguard.el somewhere on your system and load it.
You'll need to have flycheck installed.

```cl
;; replace ~/Projects/elisp/flycheck-css-colorguard/ with your location.
(add-to-list 'load-path "~/Projects/elisp/flycheck-css-colorguard/")
(load-library "flycheck-css-colorguard")
(eval-after-load 'flycheck
   '(progn
      (require 'flycheck-css-colorguard)
      (flycheck-add-next-checker 'css-csslint
                                 'css-colorguard 'append)))
```

## Usage

Just open any css file. If flycheck is properly configured, flycheck-css-colorguard will start automatically.


## License

This program is free software: you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation, either version 3 of the License, or (at your option) any later
version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A
PARTICULAR PURPOSE.  See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with
this program.  If not, see http://www.gnu.org/licenses/.
