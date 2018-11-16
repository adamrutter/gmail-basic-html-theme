# Gmail Basic HTML Theme

Updates the styling of the basic HTML Gmail view to that of the full fat JavaScript version, using custom styles in Firefox.

## Installation

Firefox reads custom styles from `userContent.css`, found in the `chrome` sub-directory of your __profile__ directory. [Instructions on how to find your profile directory](https://support.mozilla.org/en-US/kb/profiles-where-firefox-stores-user-data#w_how-do-i-find-my-profile).

_Directory paths will be relative to the __profile__ folder._

### Preparation

1. Download the theme. Either `git clone https://gitlab.com/adamrutter/gmail-basic-html-theme.git` or use the download button.
2. We need to enable some essential syntax to ensure the styles only apply to the correct pages. Change the boolean `layout.css.moz-document.content.enabled` to `true` in [about:config](about:config).
3. Determine whether `chrome/userContent.css` already exists.

### If `chrome/userContent.css` doesn't already exists.

* Copy/move `userContent.css` to `chrome/`.

### If `chrome/userContent.css` already exists.

The contents of the downloaded `userContent.css` needs to be appended to your current `userContent.css`. Either:

* Copy the contents across using a text editor
* `cat gmail-basic-html-theme/userContent.css > chrome/userContent.css`