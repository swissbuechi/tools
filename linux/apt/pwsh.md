# PowerShell Core with WinRM

## Install
```shell
sudo apt-get update
sudo apt-get install -y wget apt-transport-https software-properties-common gss-ntlmssp
wget -q "https://packages.microsoft.com/config/ubuntu/$(lsb_release -rs)/packages-microsoft-prod.deb"
sudo dpkg -i packages-microsoft-prod.deb
sudo apt-get update
sudo apt-get install -y powershell

sh -c "yes | sudo pwsh -Command 'Install-Module -Name PSWSMan'"
sudo pwsh -Command 'Install-WSMan'
```

## Test
`Enter-PSSession -ComputerName <DC_SERVER> -Authentication Negotiate -Credential <DOMAIN\USER>`