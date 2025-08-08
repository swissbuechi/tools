# Sleep

## Show

`pmset -g`

## Restore

`sudo pmset restoredefaults`

## Log

`pmset -g stats`

`pmset -g log|grep -e "DarkWake "`

`pmset -g log|grep -e " Sleep  " -e " Wake  " -e " DarkWake "`

`pmset -g log | grep -e "Wake from" -e "DarkWake" -e "due to" | tail -n 100`

`pmset -g log | grep -e "Count" | tail`

## Schedule

`pmset -g sched`

`sudo pmset schedule cancelall`

`sudo pmset repeat cancel`

`Cat /Library/Preferences/SystemConfiguration/com.apple.AutoWake.plist`

`sudo chflags schg /Library/Preferences/SystemConfiguration/com.apple.AutoWake.plist`

## Config

```bash
sudo pmset -a ttyskeepawake 0 tcpkeepalive 0 womp 0 networkoversleep 0 proximitywake 0 ring 0 displaysleep 15 disksleep 15 sleep 15 acwake 0 sms 0 powernap 0 darkwakes 0
```

## Settings

- Disable all sharing in preferences
- Disable Airdrop and continuity
- Disable Notifications when the screen is locked
- [swissbuechi/Airplane-Sleep](https://github.com/swissbuechi/Airplane-Sleep/tree/only-turn-on-wifi-if-no-lan): Disable wifi and bluetooth when closing your MacBook or putting it to sleep! (github.com)

## Troubleshooting

### Hardware issue

- https://discussions.apple.com/thread/253995484?sortBy=rank

## Optional (Not recommended)

- Disable SIP

`sudo launchctl unload -w /System/Library/LaunchDaemons/com.apple.PowerUIAgent.plist`

## Alternative

`sudo pmset -a hibernatemode 25`
