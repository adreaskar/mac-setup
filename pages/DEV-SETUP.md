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
