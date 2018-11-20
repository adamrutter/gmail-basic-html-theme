# Gmail Basic HTML Theme

Updates the styling of the basic HTML Gmail view to that of the full fat JavaScript version (as much as possible), using custom styles in Firefox.

## Installation

Firefox reads custom styles from `userContent.css`, found in the `chrome` sub-directory of your __profile__ directory. [Instructions on how to find your profile directory](https://support.mozilla.org/en-US/kb/profiles-where-firefox-stores-user-data#w_how-do-i-find-my-profile).

Therefore, we simply need to place our custom styles in the correct location.

### 1. Download the theme. 

Either:

* Use the download button. You will need to decompress/unzip the downloaded files.
* `git clone https://gitlab.com/adamrutter/gmail-basic-html-theme.git` if you are using a CLI.

### 2. Enable some options

We need to enable some essential syntax to ensure the styles only apply where we want them to:

* Open the [about:config](about:config) page.
* Search for `layout.css.moz-document.content.enabled`.
* Change `layout.css.moz-document.content.enabled` to `true` by double clicking.

### 3. Add the theme to your `chrome` directory

Now we just need to move the downloaded styles to our `chrome` directory, a sub-directory of your __profile__ directory.

__If you already have a `userContent.css` in this directory__, the content of the downloaded `userContent.css` should be appended to the existing file. You can:

* Copy/paste the content of the downloaded `userContent.css` to your current file using a text editor.
* Use a command such as `cat` in the CLI. `cat downloads/userContent.css > chrome/userContent.css` _Note: the paths will almost certainly be different in your case._

__If you do not already have a `userContent.css`__, you just need to move the downloaded `userContent.css` to the correct directory.

* Move or copy/paste the downloaded `userContent.css` to your `chrome` directory.
* 

## Constraints

There are some constraints with bringing the theme up to date with modern Gmail, mainly arising from the inability to modify any `html` code.

One obvious one is using text instead of icons for the mailbox controls. Whilst it would be possible to use icons, it is not possible to use tooltips to indicate what the buttons do. Without being able to add any `html` for tooltips, or add pseduo elements to an `input` (the buttons are actually an `<input type="submit">`), using icons would mean a poor user experience.