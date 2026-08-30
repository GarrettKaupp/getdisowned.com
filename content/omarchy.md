---
tags:
  - type/personal/note
  - todostatus/working
status: working
related:
author: me
aliases:
---
# about
I daily drive [omarchy](https://omarchy.org) linux. This is a collection of information I use regularly as I increase my understanding of linux, and computers in general.

>[!attention] 
>Dotfiles currently contain a workaround for the theme switcher, related to issue #7389 / PR #7445. need to get rid of that in the bindings hypr config eventually
# info
## core programs

### shell:fish
I am using fish instead of bash because I hate myself. I dont know why I made this switch, it annoys me every time I think about it.
#### fish alias's
    abbr -a waybarreload 'pkill waybar; hyprctl dispatch exec "waybar"'
    abbr -a weather curl wttr.in/Colorado+Springs
    abbr -a v nvim
    abbr -a cdh cd /home/shortcut/
    abbr -a cdd cd /home/shortcut/dotfiles/
    abbr -a ll ls -laX

### file manager:yazi
I used to use ranger, I am liking yazi a little better. There is a function in my fish config that makes me "cd" into whatever directory I was looking at when I close yazi. Thats pretty sick, could not figure out how to do that with ranger.
### terminal:ghostty
I tried kitty, alacritty, and some others, ghostty is fine.
### editor:neovim
Should do a complete rework of this. Have not spent any time configuring this and I dont know how to use it. Pretty sure I have lazyvim? Not sure what its capable of so I just stick to the basics.
### process manager:btop and nvtop
Self explanatory
### bootloader:limine
Just what comes with omarchy, I have no preference.
### ssh
I never use this but its pretty cool.
1. On/off  
`sudo systemctl (stop/start/enable) sshd`
2. Check current status  
`systemctl (status/is-enabled) sshd`
3. Get IP  
`ip route get 1.2.3.4 | awk '{print $7}'`

## dotfiles
[dotfiles repo ](https://github.com/GarrettKaupp/dotfiles)
#### git cheat sheet
`git add .`  adds untracked files to local branch
`git commit -m "commit message"` commits changes to local branch
`git push` upload local branch to remote  
`git pull` download remote to local branch  
`git diff` show differences between working and staging, or between commits
`git diff HEAD~1 HEAD` to see diffs between current branch and last commit after push

#### stow
Using stow to make symlinks to .config and home directories.
`stow .` in `/home/shortcut/dotfiles` to stow dotfiles. This creates symlinks in `/home/shortcut/` to the current directory, matching the folder hierarchy. 

To track files in the dotfiles repo, I manually move the files to the dotfiles folder and then run stow. Example:
`mv /home/shortcut/.config/walker /home/shortcut/dotfiles/.config`


## other programs

#### cli bs
cbonsai
fastfetch
fzf
tldr
toilet
#### ai
claude-desktop
#### essentials
coolercontrol
#### gaming
discord
gamescope
mangohud-git
osu-lazer
proton-cachyos
protonplus
steam
minecraft-launcher
linuxtrack
#### browsing
firefox
spotify
#### tools
##### editing programs
gimp
kdenlive
libreoffice-fresh
obs-pipewire-audio-capture
obs-studio
obsidian
reaper
##### coding
git
github-cli
starship
neovim
##### system
stow
gparted
unzip
yazi
yay
ventoy-bin
caligula
##### network
haguichi
quamachi
logmein-hamachi
tailscale-git
openvpn
##### periferals
input-remapper-git
openrazer-daemon
razergenie