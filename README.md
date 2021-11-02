# SRFI nnn: Browse URL

by Firstname Lastname, Another Person, Third Person

## Status

Early Draft

## Abstract

This SRFI defines a `browse-url` library similar to the Emacs package by that name.

## Issues

* Different URL schemes: mailto, ftp, gemini, etc.

## Rationale

One common task is opening documentation from the REPL.

## Specification

### Definition of a browser

A browser is an object that can do to things:

- Check whether the browser is available in general.
- Check whether the browser supports opening a given URL.
- Open the given URL.

### Exceptions

`(browse-url-error? object)`

`(browse-url-error-url error)`

`(browse-url-error-browser error)`

### Settings

`(browse-url-browsers [list])` (parameter)

The value is a list of zero or more browsers, tried in order from first to last.

`(browse-url-environment [plist])` (parameter)

The following are:

* `graphical?`

### API

Settings for the browser.

`(browse-url-find-browser url)`

Figure out the browser.

`(browse-url url)`

Browse

## Examples

`(browse-url "gemini://www.scheme.org/") -> lagrange`

`(browse-url "https://www.scheme.org/")`

## Implementation

## Acknowledgements

## References

## Copyright

Copyright (C) Firstname Lastname (20XY).

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
