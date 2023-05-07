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
Install the shell prompt of choice as shown in [SHELL-PROMPTS.md](https://github.com/adreaskar/mac-setup/edit/master/SHELL-PROMPTS.md)

# Casks
Install all the listed apps in the [brew-casks.txt](https://github.com/adreaskar/mac-setup/blob/master/brew-casks.txt) file  with the command:
```
xargs brew install < brew-casks.txt
```

# NVM
To install `nvm` run:
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
```
To find the latest LTS `Node.js` release type the command:
```
nvm ls-remote
```
And then install it with:
```
nvm install [version-number]
```
