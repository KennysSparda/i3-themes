# i3wm Theme Manager


## License
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

## Overview
The i3wm Theme Manager was created to facilitate the management of i3 Window Manager configuration files, both in terms of aesthetics and functionality. With this tool, you can easily change themes, including settings related to other monitors and their sizes.

## Dependencies
The i3wm Theme Manager has the following dependencies:

- **Nitrogen**: A utility that manages desktop wallpapers in Linux, providing an easy way to customize and personalize your desktop background.
- **Zenity**: A tool that creates simple graphical interfaces in Linux command-line scripts, enhancing user interaction.
- **Picom**: An X11 window compositor utility that enhances the visual experience of graphical interfaces with features like transparency, shading, and visual effects.

To install these dependencies on Debian-based systems, run the following command:

```bash
sudo apt-get update && sudo apt-get install i3-gaps nitrogen zenity picom
```

For Arch-based systems, use the following command:

```bash
sudo pacman -Syu i3-gaps nitrogen zenity picom
```

## Installation
To install the i3wm Theme Manager, follow the instructions below:

1. Clone the repository:
```
git clone https://github.com/KennysSparda/i3-theme-manager.git ~/.config/i3-theme-manager
```

2. Save your current i3 configuration, as the i3wm Theme Manager will overwrite the `~/.config/i3/config` file with the corresponding file for the selected theme.

3. Run the program for the first time:
```
~/.config/i3-theme-manager/i3-theme-manager.sh
```

4. Add the following line to your `.bashrc` or `.zshrc` file to allow running the script directly from the terminal:
```
source ~/.config/i3-theme-manager/i3-theme-manager.sh
```

## Usage and Customization
[![Vídeo](https://img.youtube.com/vi/OVR18_QjbZU/0.jpg)](https://youtu.be/OVR18_QjbZU)

### Example: Copying i3 Configuration and Adding an Image
To create a new theme, follow these steps:
1. Copy your current i3 configuration file to the `~/.config/i3-theme-manager/themes/new-theme` directory:
```
cp ~/.config/i3/config ~/.config/i3-theme-manager/themes/new-theme
```

2. Place an image file in the `~/.config/i3-theme-manager/themes/new-theme` directory. This image will be associated with the new theme.

3. In the configuration file that goes by default there is a section that assigns the script to a combination on the keyboard
Add the following line to your `~/.config/i3-theme-manager/themes/new-theme/config` 
```
# start i3-theme-manager
bindsym $mod+t exec bash ~/.config/i3-theme-manager/i3-theme-manager.sh
```

### Contribution
If you would like to contribute to the i3wm Theme Manager, please follow the guidelines below:
- Fork the repository on GitHub.
- Make your desired changes.
- Submit a pull request describing your changes and the rationale behind them.

We welcome contributions from the community and appreciate any feedback or suggestions.

## First-time Execution
After completing the installation, run the i3wm Theme Manager for the first time using the following command:
```
i3-theme-manager.sh
```

Be sure to read the documentation provided with the i3wm Theme Manager for more information on how to use all available features. If you have any questions or suggestions, feel free to contact us.

## Contact
You can reach me through the following channels:

- Portfolio: [kennyvargas.vercel.app](https://kennyvargas.vercel.app)
- GitHub: [github.com/KennysSparda](https://github.com/KennysSparda)
- LinkedIn: [linkedin.com/in/kenny-de-souza-vargas-8a521422a](https://www.linkedin.com/in/kenny-de-souza-vargas-8a521422a)"
