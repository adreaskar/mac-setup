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

# Oh My Zsh
To install Oh My Zsh run the following command:
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
Docs: [Oh My Zsh documentation](https://github.com/ohmyzsh/ohmyzsh/wiki)

# PowerLevel10K Theme for Oh My Zsh
Run this to install PowerLevel10K:
```
git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
```

# Casks
Install cask apps with this command:
```
xargs brew install < brew-casks.txt
```

# NVM
To install `nvm` run the following command to download and install the script:
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
```
To find the latest LTS `Node.js` release type the command
```
nvm ls-remote
```
And then install it with:
```
nvm install [version-number]
```
