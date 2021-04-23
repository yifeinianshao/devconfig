##### Terminal

```json
["homebrew", "on my zsh"]
```

##### Homebrew

```bash
#!/bin/sh
brew install git
brew install nvm
brew install nginx
brew install yarn --ignore-dependencies

brew cask install iterm2
brew cask install charles
brew cask install the-unarchiver
brew cask install mplayerx
brew cask install google-chrome
brew cask install visual-studio-code
brew cask install switchhosts
brew cask install wechatwebdevtools
brew cask install thunder
brew cask install wechat
brew cask install qq
brew cask install qqmusic
```

##### oh my Zsh

.zshrc 文件配置

```
ZSH_THEME="steeef"
plugins=(
  git
  zsh-autosuggestions
  zsh-syntax-highlighting
)

# vscode
alias vsc='/Applications/Visual\ Studio\ Code.app/Contents/Resources/app/bin/code'

# nvm
export NVM_DIR=~/.nvm
source $(brew --prefix nvm)/nvm.sh

# proxy list
alias proxy='export all_proxy=socks5://127.0.0.1:1086'
alias unproxy='unset all_proxy'
```
