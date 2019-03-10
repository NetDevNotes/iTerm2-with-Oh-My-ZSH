# iterm2-with-oh-my-zsh
How to install iTerm2 and oh-my-zsh and why you might bother.

## What is iTerm2
Terminal in OSX is nice and simple but low on features. iTerm2 is a replacemnt for the Terminal built into a MAC, and offers many additional features, some of which listed below:

* Lots of keyboard shortcuts, so less time spent touching the mouse.
* Advanced split screens (horizontal/vertical)
* Mouseless copy
* Advanced command history
* Open iTerm2 from Finder
* Autocomplete list based on your input
* Instant Replay can take you back in time! But probably not to October 21st 1985.

> I'll go into more detail on some of the best features later in the artice.

## What is Oh-My-ZSH
Zsh is a UNIX command interpreter (aka a shell, similar to bash).  Oh My Zsh is an open source framework for managing Zsh configuration. It also offers many additional features, some of which listed below:

* 250+ plugins that make using your favorite tools such as Ansible, GitHub, Python, Pyenv, easier and faster to use. 
* 140+ cool themes to make your terminal, such as iTerm2, look amazing.  
* You can even start your favourite track in Spotify from the command line. Why?  I dont know, but it was the first thing I did :smile:

## The power of team work!
So as you can imagine from listing just a few of the features iTerm2 and Oh-My-ZSH offer, you can probably understand why using both together is a powerful combination.

# Installation

## iTerm2
1. Download the latest stable version from [HERE](https://www.iterm2.com/downloads.html)
2. Extract the compressed file and copy iTerm.app to your Application folder.
3. Open iTerm and grant `Full Disk Access` as per the instructions.

## Oh-My-ZSH
1. From a terminal session (iTerm!), use curl to install:

`$ sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`

2. Enter your password when prompted & the program ....is now installed!
```
         __                                     __
  ____  / /_     ____ ___  __  __   ____  _____/ /_
 / __ \/ __ \   / __ `__ \/ / / /  /_  / / ___/ __ \
/ /_/ / / / /  / / / / / / /_/ /    / /_(__  ) / / /
\____/_/ /_/  /_/ /_/ /_/\__, /    /___/____/_/ /_/
                        /____/                       ....is now installed!


Please look over the ~/.zshrc file to select plugins, themes, and options.

p.s. Follow us at https://twitter.com/ohmyzsh.

p.p.s. Get stickers, shirts, and coffee mugs at https://shop.planetargon.com/collections/oh-my-zsh.

➜  ~
```
> Full instructions are available at https://ohmyz.sh/

# Verify ZSH install and ZSH as default shell
You probably want zsh as your default shell, so when you open a terminal session zsh will be used by default.  This is set in your environment variables, below are a few ways to check this is the case:

```
$ echo $SHELL
/bin/zsh
```
```
$ zsh --version
zsh 5.3 (x86_64-apple-darwin18.0)
```
```
$ $SHELL --version
zsh 5.3 (x86_64-apple-darwin18.0)
```
```
$ printenv
[deleted for brevity]
SHELL=/bin/zsh
``` 
> I think you can now be sure zsh is set to your defult shell.. very sure..

# Now What!?
You could go in many directions, but lets be honest, we're going to configure a Theme! 

> The list of zsh themes is located [HERE](https://github.com/robbyrussell/oh-my-zsh/wiki/Themes). Have a look through and find one you like.

## Configuration File
Your ZSH configuration file is located in your Home Directory `~/.zshrc`. This is where you can change themes, amoungst other settings.

Below I am in my home folder and I edit the file using `vi`
```
➜  ~ pwd
/Users/nico
➜  ~ vi .zshrc

# If you come from bash you might have to change your $PATH.
# export PATH=$HOME/bin:/usr/local/bin:$PATH

# Path to your oh-my-zsh installation.
export ZSH="/Users/nico/.oh-my-zsh"

# Set name of the theme to load --- if set to "random", it will
# load a random theme each time oh-my-zsh is loaded, in which case,
# to know which specific one was loaded, run: echo $RANDOM_THEME
# See https://github.com/robbyrussell/oh-my-zsh/wiki/Themes
ZSH_THEME="robbyrussell"
```
> You can use any text editor to edit the file, but vi is something worth learning, just use a cheatsheet, like [THIS](http://www.lagmonster.org/docs/vi.html) or [THIS](https://www.gosquared.com/resources/vi-cheat-sheet/).

The default theme which is enabled is shown below, all you have to do is change the theme name and restart your terminal session (or open a new tab) to enable the new theme.  You might choose to copy the line and use hash to disable all but one theme, then you can have a list of your favorites in the config file:
```
#ZSH_THEME="robbyrussell"
ZSH_THEME="gianu"
```
![gianu theme](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/gianu_theme.png)

> Notice above that im being told the folder I am currntly in is a `master` [GitHub](https://github.com/NetDevNotes/Complete-Python-3-Bootcamp.git) repository. Pretty :cool:

If you are not feeling very colourful, maybe its Monday or its raining, you can set ZSH_THEME to be blank: 

`ZSH_THEME=""`

# Split Panes (iTerm2 method)

You to divide a tab into many rectangular panes, each of which is a different terminal session: 

### Shortcuts 

Shortcut | Function
------------ | -------------
cmd-d | Divide vertically
cmd-shift-d | Divide horizontally
cmd-opt-arrow | Navigate split panes
cmd-[] | Navigate split panes    

![Split Panes](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/split_panes.png)






 
