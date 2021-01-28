# playground-util

This is a script for setting up a super-quick local playground for frontend development. Once installed, you can hit `play <playground-name>` in your Terminal and it will bootstrap a ready-to-code barebones HTML project, fire up a dev server, open the page in the browser and the project in VS Code.

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
$ play ls
```

will output a list of all existing playgrounds.