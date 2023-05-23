# Homebrew

First step is to install [Homebrew](https://brew.sh/)

Open the built in terminal and paste the command:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
This will also install the `xcode build tools` which is needed by other developer tools.

After homebrew is installed, run the following commands to add it to the `PATH`:
```
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/[username]/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

# iTerm2

Next, install `iTerm2` using brew in the built in terminal like so:
```
brew install iterm2
```
Once installed, open settings using `cmd + ,`:
1. Appearance -> Theme -> Minimal
2. Profiles -> Default
    - Reuse previous session's directory
    - Keys -> Key Mappings -> Presets -> Natural Text Editing

Docs: [iTerm2 Documentation](https://iterm2.com/documentation.html)

# Git

To install `git` run:
```
brew install git
```

# Shell Prompt
Install the shell prompt of choice as shown in [SHELL-PROMPTS.md](https://github.com/adreaskar/mac-setup/blob/master/pages/SHELL-PROMPTS.md)

# Apps
Install all the listed apps in the [brew-casks.txt](https://github.com/adreaskar/mac-setup/blob/master/brew-casks.txt) file  with the command:
```
xargs brew install < brew-casks.txt
```

# Command Shift
In order to change language input source in a more convenient way, i use `karabiner-elements` to remap keyboard shorcuts. Command + Shift is easy to use especially if you have a Windows background.
1. Go to Settings -> Keyboard -> Keyboard Shortcuts -> Input Sources and set a desired shorcut. I use `Cmd + E`
2. After karabiner-elements has been installed from the list of cask apps, open the terminal and cd to `~/.config/karabiner/assets/`
3. Once there, create a `.json` file that will handle the remapping. Example: [CmdShiftToCmdE.json](https://github.com/adreaskar/mac-setup/blob/master/misc/CmdShifttoCmdE.json)
4. This file creates a rule to map `Cmd + Shift` to `Cmd + E` thus changing input source.
5. After that, open karabiner-elements app and go to: Complex Modifications -> Rules -> Add rule and Enable Languages -> Command + Shift to Command + e.

# 𝗙𝗮𝘀𝘁𝗲𝗿 𝗗𝗼𝗰𝗸 𝗛𝗶𝗱𝗶𝗻𝗴
For me the default dock behaviour is quite slow, so i use this terminal command to change it:
```
defaults write com.apple.dock autohide-delay -float 0; defaults write com.apple.dock autohide-time-modifier -int 1;killall Dock
```
Reset to defaults:
```
defaults write com.apple.dock autohide-delay -float 0.5; defaults write com.apple.dock autohide-time-modifier -int 0.5 ;killall Dock
```

# Dev Setup
Install development tools as shown in [DEV-SETUP.md](https://github.com/adreaskar/mac-setup/blob/master/pages/DEV-SETUP.md)
