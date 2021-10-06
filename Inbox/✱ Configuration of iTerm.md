# Oh-my-zsh
## Installation
1. `git clone https://gitee.com/mirrors/oh-my-zsh.git`
2. `sh /oh-my-zsh/tools/install.sh`

## Theme
1. `vi ~/.zshrc`
2. Change the keyword `ZSH_THEME="your-theme"`, where `your-theme` is the theme name you want to choose.
3. `source ~/.zshrc`

### Some good themes
* `amuse`
- `fino`

## Plugin
### [Powerline](https://powerline.readthedocs.io/en/latest/index.html)
Install the fonts for powerline by follow steps:
```
# clone
git clone https://github.com/powerline/fonts.git --depth=1
# install
cd fonts
./install.sh
# clean-up a bit
cd ..
rm -rf fonts
```


# Default open with neovim in iterm2
1. Open Automator and create a new Application
2. Add the "Run Applescript" action
3. Paste this script into the Run Applescript section
```
on run {input, parameters}

	# must use the full path
	set cmd to "/usr/local/bin/nvim "
	set filepaths to ""
	if input is not {} then
		repeat with currentFile in input
			set filepaths to filepaths & quoted form of POSIX path of currentFile & " "
		end repeat
	end if
	tell application "iTerm"
		activate
		tell current window
			create tab with default profile command cmd & filepaths
		end tell
	end tell
	
end run
```