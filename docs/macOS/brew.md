#  Homebrew

- https://brew.sh

```shell
brew docs
brew doctor
brew tap --repair
brew cleanup
HOMEBREW_NO_INSTALL_CLEANUP

# add the tap to your list of available taps.
brew tap <tap-name>
# install a formula from the tap.
brew install <formula-name>
```

## nvm

```shell
brew install nvm

# remove self installation node
sudo rm -rf /usr/local/{bin/{node,npm,npx},lib/node_modules/npm,lib/node,share/man/*/node.*}

# Add the following to your shell profile e.g. ~/.profile or ~/.zshrc:
export NVM_DIR="$HOME/.nvm"
[ -s "/usr/local/opt/nvm/nvm.sh" ] && \. "/usr/local/opt/nvm/nvm.sh"  # This loads nvm
[ -s "/usr/local/opt/nvm/etc/bash_completion.d/nvm" ] && \. "/usr/local/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion
```
