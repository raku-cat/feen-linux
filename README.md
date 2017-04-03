feen-linux
===========
Bash script to provide feen.us screenshot and file upload functionality for linux users.

## Dependencies
 - scrot
 - curl
 - xclip
 - notify-send (notify-osd package)
 - zenity (optional for file selector, without it -f option will be unavailable)
 - jq
## Installation
- Clone/[Download](https://github.com/raku-cat/feen-linux/archive/master.zip) this repository, unzip it then navigate to **feen-linux-master** directory
- Run **feen-install** as root.
- Done, you can remove unpacked files.

First time you will run **feen** command it will ask you for API key, see [feen.me Account Settings](https://feen.us/user) to get yours, if you started the command from outside the terminal (keyboard 
shortcut) you will have to enter your API key manually in *~/.config/feen/feen.conf* file.

## Usage
Set up keyboard shortcuts within linux (in Ubuntu it's *System Settings > Keyboard > Keyboard Shortcuts > Custom Shortcuts*)

| command  | description |
| ------------- | ------------- |
| feen -d  | capture desktop  |
| feen -w  | capture window  |
| feen -a  | capture area  |
| feen -f  | upload file  |

### Nautilus integration
Sample Nautilus script:
```
#!/bin/bash

for arg 
do
	feen "$arg"
done
```
