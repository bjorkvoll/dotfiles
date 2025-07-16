sudo apt update
sudo apt install git

git clone https://github.com/bjorkvoll/dotfiles.git

sudo apt install kitty zsh
chsh -s $(which zsh)

Install Oh My Zsh
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

# Copy dotfiles to correct location
```bash
cp .zshrc ~/.zshrc
mkdir -p ~/.config/kitty
cp kitty.conf ~/.config/kitty/kitty.conf

```


# Install FiraCode Nerd Font Mono
1. Download the FiraCoda faont from the Nerd Fonts GitHub release: (Scroll down and download .zip) 
   https://github.com/ryanoasis/nerd-fonts/releases

2. Extract the font files and install them in your system's font directory.
   For example:
   - On Arch / Ubuntu: `~/.local/share/fonts/`
   - On macOS: `~/Library/Fonts/`
   - On Windows: Control Panel > Fonts

3. Update font cache
```bash
fc-cache -fv
```
