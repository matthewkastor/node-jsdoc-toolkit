This fork just updates package.json to use node >= 04.10, publishes as a new npm package "jsdoc-toolkit"

======================================================================

DESCRIPTION:

This is the source code for JsDoc Toolkit, an automatic documentation
generation tool for JavaScript. It is written in JavaScript and is run
from a command line (or terminal) using the Node.JS JavaScript runtime
engine.

Using this tool you can automatically turn JavaDoc-like comments in
your JavaScript source code into published output files, such as HTML
or XML.

For more information, to report a bug, or to browse the technical
documentation for this tool please visit the official JsDoc Toolkit
project homepage at http://code.google.com/p/jsdoc-toolkit/

For the most up-to-date documentation on JsDoc Toolkit see the 
official wiki at http://code.google.com/p/jsdoc-toolkit/w/list

======================================================================

REQUIREMENTS:

Node.JS interpreter http://nodejs.org

======================================================================

INSTALLATION:

`npm install jsdoc-toolkit`

or, you can install it globally and have it available for all your projects.

`npm install jsdoc-toolkit -g`

Make sure to add your global `node_modules/.bin` directory to your path for
convenient access to your global packages from the command line.

======================================================================

USAGE:

From Scripts:

This module exports jsdoctoolkit, it has a run method that accepts a single
argument: an array of strings corresponding to the exact command line arguments
you would use, in the same order as you would give them on the command line.

```
var jsdocToolkit = require('jsdoc-toolkit').jsdoctoolkit;

jsdocToolkit.run(['--help']);
```

```
var jsdocToolkit = require('jsdoc-toolkit').jsdoctoolkit;
var argz = [
    "-d=./docs/",  // output directory for documentation.
    "-o=./jsdoc-toolkit-log.txt" // file for logging messages like warnings.
    "cli.js" // the file or directory to generate documentation for.
];
jsdocToolkit.run(argz);
```

Command line:

Given a file named mycode.js that you want documented:

if you've installed this package globally it's as easy as running

`jsdoc-toolkit -a mycode.js`

If you have installed jsdoc-toolkit into your package instead, from the package
root run

`node_modules/.bin/jsdoc-toolkit -a mycode.js`

In both cases the output documentation files will be saved to a new directory
named "out" (by default) in the current directory, or if you specify a
`-d=somewhere_else` option, to the somewhere_else directory.

For help (usage notes) enter this on the command line:

`jsdoc-toolkit --help`

More information about the various command line options used by JsDoc
Toolkit are available on the project wiki.

======================================================================

TESTING:

To run the suite of unit tests included with JsDoc Toolkit enter this
on the command line:

npm test

To see a dump of the internal data structure that JsDoc Toolkit has
built from your source files use this command:

jsdoc-toolkit mycode.js -Z

======================================================================

LICENSE:

JSDoc.pm

This project is based on the JSDoc.pm tool, created by Michael
Mathews and Gabriel Reid. More information on JsDoc.pm can
be found on the JSDoc.pm homepage: http://jsdoc.sourceforge.net/

Complete documentation on JsDoc Toolkit can be found on the project
wiki at http://code.google.com/p/jsdoc-toolkit/w/list

JsDoc Toolkit

All code specific to JsDoc Toolkit are free, open source and licensed
for use under the X11/MIT License.

JsDoc Toolkit is Copyright (c)2009 Michael Mathews <micmath@gmail.com>
Additional portions are Copyright (c)2010 Aaron Wirtz <me@awirtz.com>

This program is free software; you can redistribute it and/or
modify it under the terms below.

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions: The above copyright notice and this
permission notice must be included in all copies or substantial
portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
