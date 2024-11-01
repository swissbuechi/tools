# Installation

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

## Update

```shell
brew tap homebrew/autoupdate
brew autoupdate start --upgrade --cleanup --immediate --sudo --ac-only
```

`nano .zshrc`

```shell
export HOMEBREW_NO_AUTO_UPDATE="1"
export HOMEBREW_CASK_OPTS="--no-quarantine"
```

# Utils

## Mouse

`brew install --cask scroll-reverser`

<s> https://github.com/sbmpost/AutoRaise </s>

`brew install --cask discretescroll`

## Keyboard

`brew install --cask alt-tab`

<s>`brew tap homebrew/cask-drivers` </s>

<s>`brew install logitech-g-hub`</s>

### Fix sapped keys `<` and `§` on CH Layout

`sudo plutil -convert xml1 /Library/Preferences/com.apple.keyboardtype.plist `

`sudo nano /Library/Preferences/com.apple.keyboardtype.plist`

- Change all `type` to `41`

`sudo plutil -convert binary1 /Library/Preferences/com.apple.keyboardtype.plist`

- Reboot

## Dock

`defaults write com.apple.dock autohide-delay -float 0.1; killall Dock`

`defaults write com.apple.dock autohide-time-modifier -float 0.5; killall Dock`

`defaults write com.apple.dock scroll-to-open -bool TRUE; killall Dock`

Restore Defaults

`defaults delete com.apple.dock autohide-delay; killall Dock`

`defaults delete com.apple.dock autohide-time-modifier; killall Dock`

`defaults write com.apple.dock scroll-to-open -bool FALSE; killall Dock`

## Battery

`brew install --cask aldente`

### Enable deep sleep mode

[Sleep](./sleep.md)

 ## Window Management

<s>`brew install --cask rectangle`</s>

Obsolete since macOS 15...

## Font

### Smooth fonts on 1080p external displays

```bash
defaults write -g CGFontRenderingFontSmoothingDisabled -bool NO
defaults -currentHost write -globalDomain AppleFontSmoothing -int 4
```

Restore defaults

```bash
defaults -currentHost delete -globalDomain AppleFontSmoothing
defaults write -g CGFontRenderingFontSmoothingDisabled -bool YES
```


# Entertainment

## PDF

`brew install --cask adobe-acrobat-reader`

## Education

`brew install --cask anki`

`brew install --cask deepl`

## Music

`brew install --cask spotify`

## Collaboration

`brew install --cask microsoft-teams`

`brew install --cask zoom`

## Browser

`brew install --cask firefox`
`brew install --cask microsoft-edge`

## Cloud

`brew install --cask google-drive`

# Security

`brew install --cask bitwarden`

# Development

## General

`brew install --cask postman`

`brew install --cask http-toolkit`

`brew install git`

## NodeJs

[Node JS](../linux/apt/nodejs.md)

## Java

```shell
brew install --cask liberica-jdk17-full
brew tap bell-sw/liberica
```

`brew install maven`

## Docker

`brew install docker`

`brew install docker-compose`

## IDE

`brew install --cask visual-studio-code`

`brew install --cask intellij-idea`

# System Administration

## Remote

`brew install --cask remote-desktop-manager`

`brew install --cask microsoft-remote-desktop`

`brew install --cask teamviewer`

`brew install --cask tunnelblick`

`brew install wakeonlan`

## Automation

`brew install ansible`

`brew install terragrunt`

## CLI

`brew install --cask powershell`

`brew install telnet`

[ZSH](../linux/apt/zsh.md)

## Image

`brew install --cask balenaetcher`
