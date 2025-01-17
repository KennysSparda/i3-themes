# i3wm Theme Manager


## License
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

## Overview
The i3wm Theme Manager was created to facilitate the management of i3 Window Manager configuration files, both in terms of aesthetics and functionality. With this tool, you can easily change themes, including settings related to other monitors and their sizes.

## Dependencies
The i3wm Theme Manager has the following dependencies:

- **i3-gaps**: A fork of the i3 window manager with support for adjustable gaps between windows.
- **Nitrogen**: A utility for setting and managing desktop wallpapers, providing an easy way to customize your desktop background.
- **Zenity**: A tool that enables the creation of simple graphical interfaces in command-line scripts, making user interaction more convenient.
- **Picom**: An X11 window compositor utility that enhances the user experience with visual effects, transparency, and shadowing.

### Installation
To install the dependencies on Debian-based systems, run the following command:

```bash
sudo apt-get update && sudo apt-get install i3-gaps nitrogen zenity picom
```

For Arch-based systems, use the following command:

```bash
sudo pacman -Syu i3-gaps nitrogen zenity picom
```

On Fedora, execute the following command:

```bash
sudo dnf install i3-gaps nitrogen zenity picom
```

## Installation
To install the i3wm Theme Manager, follow the instructions below:

1. Clone the repository:
```bash
git clone https://github.com/KennysSparda/i3-theme-manager.git ~/.config/i3-theme-manager
```

2. Save your current i3 configuration, as the i3wm Theme Manager will overwrite the `~/.config/i3/config` file with the corresponding file for the selected theme.

3. Run the program for the first time:
```bash
~/.config/i3-theme-manager/i3-theme-manager.sh
```

4. Add the following line to your `.bashrc` or `.zshrc` file to allow running the script directly from the terminal:
```bash
source ~/.config/i3-theme-manager/i3-theme-manager.sh
```

## Usage and Customization
[![Vídeo](https://img.youtube.com/vi/OVR18_QjbZU/0.jpg)](https://youtu.be/OVR18_QjbZU)

### Example: Creation of new theme
To create a new theme, follow these steps:
1. Create new directory on `~/.config/i3-theme-manager/themes/my-new-theme`
```bash
mkdir -p ~/.config/i3-theme-manager/themes/my-new-theme
```

2. Place an image file with name "image" in the `~/.config/i3-theme-manager/themes/my-new-theme` directory. This image will be associated with the new theme.

3. Add new entry on zenity menu for my-new-theme in `~/.config/i3-theme-manager/i3-theme-manager.sh` file:
```bash
# [...]
menu() {
  options=("red" "blue" "green" "purple" "my-new-theme" "Exit")
  theme=$(zenity --list --height="300" --title="Change theme" --column="Themes" "${options[@]}")

  case $theme in
    red|blue|green|purple|my-new-theme)
# [...]
```

4. In the configuration file `~/.config/i3-theme-manager/apply-color.sh` create new case for your favorite color palette, and add colors in hexadecimal format, like this:
```bash
  my-new-theme)
    primarycolor="#ffff00"
    secundarycolor="#333333"
    tertiarycolor="#000000"
    ;;
```

### Example: Configuration of monitors
To change output and size of video, edit this fil: `~/.config/i3-theme-manager/monitor-sizes.sh`
Change the values according to your preferences.
To know about available videos enter the following command:
```bash
xrandr --listmonitor
```
To know all sizes determined video supports enter this:
```bash
xrandr
```

### Contribution
If you would like to contribute to the i3wm Theme Manager, please follow the guidelines below:
- Fork the repository on GitHub.
- Make your desired changes.
- Submit a pull request describing your changes and the rationale behind them.

We welcome contributions from the community and appreciate any feedback or suggestions.

## First-time Execution
After completing the installation, run the i3wm Theme Manager for the first time using the following command:
```bash
i3-theme-manager.sh
```
Or pressing Win+t

Be sure to read the documentation provided with the i3wm Theme Manager for more information on how to use all available features. If you have any questions or suggestions, feel free to contact us.

## Contact
You can reach me through the following channels:

- Portfolio: [kennyvargas.vercel.app](https://kennyvargas.vercel.app)
- GitHub: [github.com/KennysSparda](https://github.com/KennysSparda)
- LinkedIn: [linkedin.com/in/kenny-de-souza-vargas-8a521422a](https://www.linkedin.com/in/kenny-de-souza-vargas-8a521422a)"
