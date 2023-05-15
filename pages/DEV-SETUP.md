# NVM
To install `nvm` run:
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
```
To find the latest LTS `Node.js` release, type the command:
```
nvm ls-remote
```
And then install it with:
```
nvm install [version-number]
```

# Python
To install the latest `python` version run:
```
brew install python
```
Then install `virtualenv` using the command:
```
pip3 install virtualenv
```
Now inside a project directory run the following to instanciate and activate a venv:
```
python3 -m virtualenv venv
source venv/bin/activate
```

# Jekyll Project
To install a newer version of Ruby (other than 2.6 that macOS has by default), run the command:
```
brew install rbenv ruby-build
```
Add this to ~/.zshrc if you are using zsh:
```
eval "$(rbenv init - zsh)"
```
Also add this to ~/.zprofile:
```
export PATH="$HOME/.rbenv/bin:$PATH"
eval "$(rbenv init - zsh)"
```
Now that rbenv is installed, cd to Jekyll project directory and update Ruby version:
```
rbenv install 3.1.3
rbenv local 3.1.3
```
Install the two essential gems:
```
gem install bundler jekyll
```
Set bundle to use a local folder inside your website:
```
bundle config set --local path 'vendor/bundle'
```
Install the rest of gems:
```
bundle install
bundle add webrick
```
Finally, run the application:
```
bundle exec jekyll serve --watch
```
