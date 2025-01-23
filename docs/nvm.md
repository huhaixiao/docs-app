# nvm

- `which nvm`
    - prints out a function
    - because `nvm` is not a standlone executable
    - but rather a shell function
- nodejs version managed by nvm is controlled by shell session
- nvm default version is shared by all shell sessions
```shell
brew install nvm
which nvm
source ~/.nvm/nvm.sh
nvm list
# v14.21.3
nvm install lts/fermium
# v16.20.2
nvm install lts/gallium
# v18.20.4
nvm install lts/hydrogen
# v20.18.0
nvm install lts/iron
nvm ls-remote
nvm use <version>
nvm use default
nvm use latest
nvm use 14.17.0
nvm install 18.12.0
# use this to setup the default version of all shell sessions
nvm alias default 18.12.0
# nvm mirror ~/.zshrc
export NVM_NODEJS_ORG_MIRROR=https://npm.taobao.org/mirrors/node

# macOS m1 chip using nvm to install v14
arch # arm64
arch -x86_64 zsh
arch # i386
nvm install 14
```
