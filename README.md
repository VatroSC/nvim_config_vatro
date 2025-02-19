# nvim_config_vatro

### this is a messy repo

- [x] nvim, vim löschen 
- [x] vanilla nvim neu instalieren
- [] config, plugins instalieren
- [] den ganzen prozess Dokumentieren

## Removing old nvim setup
```bash
rm -vf /usr/local/bin/nvim
rm -rvf /usr/local/share/nvim
rm -rvf ~/.config/nvim
rm -rfv /usr/local/share/nvim-linux-x86_64/bin/nvim
rm -rfv /root/.local/share/
rm -rfv /root/.local/state/
```

## Installing nvim via git
[releases:](https://github.com/neovim/neovim/releases)
```bash
cd /usr/local/share
wget https://github.com/neovim/neovim/releases/download/v0.10.4/nvim-linux-x86_64.tar.gz
tar xzvf nvim-linux-x86_64.tar.gz
ln -s /usr/local/share/nvim-linux-x86_64/nvim /usr/local/bin/nvim
nvim --version
```
## config
```bash
mkdir -p ~/.config/nvim
touch ~/.config/nvim/init.lua
```
### init.lua config

*"tab" funktion*
```lua
vim.cmd("set expandtab")
vim.cmd("set tabspace=4")
vim.cmd("set softtabstop=4")
vim.cmd("set shiftwidth=4")
```
packet manager
- [manager of choice](https://github.com/folke/lazy.nvim)
color theme
- [theme of choice](https://github.com/catppuccin/nvim?tab=readme-ov-file)
file finding
- [telescope](https://github.com/nvim-telescope/telescope.nvim)
- [fzf](https://github.com/ibhagwan/fzf-lua) may be a better alternative. not shure. me noob
highlit and indent ("")
- [treesitter][https://github.com/nvim-treesitter/nvim-treesitter}
file tree
- [Neo_Tree](https://github.com/nvim-neo-tree/neo-tree.nvim)
nerd fonts (optional)
````bash
cd ~/.local/share/fonts
curl -OL https://github.com/ryanoasis/nerd-fonts/releases/latest/download/JetBrainsMono.tar.xz
tar xf
fc-cache -fv
# Install on Win11 bc Win terminal has to render the Nerd Fonts
```
### nvim config

*File Structure*
```arduino
~/.config/nvim
├── lua 
│   └── plugins
│   │   ├── plugin1.lua
│   │   ├── plugin2.lua
│   │    └── usw.lua
│   └── plugins.lua
└── init.lua
```
hmmm... need help https://lazy.folke.io/usage/structuring
do I want a seperate folder for all keymaps or the the keymaps of a plugin in the plugin's lua file?

```pgsql
This README.md is based on my personal notes and configuration process as documented in my nvim.md file :contentReference[oaicite:0]{index=0}.
```
