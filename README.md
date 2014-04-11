script-backups
==============

Scripts de backup que utilizo para sincronizar meu computador com Dropbox e Google Drive



- MAC
SymbolicLinker - http://seiryu.home.comcast.net/~seiryu/symboliclinker.html 



# Setup new Mac with OSX Lion from scratch


## Install xcode 
App store http://itunes.apple.com/us/app/xcode/id448457090?mt=12)
The download/install takes awhile so start it first. When it finishes downloading you will still need to run it to complete installation.

## iTerm2 http://www.iterm2.com/
Really the nicest choice for a terminal on OSX right now, especially with Lion style full screen support.

## Solarized color scheme http://ethanschoonover.com/solarized
I feel there is an advantage in setting all your dev apps to use a consistent color scheme, especially your terminal and text editor/dev environment.


## Homebrew http://mxcl.github.com/homebrew/
    ruby -e "$(curl -fsSL https://raw.github.com/gist/323731)"
Note that Xcode is a pre-req for Homebrew

## Set shell to ZSH and install oh-my-zsh
    brew install wget
    wget --no-check-certificate https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | sh restart iTerm2





## TMUX: Auto start on shell start

```sh

 # If you don't do this, your (graphical) login sessions will hang
 [[ $- != *i* ]] && return
 
 # If we are not yet in a screen session
 if [[ $TERM != screen* ]]; then
   # Start tmux if there is no panicfile and tmux actually exists.
   [ ! -f /tmp/panic -a -x /usr/bin/tmux ] && exec tmux
 fi
 
```
