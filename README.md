# iterm2-with-oh-my-zsh :coffee:
How to install `iTerm2` and `Oh-My-ZSH` and why you might bother.

* [What is iTerm2](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#what-is-iterm2)
* [What is Oh-My-ZSH](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#what-is-oh-my-zsh)
* [The power of team work!](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#the-power-of-team-work)
* [Installation](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#installation)
* [Verify ZSH install and ZSH as default shell](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#verify-zsh-install-and-zsh-as-default-shell)
* [Now What!?](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#now-what)
* [Configuration File](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#configuration-file)
* [Themes](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#themes)
* [Split Panes (iTerm2)](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#split-panes-iterm2)
* [Autocomplete](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#autocomplete)
* [Tab completion for cd](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#tab-completion-for-cd)
* [Shared command history](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#shared-command-history)
* [ZSH fixes case](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#zsh-fixes-case)
* [Find a switch](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#find-a-switch)
* [Instant Replay (iTerm)](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#instant-replay-iterm)
* [Oh-My-ZSH Plugins](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#oh-my-zsh-plugins)
* [Enable multiple plugins](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#enable-multiple-plugins)
* [Spotify (OSX plugin)](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#spotify-osx-plugin)
* [Ansible](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#ansible)
* [Over to you](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/README.md#over-to-you)

<div align="right">
    <b><a href="#top">↥ back to top</a></b>
</div>
<br/>

## What is iTerm2
Terminal in OSX is nice and simple but low on features. iTerm2 is a replacement for the Terminal built into a MAC, and offers many additional features, some of which listed below:

* Lots of keyboard shortcuts, so less time spent touching the mouse.
* Advanced split screens (horizontal/vertical)
* Mouse-less copy
* Advanced command history
* Open iTerm2 from Finder
* Autocomplete list based on your input
* Instant Replay can take you back in time! But probably not to October 21st 1985.

> I'll go into more detail on some of the best features later in the article.

## What is Oh-My-ZSH
Zsh is a UNIX command interpreter (aka a shell, similar to bash).  Oh My Zsh is an open source framework for managing Zsh configuration. It also offers many additional features:

* 250+ plugins that make using your favourite tools such as Ansible, GitHub, Python, Pyenv, easier and faster to use. 
* 140+ cool themes to make your terminal, such as iTerm2, look amazing.  
* You can even start your favourite track in Spotify from the command line. Why?  I dont know, but it was the first thing I did :smile:

> The terms Oh-My-ZSH and zsh will be used synonymously throught this document.

<div align="right">
    <b><a href="#top">↥ back to top</a></b>
</div>
<br/>

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

<div align="right">
    <b><a href="#top">↥ back to top</a></b>
</div>
<br/>

# Verify ZSH install and ZSH as default shell
You probably want zsh as your default shell, so when you open a terminal session zsh will be used by default.  This is set in your environment variables, below are a few ways to check the installer set this for you:

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
> I think you can now be sure zsh is set to your default shell.. very sure..

# Now What!?
You could go in many directions, but lets be honest, we're going to configure a Theme! 

> The list of zsh themes is located [HERE](https://github.com/robbyrussell/oh-my-zsh/wiki/Themes). Have a look through and find one you like.

<div align="right">
    <b><a href="#top">↥ back to top</a></b>
</div>
<br/>

## Configuration File
Your ZSH configuration file is located in your Home Directory `~/.zshrc`. This is where you can change themes, amongst other settings.

## Themes
Below I am in my home folder and I edit the `.zshrc` file using `vi`
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
<div align="right">
    <b><a href="#top">↥ back to top</a></b>
</div>
<br/>

> You can use any text editor to edit the file, but vi is something worth learning, just use a cheatsheet, like [THIS](http://www.lagmonster.org/docs/vi.html) or [THIS](https://www.gosquared.com/resources/vi-cheat-sheet/).

The default theme which is enabled is shown below, all you have to do is change the theme name and restart your terminal session (or open a new tab) to enable the new theme.  You might choose to copy the line and use hash to disable all but one theme, then you can have a list of your favourites in the config file:
```
#ZSH_THEME="robbyrussell"
ZSH_THEME="gianu"
```
![gianu theme](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/gianu_theme.png)

> Notice above that I’m being told in my prompt that the folder I am currently in is a `master` [GitHub](https://github.com/NetDevNotes/Complete-Python-3-Bootcamp.git) repository.  This is the zsh Git plugin providing the additional information.  See the zsh Plugin section below for more info.

If you are not feeling very colourful, maybe its Monday or its raining, you can set ZSH_THEME to be blank: 

`ZSH_THEME=""`

<div align="right">
    <b><a href="#top">↥ back to top</a></b>
</div>
<br/>

## Split Panes (iTerm2)

You to divide a tab into many rectangular panes, each of which is a different terminal session.

### Split Pane Shortcuts 

Shortcut | Function
------------ | -------------
cmd-d | Divide vertically
cmd-shift-d | Divide horizontally
cmd-opt-arrow | Navigate split panes
cmd-[] | Navigate split panes    

![Split Panes](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/split_panes.png)

## Autocomplete
Both iTerm2 and Oh-My-ZSH have command history autocompletion features.

### iTerm2
1. To use autocomplete, type the beginning of a word and then press `cmd-;`
2. Use the `arrow keys` to select the command from within the list
3. Use `enter` to select the command

### ZSH
1. To use autocomplete, type the beginning of a word
2. Use the `arrow keys` to scroll through the command history

<div align="right">
    <b><a href="#top">↥ back to top</a></b>
</div>
<br/>

## Tab completion for cd
In Bash when you press <TAB> you get prompted with a list of files in the current directory. But zsh shows you folders which you can tab through, which in the context of cd is of course more useful.
         
## Shared command history
In Bash each shell has its own history, zsh shares the command history with all active shells.

## ZSH fixes case
If you type a lower case letter instead of an upper, or visa versa, zsh notices and changes the capitalisation.

## Find a switch
Not that kind of switch networkers! 
```
$ ls -l <TAB>
-1  -- single column output
-A  -- list all except . and ..
-B  -- print octal escapes for control characters
-C  -- list entries in columns sorted vertically
-F  -- append file type indicators
-H  -- follow symlinks on the command line
[removed for brevity]
```
Another example:
```
[nico@Nicos-MacBook ~ ]$ git - <TAB>
--bare                    -- use $PWD as repository
--exec-path               -- path containing core git-programs
--git-dir                 -- path to repository
--help                    -- display help message
--html-path               -- display path to HTML documentation and exit
--info-path               -- print the path where the info files are installed and exit
[removed for brevity]
```
<div align="right">
    <b><a href="#top">↥ back to top</a></b>
</div>
<br/>

## Instant Replay (iTerm)
This is a cool feature which will take you back in time!
1. To enable, press cmd-opt-B. 
2. Use left and right arrow keys to navigate back and forward through time. 
3. Use Esc to exit.

> More iTerm2 features are listed [HERE](https://www.iterm2.com/documentation-highlights.html).

## Oh-My-ZSH Plugins
I mentioned there were a lot of plugins for zsh, they extend the features of zsh even further and relate to specific services, applications and OS features.

> The list of Oh-My-ZSH plugins can be found [HERE](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins)

To enable plugins you need to append to a line in your `~/.zshrc` file, scroll down until you find section.  You will see that `git` is already enabled:
```
# Which plugins would you like to load?
# Standard plugins can be found in ~/.oh-my-zsh/plugins/*
# Custom plugins may be added to ~/.oh-my-zsh/custom/plugins/
# Example format: plugins=(rails git textmate ruby lighthouse)
# Add wisely, as too many plugins slow down shell startup.
plugins=(git)
```
This is why my command prompt had `(master)` appended earlier.  It's part of the git plugin that highlights to us when we are in a master git repository:
```
[python]$ cd Complete-Python-3-Bootcamp
[Complete-Python-3-Bootcamp (master ✗)]$
```
The git plugin has many more features detailed in the [documentation](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins)

<div align="right">
    <b><a href="#top">↥ back to top</a></b>
</div>
<br/>

## Enable multiple plugins
To add more plugins, append the plugin name to the below line in your `~/.zshrc` file.  I have enabled secveral below:

`plugins=(git github osx ansible history iterm2 iwhois pip pyenv python sublime)`

## Spotify (OSX plugin)
Play a song via the Spotify API from the command line. As with any plugin, type `spotify --help` to see the help page:

`$ spotify play 'dave matthews band' 'let you down'`

![Play Spotify](https://github.com/NetDevNotes/iTerm2-with-Oh-My-ZSH/blob/master/spotify_plugin.png)

## Ansible 
The [Ansible plugin](https://github.com/robbyrussell/oh-my-zsh/tree/master/plugins/ansible) offers several aliases for common Ansible commands:

Command | Description
------------ | -------------
ansible-version / aver | Show the version on ansible installed in this host
ansible-role-init <role name> / arinit | Creates the Ansible Role as per Ansible Galaxy standard
a | command ansible
aconf | command ansible-config
acon | command ansible-console
ainv | command ansible-inventory
aplaybook | command ansible-playbook
ainv | command ansible-inventory
adoc | command ansible-doc
agal | command ansible-galaxy
apull | command ansible-pull
aval | command ansible-vault

# Over to you
So thats a few things you can do with iTerm2 and Oh-My-ZSH, I'll add a few more tips from time-to-time, but of course the best way to learn is to have a play.  **Enjoy**

<div align="right">
    <b><a href="#top">↥ back to top</a></b>
</div>
<br/>
