# playground-util

This is a script for setting up a super-quick local playground for frontend development. You can choose between:

- a barebones HTML project
- a simple Webpack setup that will allow you to install and import npm dependencies out of the box.

Once installed, you can hit `play <playground-name>` in your Terminal and the util will bootstrap the project if necessary, fire up a dev server, open the page in the browser and the project in VS Code.

## Requirements

This script relies on the following software to be installed and set up on your machine:

- [VS Code](https://code.visualstudio.com/) with [`code` shell command](https://code.visualstudio.com/docs/setup/mac#_launching-from-the-command-line) installed
- [Node.js](https://nodejs.org/en/) >= v6
- [http-server](https://www.npmjs.com/package/http-server#globally-via-npm) for Node installed globally

## Setup

Clone or download this repo to any location on your machine.

Add the `./script/` directory from this repo to your `$PATH`. I use bash, so I add the following line to `~/.bash_profile`:

``` bash
export PATH=/path/to/playground-util/script/:$PATH
```

Create a directory `~/code/_playgrounds/`

``` shell
$ mkdir ~/code/_playgrounds/
```

Finally, restart your Terminal.app to apply the changes.

## Usage

``` shell
$ play playground-name
```

will create a directory called "playground-name" inside the `~/code/_playgrounds/` directory, create the index.html, fire up a http-server, open the page in your browser and open the directory in VS Code.

If a directory `~/code/_playgrounds/playground-nanme/` already exists, it will open the existing one instead.

``` shell
$ play playground-bundled --webpack
```

will setup a copy of [playground-template-webpack](https://github.com/mgschoen/playground-template-webpack). For all subsequent boots of this project, calling `play playground-bundled` will be sufficient. The util will auto-detect that this is a webpack project.

``` shell
$ play ls
```

will output a list of all existing playgrounds.