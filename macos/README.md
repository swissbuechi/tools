# Installation

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

## Update

```shell
brew tap homebrew/autoupdate
brew autoupdate start --upgrade --cleanup
```

```shell
brew install --cask forticlient-vpn
open /opt/homebrew/Caskroom/forticlient-vpn/7.0/FortiClientUpdate.app
```

# Utils

## Mouse

`brew install --cask scroll-reverser`

`brew install --cask discretescroll`

## Keyboard

`brew tap homebrew/cask-drivers`

`brew install logitech-g-hub`

## Dock

`defaults write com.apple.dock autohide-delay -float 0; killall Dock`

`defaults write com.apple.dock autohide-time-modifier -float 0.5; killall Dock`

## Battery

`brew install --cask aldente`

## Display

`brew tap jakehilborn/jakehilborn && brew install displayplacer`

## Font

### Smooth fonts on 1080p external displays

```bash
defaults write -g CGFontRenderingFontSmoothingDisabled -bool NO
defaults -currentHost write -globalDomain AppleFontSmoothing -int 2
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

`brew install --cask microsoft-remote-desktop`

`brew install --cask teamviewer`

`brew install --cask tunnelblick`

`brew install wakeonlan`

## Automation

`brew install ansible`

## CLI

`brew install --cask powershell`

## Image

`brew install --cask balenaetcher`
