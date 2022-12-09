# Setup

## Install Chocolatey

<https://chocolatey.org/install>

## Auto updates for packages

### At Startup

`choco install choco-upgrade-all-at-startup -y`

### Daily

`choco install choco-upgrade-all-at --params "'/DAILY:yes /TIME:12:00 /ABORTTIME:02:00'" -y`

### Weekly

`choco install choco-upgrade-all-at --params "'/WEEKLY:yes /DAY:SUN /TIME:01:00'" -y`

# System Engineering

### Utils

```powershell
choco install rufus -y 
choco install etcher -y
choco install partitionwizard -y
```

### File

```poweshell
choco install filezilla -y
choco install winscp -y
```

### Network

```powershell
choco install nmap -y
choco install advanced-ipscanner -y
choco install angryip -y
choco install putty -y
choco install wireshark -y
choco install fiddler -y
```

### Remote Access

```powershell
choco install royalts-v6 -y
choco install rdm -y
choco install teamviewer -y
choco install microsoft-windows-terminal -y
choco install termius -y
choco install bitvise-ssh-client -y
choco install openvpn -y
```

### Powershell

```powershell
choco install azure-cli -y
choco install powershell-core -y
choco install az.powershell -y
```

### Backup

```powershell
choco install veeam-agent -y
```

### Monitoring

```powershell
choco install zabbix-agent -y
```

# Development

### IDEs

```powershell
choco install intellijidea-ultimate -y
choco install phpstorm -y
choco install postman -y
choco install vscode -y
choco install notepadplusplus -y
choco install atom -y
choco install vim -y
```

### Tools

```powershell
choco install openssl -y
choco install git -y
```

### Docker

```powershell
choco install docker-desktop -y
choco install docker-compose -y
choco install docker-cli -y
```

### Java

```powershell
choco install maven -y
choco install liberica11jdk -y
choco install liberica11jdkfull -y
choco install liberica11jre -y
choco install liberica11jrefull -y
```

### Python 3
```powershell
choco install python -y
```

### SQL

```powershell
choco install heidisql -y
choco install mysql.workbench -y
```

# Productivity

### Browser

```powershell
choco install microsoft-edge -y
choco install googlechrome -y
choco install firefox -y
```

### Tools

```powershell
choco install snagit -y
```

### Password

```powershell
choco install keepass -y
choco install keepass-plugin-keeotp2 -y
choco install keepass-plugin-keetheme -y
choco install bitwarden-cli -ia "/allusers " -y
choco install bitwarden -ia "/allusers " -y
````

### Collaboration

```powershell
choco install microsoft-teams.install -y #machine wide
choco install microsoft-teams -y
choco install discord -y
choco install slack -y
```

### Cloud

```powershell
choco install onedrive -y
choco install google-drive-file-stream -y
```

### Office

```powershell
choco install office365business -y
choco install onenote -y
```

### PDF

```powershell
choco install adobereader -y
```

### Diagram

```powershell
choco install drawio -y
```

### Music

```powershell
choco install spotify -y
choco install mp3tag -y
```
