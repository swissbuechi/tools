## X11

### Simple

`sudo apt install freerdp2-x11 `

```shell
xfreerdp /multimon +clipboard /u:<username> /p:$(zenity --password --title=Authentication) /fonts /d:<domain> /v:<server-name> +toggle-fullscreen /f /t:<server-name> +decorations /sound:sys:pulse /microphone /cert:ignore /log-level:off /kbd:0x00000807 /wm-class:<server-name>
```

### Advanced

`sudo apt install libsecret-tools`

`nano ~/ts.sh`

```shell
#!/bin/bash

# Server
USERNAME=<username>
SERVER=<server>
DOMAIN=<domain>

# Secret Store
LOGIN=$SERVER			# Unique id for your login
LABEL="Login for $SERVER" 	# Human readable label

ST=/usr/bin/secret-tool

get_password() {
    $ST lookup "$LOGIN" "$USER"
}

password=$( get_password )
if [ "$password" = "" ]; then
    zenity --password --title=Authentication | $ST store --label "$LABEL" "$LOGIN" "$USER"
    password=$( get_password )
fi

if [ "$password" = "" ]; then
    echo "ERROR: Failed to fetch password!"
else
    xfreerdp /monitors:0,1,2 /multimon /smart-sizing +clipboard /u:$USERNAME /p:$password /fonts /d:$DOMAIN /v:$SERVER +toggle-fullscreen /f /t:$SERVER +decorations /sound:sys:pulse /microphone /cert:ignore /log-level:off /kbd:0x00000807 /wm-class:$SERVER
fi

```

`chmod +x ~/ts.sh`

`nano .local/share/applications/ts.desktop`

```shell
[Desktop Entry]
Encoding=UTF-8
Version=1.0
Name=DKTS01
Type=Application
Terminal=false
Exec=~/ts.sh
Icon=/usr/share/icons/Adwaita/512x512/devices/computer.png
```