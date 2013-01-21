##PyroAdmin
======================

### 1. Install Development Tools (LESS, Recess, Bower)
------
+ **dependencies**
Our makefile depends on you having recess, connect, uglify.js, and jshint installed. To install, just run the following command in npm:

```
$ npm install bower recess less -g
```

+ **build** - `make`
Runs the recess compiler to rebuild the `/less` files and compiles the docs pages. Requires recess and uglify-js. <a href="http://twitter.github.com/bootstrap/extend.html#compiling">Read more in our docs &raquo;</a>

+ **test** - `make test`
Runs jshint and qunit tests headlessly in [phantomjs](http://code.google.com/p/phantomjs/) (used for ci). Depends on having phantomjs installed.

+ **watch** - `make watch`
This is a convenience method for watching just Less files and automatically building them whenever you save. Requires the Watchr gem.


### 2. Download Bootstrap
------
Download and unpack [PyroAdmin](https://github.com/pyrocms/pyroadmin). In terminal, navigate to `assets/` and run the command `make bootstrap` to update to the latest version of Bootstrap.


### 3. Customize Bootstrap
------
Make your customizations to the two files found in the `less` directory, `variables.less` and `theme.less`.


### 4. Build Customized Bootstrap
------
In the `assets` directory, run `make theme`. The compiled CSS files will be created in the `css` directory.
