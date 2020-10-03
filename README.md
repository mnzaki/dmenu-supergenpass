# dmenu-supergenpass

A shell + perl [dmenu](https://tools.suckless.org/dmenu/) utility to generate a
password and simulate typing it into into the focused window.

Instead of using a password manager, a password is generated from
a "password item" + "master password" combination. This was inspired by, and is compatible with, [SuperGenPass](https://chriszarate.github.io/supergenpass/)

## Usage
Make sure you have `perl`, `xsel`, and `xdotool` installed.

Copy `dmenu-supergenpass` to somewhere in your `$PATH` (like `/usr/local/bin`
for example) and bind it to a key in your Window Manager.

When you need to type a password, focus the window/field for the password and
hit the key combination. You will be presented with "password items" to choose
from. Any text that is in the clipboard selection will also be presented as the
first item (so selecting the domain name in a browser bar for example lets you
use that). Press `Enter` to choose the highlighted item, or `Shift+Enter` to
force choosing whatever text was typed in. Then enter the master password and
press `Enter` to have the password generated and "typed" using `xdotool`


If you need to remove items, remove them from `$HOME/.config/dmenu-supergenpass/items`

## History
Originally published on https://bbs.archlinux.org/viewtopic.php?pid=1123014#p1123014
