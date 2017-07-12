As with most GitHub accounts, many of my repositories are simply forks of other people's repositories. Here are the ones that are actually mine.

* [`gulp-dest-atomic`](/00dani/gulp-dest-atomic) - a drop-in replacement for the `gulp.dest` call which always writes new files to disk atomically. This is achieved by writing the file under a temporary name, and then renaming it only when writing is complete.
* [`livemacros.vim`](/00dani/livemacros.vim) - Vim plugin to aid in writing advanced macros. The full text of the macro is displayed in a small window and is fully editable; as the macro is changed, it is instantly applied to the buffer you were editing, so its effect is immediately visible.
* [`path-format`](/00dani/path-format) - A Node.js polyfill for the `path.format` method. I needed that method and could only find polyfills for `path.parse`, so I wrote my own. Very simple!
* [`tumblr-assets`](/00dani/tumblr-assets) - The theme, styles, and scripts for [my Tumblr blog](https://00dani.tumblr.com). They're published here primarily so that I can use GitHub Pages to serve them to visitors.
* [`vim-nginx`](/00dani/vim-nginx) - There's an official Vim plugin for nginx configuration files living in the main nginx repo. For ease of installation, this repository is a mirror of *just* the Vim plugin from the nginx repository. It's automatically synchronised and should always be up-to-date.
* [`wundernap`](/00dani/wundernap) - A script for adding "snooze" support to Wunderlist. It's pretty hacky? Basically, it moves tasks into separate Snoozed list, and then moves them back when their reminder date/time arrives.  You've gotta run it regularly, perhaps with a cron job.

# `dot-*`

Repos beginning with `dot-` are my dotfiles. They're split across several repositories in order to keep concerns separated. The most important ones are `dot-dots` and `dot-stow`:

* [`dot-dots`](/00dani/dot-dots) - `dots` is a simple shell script which quickly bootstraps my dotfiles on a new system, and once installed can be used to manage local dot repositories. When first run, it will install itself, [`dot-stow`](/00dani/dot-stow), [`dot-git`](/00dani/dot-git), [`dot-vim`](/00dani/dot-vim), and [`dot-zsh`](/00dani/dot-zsh).
* [`dot-stow`](/00dani/dot-stow) - a somewhat modified version of the [GNU Stow](https://www.gnu.org/software/stow/) symlink farm manager. Stow is used to install every dot repository, including itself, into your home directory.  This version of Stow is prepackaged for self-hosting regardless of its actual filesystem location, and in addition it supports a new feature, the `.stow-rename` file, which allows the symlinked version of a file to have a different name to the original. (It's mostly used so that `~/.config` can point to `$REPO/config`, without needing the dot inside as well.)
