# Elementary-OS-First-Steps
:baby_bottle: First steps for configuring a fresh installed Elementary OS.

## Contents
  
  1) [update the system](#1-update-the-system)
  
  2) [deb & ppa](#2-deb--ppa)
  
  3) [elementary tweaks](#3-elementary-tweaks)
  
  4) [prevent heating & mem overload](#4-prevent-heating--mem-overload)
  
  5) [libreoffice](#5-libreoffice)
  
  6) [vim, git & zsh](#6-vim-git--zsh)
  
  7) [thefuck, revolver, Sublime Text & Antigen](#7-thefuck-revolver-sublime-text--antigen)
  
  8) [n & nodengine](#8-n--nodengine)
  
  9) [my .zshrc](#9-zshrc)
  
  10) [hyper & yarn](#10-hyper--yarn)
  
  11) [other](#11-other)

## 1) update the system

command: `sudo apt-get update && sudo apt-get upgrade`

[⬆ Back to top](#contents)

## 2) deb & ppa

command: `sudo apt install gdebi && sudo apt-get install software-properties-common`

[⬆ Back to top](#contents)

## 3) elementary tweaks

install: `sudo add-apt-repository ppa:philip.scott/elementary-tweaks && sudo apt-get update && sudo apt-get install elementary-tweaks`

[⬆ Back to top](#contents)

## 4) prevent heating & mem overload

install TLP: `sudo apt install tlp tlp-rdw`

stop samba: `sudo chmod 744 /usr/lib/gvfs/gvfsd-smb-browse`

[⬆ Back to top](#contents)

## 5) libreoffice

install: `sudo apt install libreoffice`

[⬆ Back to top](#contents)

## 6) vim, git & zsh

- vim: `sudo apt-get install vim && sudo update-alternatives --config editor`

- git: `sudo apt-get install git`

- [ZSH](https://github.com/robbyrussell/oh-my-zsh/wiki/Installing-ZSH)

[⬆ Back to top](#contents)

## 7) thefuck, revolver, Sublime Text & Antigen

- [Sublime Text](https://sublimetext.com)

- [The Fuck](https://github.com/nvbn/thefuck)

- [revolver](https://github.com/molovo/revolver)

- [Antigen](https://github.com/zsh-users/antigen)

[⬆ Back to top](#contents)

## 8) n & nodengine

- [n](https://github.com/mklement0/n-install)

- [nodengine](https://github.com/Kikobeats/nodengine)

[⬆ Back to top](#contents)

## 9) my .zshrc

[.zshrc](.zshrc)

[⬆ Back to top](#contents)

## 10) hyper & yarn 

- [hyper](https://github.com/zeit/hyper)

- [hpm-cli](https://www.npmjs.com/package/hpm-cli)

- [my .hyper.js](.hyper.js)

- [yarn](https://yarnpkg.com/docs/install)

[⬆ Back to top](#contents)

## 11) other

- [trash-cli](https://github.com/sindresorhus/trash-cli)

- [gitflow](https://github.com/petervanderdoes/gitflow-avh)

- sushi:

      sudo apt-get update && sudo apt-get install gnome-sushi

- [arc-theme](https://github.com/horst3180/Arc-theme):

      wget http://download.opensuse.org/repositories/home:Horst3180/xUbuntu_15.10/Release.key
      sudo apt-key add - < Release.key 

      sudo sh -c "echo 'deb http://download.opensuse.org/repositories/home:/Horst3180/xUbuntu_15.10/ /' >> /etc/apt/sources.list.d/arc-theme.list"
      sudo apt-get update
      sudo apt-get install arc-theme

- [papirus icons](http://www.noobslab.com/2015/10/papirus-icons-for-unity-papirus-theme.html):

      sudo add-apt-repository ppa:noobslab/icons
      sudo apt-get update
      sudo apt-get install papirus-icons

- Sushi(nemo):

      sudo add-apt-repository ppa:nilarimogard/webupd8
      sudo apt-get update
      sudo apt-get install nemo-gloobus-sushi

- Ranger:

      sudo apt-get install ranger caca-utils highlight atool w3m poppler-utils mediainfo
- htop:

      sudo apt-get install htop

- [indicator-sysmonitor](https://github.com/fossfreedom/indicator-sysmonitor)

- [sensors-indicator](https://launchpad.net/~alexmurray/+archive/ubuntu/indicator-sensors/+sourcepub/4472975/+listing-archive-extra)

- Magic mouse ([askubuntu](http://askubuntu.com/questions/261791/how-to-set-the-scroll-speed-of-apple-magic-mouse)):

  > put this inside `/etc/modprobe.d/magicmouse.conf`:
  > 
  > `options hid_magicmouse scroll-speed=45 scroll-acceleration=1`

- Alternate command & ctrl keys ([StackExchange](http://elementaryos.stackexchange.com/questions/1283/how-to-setup-keyboard-layout-similar-to-os-x)):

  > `gsettings set org.gnome.desktop.input-sources xkb-options "['ctrl:swap_lwin_lctl']"`

- Disable annoying middle mouse click ([AskUbuntu](http://askubuntu.com/questions/4507/how-do-i-disable-middle-mouse-button-click-paste)):

  > Run the following command:
  >
  > `xmodmap -e "pointer = 1 25 3 4 5 6 7 8 9"`
  >
  > To persist this behavior, edit `~/.Xmodmap` and add
  >
  > `pointer = 1 25 3 4 5 6 7 8 9`

- Create native app with npm package [nativefyer](https://www.npmjs.com/package/nativefier)

- Add an app to Applications menu ([StackExchange](http://elementaryos.stackexchange.com/questions/560/how-can-i-add-an-executable-file-to-the-dock)):

  > Create an application desktop-entry at `/usr/share/applications/` with the name `app-name.desktop` with the following basic details:
  > 
  >```
  > [Desktop Entry]
  > Version=1.0
  > Name=App Name
  > Exec=/dir/path/app/binary
  > Terminal=false
  > Icon=/icon/path/icon.png
  > Type=Application
  >```
  
- [Neovim](https://github.com/neovim/neovim/wiki/Installing-Neovim)

- [Better emojis](http://www.omgubuntu.co.uk/2016/08/enable-color-emoji-linux-google-chrome-noto) - fonts.conf file:

	  <fontconfig>

	    <match>
	      <test name="family"><string>sans-serif</string></test>
	      <edit name="family" mode="prepend" binding="weak">
	      <string>Noto Color Emoji</string>
	      </edit>
	    </match>

	    <match>
	      <test name="family"><string>serif</string></test>
	      <edit name="family" mode="prepend" binding="weak">
	      <string>Noto Color Emoji</string>
	      </edit>
	    </match>

	    <match>
	      <test name="family"><string>Apple Color Emoji</string></test>
	      <edit name="family" mode="prepend" binding="weak">
	      <string>Noto Color Emoji</string>
	      </edit>
	    </match>

	  </fontconfig>

[⬆ Back to top](#contents)
