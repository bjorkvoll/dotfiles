# Dotfiles Setup for Kitty & Zsh

This guide will set up **Kitty**, **Zsh**, and my custom dotfiles on a fresh system.  

---

## 🚀 Quick Setup

### 1️⃣ Update your system and install Git
```bash
sudo apt update
sudo apt install git
```


## Clone this repository
```bash
git clone https://github.com/bjorkvoll/dotfiles.git
cd dotfiles
```

## Install kitty and zsh
```bash
sudo apt install kitty zsh
```

Set zsh as default shell:
```bash
chsh -s $(which zsh)
```

## Install Oh My Zsh
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Install zsh plugins

**zsh-autosuggestions**
```bash
git clone https://github.com/zsh-users/zsh-autosuggestions \
~/.oh-my-zsh/custom/plugins/zsh-autosuggestions
```

## Copy dotfiles to correct location
```bash
# Copy Zsh config
cp .zshrc ~/.zshrc

# Copy Kitty config
mkdir -p ~/.config/kitty
cp kitty.conf ~/.config/kitty/kitty.conf
```



# Install FiraCode Nerd Font Mono
1. Download the FiraCoda faont from the Nerd Fonts GitHub release: (Scroll down and download .zip) 
   https://github.com/ryanoasis/nerd-fonts/releases

2. Extract the font files and install them in your system's font directory.
   Create the directory if it does not exist on Arch / ubuntu
   For example:
   - On Linux (Arch / Ubuntu): `~/.local/share/fonts/`
   - On macOS: `~/Library/Fonts/`
   - On Windows: Control Panel > Fonts

3. Linux (Arch / ubuntu) Update font cache
```bash
fc-cache -fv
```
