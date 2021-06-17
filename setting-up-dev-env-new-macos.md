
## Install Homebrew

This step on your mac is essential to other dev dependency installations. It’s worth noting that this installation  _automatically installs_  **XCode**  command line tools. Run this line of code,  [here’s where you can verify if it’s the latest](https://brew.sh/), and you’re set:
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

## Install Git

`brew install git`
Note that you’ll also need an ssh key tied to your github account for secure data transfering. To do this first run
`ssh-keygen`

Then you can view your ssh key by running
`~/.ssh/id_rsa.pub  `
Copy & paste to GitHub profile > settings > SSH & GPG Keys, ‘New SSH Key’. Add to profile

After that, login to Github, click on your profie, open Settings then click “SSH & GPG Keys” on the left. Select ‘New SSH Key” and copy paste this key to that field. You can name the key after your computer type or the name of your machine. Next, configure the Git CLI with:

`git config --global user.email "you@example.com"`
`git config --global user.name "Your Name"`

(Optional)  [**Github Desktop**](https://desktop.github.com/)  is great incase you ever need to undo a push to your project’s branches.

## Encryption & Security Support

`brew install gnupg`

## Download Code Editors

Feel free to install your preferred editor, these are the two I prefer…

### VSCode

-   [Current download link](https://code.visualstudio.com/download)
-   Open it, select “View” > “Command Pallet” and type “Command Pallet: Add code to terminal”. Now you’ll be able to use the  _code_  command in terminal to open directories.
-   Optional: Sync / Import your previous settings (article coming soon)

### Atom

-   [https://atom.io](https://atom.io/)

## Thoughts on Terminal

Your mac comes standard with Zsh as your default command line shell in the Terminal application. If you want to give your terminal a bit of a facelift, you can consider iTerm 2 and Oh-My-Zsh styles. If you’re a bash fanatic, there’s a few steps you can follow below to set it as your default I’ll throw out there just incase as well.

### iTerm2

A super-powered terminal alternative:  [https://iterm2.com](https://iterm2.com/)

### Bash

How to change the default shell to Bash on Mac OS Catilina:  [https://www.howtogeek.com/444596/how-to-change-the-default-shell-to-bash-in-macos-catalina/](https://www.howtogeek.com/444596/how-to-change-the-default-shell-to-bash-in-macos-catalina/)

How to update your version of Bash on a Mac:  [https://itnext.io/upgrading-bash-on-macos-7138bd1066ba](https://itnext.io/upgrading-bash-on-macos-7138bd1066ba)

### Oh-My-Zsh

order to enable a theme, set  `ZSH_THEME`  to the name of the theme in your  `~/.zshrc`, before sourcing Oh My Zsh; for example:  `ZSH_THEME=xiong-chiamiov-plus`is a good one. If you do not want any theme enabled, just set  `ZSH_THEME`  to  `bl`:  `ZSH_THEME="".`  Themes are listed below on GitHub.

[ohmyzsh/ohmyzsh](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes)

## NodeJs

As Node updates more than I update my blog posts, [please be sure to verify the latest install commants here](https://github.com/nvm-sh/nvm#installing-and-updating). These are the latest as of Feb 2021:

	curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash
	# This next command loads nvm into ~/.bash_profile, ~/.zshrc, ~/.profile, or ~/.bashrc 
	export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"  
	[ -s "$NVM_DIR/nvm.sh"] && \. "$NVM_DIR/nvm.sh" 
	nvm install node
	nvm use node
	nvm alias default node
