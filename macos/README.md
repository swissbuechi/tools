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

### Enable deep sleep mode

[Sleep](./sleep.md)

 ## Window Management

<s>`brew install --cask rectangle`</s>

Obsolete since macOS 15...

<!-- ## Font

### Smooth fonts on 1080p external displays

```bash
defaults write -g CGFontRenderingFontSmoothingDisabled -bool NO
defaults -currentHost write -globalDomain AppleFontSmoothing -int 4
```

Restore defaults

```bash
defaults -currentHost delete -globalDomain AppleFontSmoothing
defaults write -g CGFontRenderingFontSmoothingDisabled -bool YES
``` -->

## CLI

[ZSH](../linux/apt/zsh.md)
