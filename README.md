# Presentable macOS ✨
Notes and Snippets to optimize macOS for screen recording and screen sharing.


## Terminal

Terminals are highly customizable and can be fun to configure. Still, it's important to create a clean and distraction free experience when performing tasks in the terminal. This may also mean to decide against a Zsh configuration framework like [Oh My Zsh!](https://ohmyz.sh/) or a Zsh theme like [powerlevel10k](https://github.com/romkatv/powerlevel10k). Otherwise you may confuse students or spend time answering questions on why the student's terminal doesn't look as fancy as yours.

### Decide on the Terminal Emulator

There are exciting terminal emulators like [Warp](https://www.warp.dev/) out there. For presentations, a more basic terminal emulator like [iTerm2](https://iterm2.com/) might be a better choice, though. It's a free application with the right amount of configuration options.

### Customize Your Prompt

For an additional personal touch, you can customize your terminal sessions with a custom colored prompt. For a green `$`, add this line to your `~/.zshrc` file:

```sh
PROMPT='%F{green}$ %f'
```

Customizing your prompt helps you to minimize the characters that every prompt line starts with. Also, you can hide your computer name that's shown in the default prompt.

See the [Zsh Wiki](https://wiki.archlinux.org/title/zsh#Colors) for more color options and additional instructions on how to customize your prompt.

### Hush the Last Login

When you create a new terminal session you can see the your last terminal login displayed like this:

```
Last login: Fri Feb  2 13:02:47 on ttys000
```

To surpress this message, you can create an empty `.hushlogin` file in your user folder:

```sh
$ touch ~/.hushlogin
```

When macOS sees this file, the last login message doesn't appear anymore.

## Finder

The Finder is great for giving an overview of a project's structure. To keep the focus on what you want to show, these are some things to keep in mind:

- Always hide the sidebar if you don't need it to show something.
- Prefer the list view and unfold the folders you want to show.
- Sort the list by name. Otherwise files and folders will jump after editing.
- Always show file extensions.

### Hidden Files

Depending on the situation it can make sense to always show hidden files. This is especially important in an development environment. For presentations hidden files can be distracting or even confusing. 

To swiftly toggle the display of hidden files you can use this shortcut in Finder:

- **Toggle Hidden Files:** <kbd>Cmd</kbd> + <kbd>Shift</kbd> + <kbd>.</kbd>

## Git

There are certain files that you probably don't want ever to be part of your commits. Instead of ignoring those unwanted files every time when you create a repository, you can add them to your global Git ignore file:

```sh
$ echo .DS_Store >> ~/.config/git/ignore
```
