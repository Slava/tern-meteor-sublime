# Tern.js Meteor for Sublime Text 3

![demo.gif](/img/demo.gif)

This is a repository with a package for the Sublime Text 3 editor. By running a
customized version of Tern.js, this package provides an autocompletion option
for developing Meteor applications in JavaScript.

Interested in this for a different editor? Check out [this project](https://github.com/slava/tern-meteor).

This package is a fork of the [original `tern_for_sublime`
package](https://github.com/marijnh/tern_for_sublime). You can find the original
README in this repository as [Original_README.md](./Original_README.md).

## Installation

There are two parts to the installation. First, let your Sublime Text 3 know to
autocomplete words on the dot character (`.`):

1. Open Sublime Text 3
2. Open "Preferences", "Settings - User"
3. Add a line to your JSON (inside the main object):
	`, "auto_complete_triggers": [ { "characters": "<", "selector": "text.html" }, { "characters": ".", "selector": "source.js" } ]`

The second part is to install the package itself. The automatic way is to
install it from the Package Control.

1. Install the Package Control from <https://packagecontrol.io/>
2. Install this package by running "Cmd/Ctrl + Shift + P" -> "Install Package" -> "Meteor Autocomplete (TernJS)"

The manual way is to clone this repo in your Sublime Text 3 editor's "Packages"
folder. See [this handy page by
floobits](https://floobits.com/help/plugins/sublime) to learn more.

Restart your Sublime Text 3 editor.

## Usage

### Autocompletion

This package searches your source tree for the folder called ".meteor" or a "package.js" file. 
Once it is found, the package considers its parent to be the root of your Meteor
project or package.

In addition to the default Meteor symbols generated out of the documentation,
you get the autocompetion between files and packages. This package is not smart
enough to understand the packages dependencies, but it can distinguish local
files scope as well as the global scope.

### Jump to definition

Put your cursor on a symbol and press the `alt+.` combination to jump to the
symbol definition. You can jump back to where you started by pressing the
`alt+,` combination.

Alternatively, you can select the "TernJS: Jump To Definition" item from the
command palette.

### Look up type of selection

![show type](/img/demo2.gif)

Put your blinking cursor on a symbol or select an expression and run "TernJS:
Show Type For Selection" from the command palette.

### Look up documentation of selection

Similarly, you can get an API documentation excerpt and a link to the docs if
you run "TernJS: Show Documentation For Selection" from the command palette.

By default, this plugin provides docs for Meteor APIs, as well as APIs for
node.js, jQuery, and browser/ES5,6 features.

### Jump to the Template declaration file

You can find the `.html` Template file just by looking at its JavaScript
reference. You can call the same "TernJS: Jump To Definition" command or press
`alt+.`.

![jump to template](/img/demo3.gif)

### Using Meteor Packages from Atmosphere

This plugin will find and analyze all 3rd party packages your app uses if you
run your app with the `meteor` command at least once. Every time you update your
used packages, you would need to trigger the re-reading of the
`.meteor/versions` file (either by restarting the Tern server or restarting
Sublime or editing and saving the versions file).

![use Atmosphere packages](/img/demo4.gif)

## Using Meteor with Sublime? Here is more!

Here is a list of recommended Sublime Text packages by other authors you might want to install.

- Gitignored File Excluder - ignores lots and lots of build files from your search queries


## Background

- https://www.youtube.com/watch?v=OxzdNZCxPjk
- https://www.youtube.com/watch?v=CcPZ56t8x4I
