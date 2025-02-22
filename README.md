# i3 and Zsh Configuration

I have a habit of **removing everything and reinstalling everything** frequently. This README is to help me **restore my setup quickly** every time I reset my system.

## **1️⃣ Installation Steps**
Run the following command to install all necessary packages:
```bash
sudo pacman -S acpi alacritty astyle base base-devel btrfs-progs chafa clang cmake discord fastfetch firefox \
fuse2 gdb git github-cli grub gst-plugin-pipewire helix htop i3-wm i3blocks i3lock i3status intel-ucode iwd \
libpulse lightdm lightdm-gtk-greeter linux linux-firmware linux-lts lldb minesweeper-cli-git network-manager-applet \
networkmanager ninja nitrogen picom pipewire pipewire-alsa pipewire-jack pipewire-pulse scrot ttf-jetbrains-mono-nerd \
unzip vim wireplumber xmake yay yay-debug zram-generator
```

### **Step 2: Enable Essential Services**
```bash
sudo systemctl enable lightdm
sudo systemctl enable NetworkManager
```

## **3️⃣ Configuring i3 and Zsh**

### **i3 Setup**
1. **Install i3 Window Manager** (already included in the package list above)
2. **Copy i3 config files:**
   ```bash
   mkdir -p ~/.config/i3
   cp -r /path/to/saved/i3/config ~/.config/i3/
   ```
3. **Set up Nitrogen for Wallpapers:**
   ```bash
   nitrogen --restore &
   ```
4. **Enable Picom for Transparency & Effects:**
   ```bash
   picom --config ~/.config/picom.conf &
   ```

### **Zsh & Oh My Zsh Setup**
1. **Set Zsh as the default shell:**
   ```bash
   chsh -s $(which zsh)
   ```
2. **Install Oh My Zsh:**
   ```bash
   sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
   ```
3. **Use Powerlevel10k for a cool prompt:**
   ```bash
   git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
   ```
4. **Set `ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc`**

### **Git & Yay Setup**
1. **Set up Git (Optional):**
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "you@example.com"
   ```
2. **Enable Paru/Yay for AUR Packages:**
   ```bash
   yay -Syu
   ```

## **Done! 🎉**
Now, I can rest in peace **i3 + Zsh setup!** 🚀

