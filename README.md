## Homebrew

First step is to install [Homebrew](https://brew.sh/)

Open the built in terminal and paste the command:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
This will also install the `xcode build tools` which is needed by other developer tools.

## iTerm2

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

## Bash

To install `bash` shell, run:
```
brew install bash
```
To see the location where bash is installed, run the command:
```
which bash
```
If the directory is anything else other than `/bin/bash`, add it to the `/etc/shells` file using the command:
```
sudo nano /etc/shells
```
Now, we can set it as our default shell:
```
chsh -s /bin/bash
```
