# Tern.js Meteor for Sublime Text 3

This is a repository with a package for the Sublime Text 3 editor. By running a
customized version of Tern.js, this package provides an autocompletion option
for developing Meteor applications in JavaScript.

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
install it from the Package Control (isn't available in the registry yet).

The manual way is to clone this repo in your Sublime Text 3 editor's "Packages"
folder. See [this handy page by
floobits](https://floobits.com/help/plugins/sublime) to learn more.

Restart your Sublime Text 3 editor.

## Usage

### Autocompletion

This package searches your source tree for the folder called ".meteor". Once it
is found, the package considers its parent to be the root of your Meteor
project.

In addition to the default Meteor symbols generated out of the documentation,
you get the autocompetion between files and packages. This package is not smart
enough to understand the packages dependencies, but it can distinguish local
files scope as well as the global scope.

### Jump to definition

Put your cursor on a symbol and press the `alt+.` combination to jump to the
symbol definition. You can jump back to where you started by pressing the
`alt+,` combination.

