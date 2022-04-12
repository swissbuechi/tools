Install node version manager:
`curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash`

<https://github.com/nvm-sh/nvm>

reopen shell and test with: `command -v nvm`

install nodejs + npm: `nvm install --lts`

list remote versions: `nvm ls-remote`

install version: `nvm install 14 --lts`

list local versions: `nvm list`

set default version: `nvm use <version>`

uninstall version: `nvm uninstall <version>`