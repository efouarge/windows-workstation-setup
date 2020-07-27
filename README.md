# Windows Workstation Setup for DevOps development
## Summary
This is an very opinionated way to setup your Windows 10 workstation

## Window 10 Requirements

- WSL Installed on your system
- IntelliJ Community Edition or Ultimate installed
- https://hyper.is installed for a terminal

## WSL Setup
First set of commands that you're going to want to run
```bash
sudo apt-get update && apt-get upgrade -y

sudo apt-get install git zsh -y

```
Install oh-my-zsh for productivity

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
Fix WSL to load zsh automatically

```bash
nano ~/.bashrc

if test -t 1; then
exec zsh
fi
```

## Setting up Hyper.is Terminal

- Replace the content from hyper-config.js into File > Edit > Preferences
- Restart Hyper.is application with the new configs

## Setting up IntelliJ 

Install the following plugins (File > Settings > Plugins)
- BashSupport
- HashiCorp Terraform / HCL Language
- Kubernetes
- Native Terminal
- YAML/Ansible Support
- gitignore

Enabling WSL in the IntelliJ default terminal
- File > Settings > Tools > Terminal
- Replace with `wsl.exe`

Restart IntelliJ
