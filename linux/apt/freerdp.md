<https://lzone.de/blog/Using-Linux-keyring-secrets-from-your-scripts>

```shell
xfreerdp /multimon +clipboard /u:<username> /p:$(zenity --password --title=Authentication) /fonts /d:<domain> /v:<server-name> +toggle-fullscreen /f /t:<server-name> +decorations /sound:sys:pulse /microphone /cert:ignore /log-level:off /kbd:0x00000807 /wm-class:<server-name>
```