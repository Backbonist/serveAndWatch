# serveAndWatch

Not yet stable.

A very simple http server (forked from [serve](https://github.com/visionmedia/serve)) that force
browsers to reload when the server detects file changes.

Use the `--watch` or `-w` option to activate this feature.

The watch mode has been borrowed from [https://github.com/mklabs/mockerie](mockerie) by the genious [mklabs](https://github.com/mklabs).

## Installation

    $ git clone https://Filirom1@github.com/Backbonist/serveAndWatch.git
    $ cd serveAndWatch
    $ npm intall -g

## Usage

```

Usage: serve [options] [dir]

Options:

  -v, --version       output the version number
  -F, --format <fmt>  specify the log format string
  -p, --port <port>   specify the port [3000]
  -w, --watch         watch dir and reload clients on change
  -H, --hidden        enable hidden file serving
  -S, --no-stylus     disable stylus rendering
  -J, --no-jade       disable jade rendering
  -I, --no-icons      disable icons
  -L, --no-logs       disable request logging
  -D, --no-dirs       disable directory serving
  -h, --help          output usage information

```

## Examples

 HTTP Accept support built into `connect.directory()`:
 
     $ curl http://local:3000/ -H "Accept: text/plain"
     bin
     History.md
     node_modules
     package.json
     Readme.md

  Requesting a file:

    $ curl http://local:3000/Readme.md

     # serve
     ...

  Requesting JSON for the directory listing:

    $ curl http://local:3000/ -H "Accept: application/json"
    ["bin","History.md","node_modules","package.json","Readme.md"]

 Directory listing served by connect's `connect.directory()` middleware.

  ![directory listings](http://f.cl.ly/items/100M2C3o0p2u3A0q1o3H/Screenshot.png)

## License 

(The MIT License)

Copyright (c) 2011 TJ Holowaychuk &lt;tj@vision-media.ca&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
