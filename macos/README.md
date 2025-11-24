# macOS default setup

## Package Manager

### Install Homebrew

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

#### Updates

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

### Settings

- Scrolling Axes
  - Reverse Vertical: `true`
  - Reverse horizontal: `false`
- Scrolling Devices
  - Reverse Trackpad: `false`
  - Reverse Mouse: `true`
- Scroll Wheel: Right after Small
- Start at Login: `true`
- Show in menu bar: `false`

`brew install --cask discretescroll`

## Keyboard

`brew install --cask alt-tab`

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

## Enable deep sleep mode

[Sleep](./sleep.md)

## Window Management

`brew install --cask alt-tab`

### alt-tab Settings

- Start at login: `false`
- Menubar icon: `false`
- Shorcut 1:
  - `alt` + `tab`
  - After release: `focus selected windows`
  - Show from: All apps
  - All spaces
  - All screens
  - Show minimized
  - Show hidden
  - Show fullscreen
  - Order by: Recently focused First 
- Shortcut 2:
  - `command` + `tab`
  - Show from: Acrive app
- Apperance:
  - Thumbnails
  - Medium
  - Normal
- Policies:
  - Auto install
- Blacklisr:
  - `com.utmapp.UTM`

#### Recording permission

- Create `altTab.command` in `Applicaions`
  
   ```Command
   screen -dmS AltTab /Applications/AltTab.app/Contents/MacOS/AltTab
   ```

- Add to login items

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

### App Store

- Automatic Updates: `true`

#### Apps

- Greenshot
  - Area screenshot: `F13`
  - Destination: `Editor`
  - Always copy to clipboard: `true`
- Bitwarden

## Terminal

- [ZSH](../linux/apt/zsh.md)

- Profiles:
  - Color: `000000`
  - Font: `SF Mono Regular 11`
  - Keyboard
    - Use Meta as Option key: `false`

## Finder

- General
  - Show items on Desktop: `false`
  - Open folders in tabs: `false`

- Sidebar:
  - Recents
  - AirDrop
  - Application
  - Documents
  - Downloads
  - Home
  - Locations

- Advances:
  - `true`

## System Settings

### Wi-Fi

- Ask to join networks: `false`
- Ask to join hotspots: `true`

## Network

- Firewall: `true`
- DNS:
  - Install Adguard DoH via: https://adguard-dns.io/en/public-dns.html

### General

- Software Update
  - Autoamtic Updates: `true`
- AirDrop & Handoff
  - Allow Handoff: `false`
- AutoFill: `false`
- Sharing: `false`
- Time Machine
  - Backup Frequency: `Manually`
  - Excluded:
    - ~/Downloads
    - ~/Library/CloudStorage
    - ~/Repos
    - ~/Tmp

### Control Centre

- `Don't Show`
- Wi-Fi: `Show`
- Focus: `Show When Active`
- Battery: `Show`
- Music Recognition: `Show in Control Centre`
- Keyboard Brightness: `Show in Control Centre`
- Automatically hide and show the menu bar: `Full Screen Only`
- Recent documents, applications an servers: `None`

### Desktop & Dock

- Dock Size:
  - Size: `25%`
  - Magnification: `33%`
- Minimize using: `Scale Effect`
- Double-click: `Fill`
- Automatically hide and show Dock: `true`
- Show indicators for open applications: `true`
- Shortcuts:
  - None
- Hot Corners:
  - Top-Left: `None`
  - Top-Right: `None`
  - Bottom-Left: `Mission Control`
  - Bottom-Right: `Desktop`

### Display

- HDR: `true`
- Advanced:
  - Link to Mac or iPad: `false`

### Spotlight

- Search results:
  - TBD
- Help Apple Impove Search: `false`

### Focus

- Share accross devices: `false`

### Screen Time

- `false`

### Lock Screen

- Require password: `Immediatley`
- Message: `return to please-return-my-mac@<domain>`

### Privacy & Security

- Analytics & Improvements: `false`

### Game Center

- `false`

### iCloud

- Saved to iCloud:
  - Notes
  - Contacts
  - Calendar
  - Stocks
  - Home
  - Wallet
  - Siri
  - FaceTime
  - Maps
  - Music Recognition
  - Shortcuts

### Keyboard

- 🌐: `Show Emoji`
- Keyboard navigation: `true`
- Shortcuts: 
  - Mission Control:
    - Move a space left: `Command` + `Alt` + `<--`
    - Move a space right: `Command` + `Alt` + `-->`
  - Function Keys: `true`
  - ~~Modifier Keys:~~
    - ~~Apple Internal Keyboard:~~
      - ~~Command Key = `Option`~~
      - ~~Option Key = `Command`~~
- Input Sources:
  - `false`
  - Show inline predictive text: `true`

### Mouse

- Tracking speed: `8 of 10`
- Natural scrolling: `true`
- Secondary click: `Click Right Side`
- Scrolling Speed: `4 of 10`
- Advanced:
  - Pointer acceleration: `true`

### Trackpad

- Point & Click
  - Tracking speed: `5 of 10`
  - Force Click and haptic feedback: `true`
  - Look up: `false`
  - Secondary click: `Click or Tap with Two Fingers`
  - Tap to click: `true`
- Scroll & Zoom
  - `true`
- More Gestures

## Customization

### Control Panel

- ProtonVPN
- ProtonDrive
- Wi-Fi
- Battery
- Greenshot

### Keep in Dock

- Finder
- Settings
- Ungoogled-Chromium
- Edge
- Bitwarden
- VS Code
- Terminal
- Joplin
- TextEdit
- Preview
- Anki
- Skim

## Apps

### Bitwarden

- Install via Store: https://apps.apple.com/ch/app/bitwarden/id1352778147?l=en-GB&mt=12
- Settings
  - Vault Security:
    - Timeout: `On system lock`
    - Unlock with Touch ID: `true`
      - Ask for Touch ID on app start: `true`
  - Preferences:
    - Clear clipboard: `5 Minutes`
  - App Settings:
    - Enable SSH agent: `Always`
- SSH
  - `nano .zshrc`
    - Add: `export SSH_AUTH_SOCK=/Users/raphi/Library/Containers/com.bitwarden.desktop/Data/.bitwarden-ssh-agent.sock`

## Backup Commands

Usefull commands to backup the system or installed application list

### System

`sudo tmutil startbackup`

`caffeinate -s -m -i -t 14400`

### Homebrew

`brew bundle dump`

`mv Brewfile Library/CloudStorage/ProtonDrive*/Backup/`