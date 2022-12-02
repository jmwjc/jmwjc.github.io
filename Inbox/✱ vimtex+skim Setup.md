# [vimtex](https://github.com/lervag/vimtex)
- Install [neovim-remote](https://github.com/mhinz/neovim-remote) package:
 ```
pip3 install neovim-remote
 ```
- Open file by `nvr`
# [Skim](https://skim-app.sourceforge.io/)
- Set `Preferences`->`Sync`->`PDF-Tex Sync support`:
    - `Preset`: `Custom`
    - Command: `nvr`
    - Arguments: `--servername /tmp/nvimsocket +"%line" "%file"`

# Usage
- Type `\ll` in nvr to start service
- Type `\lv` in nvr to show the selection in Skim 
- Press `Shift` + `Command` and click the text in Skim to inv-search
