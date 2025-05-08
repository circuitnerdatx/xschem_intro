# xschem_intro
getting started guide for xschem

## Introduction to SKY130 Workflow
The current version of Open PDK for Skywater 130nm technology support the following tools:
irsim, klayout, magic, netgen, openlane, qflow, xcircuit, xschem

## Instructions to Download Docker preloaded with Sky130 tools
[UNIC-CASS Homepage](https://kwantaekim.github.io/2024/05/25/OSE-Docker/#docker-1)
1.  Install WSL2 and Ubuntu 22.04 to Windows 11. <br />
check version in powershell.  Type wsl -l -v
3.  Update Linux distro <br />
sudo apt-get update -q && sudo apt-get upgrade -q -y
4.  Install MobaXterm to get benefit of X11 forwarding.  This approach enables multiple screens.  Mobaterm must ALWAYS be active before opening Docker session.
5.  Install VS Code.<br />
a. Install Docker and GIT extensions<br />
b. Ctrl + ' opens terminal in VSCode.<br />
c. Clone [iic-oisc-tools](https://github.com/iic-jku/iic-osic-tools) repo <br />
d. Change access.<br />
		sudo chmod 666 /var/run/docker.sock<br />
7.  Modify repo scripts to enable X11<br />
	a.  in start_vnc.sh, ${PARAMS} -e DISPLAY=host.docker.internal:0 **to** PARAMS<br />
	b.  assign working directory, DESIGNS= /mnt/c/Users/{your username}/Documents/open-source<br />
8.  Run ./start_vnc.sh from WSL powershell.<br />
	a.  Future session can be opened with Docker Desktop.<br />

## Getting Started Demos
[RC Circuit Simulation using Xschem](https://www.youtube.com/watch?v=qbf9CbWoX4w)

## Misc
# Unable to move VSCode window
   Create ~/.config/Code/User/settings.json
   Add single line: { "window.titleBarStyle": "native" }
   Type 'code' to launch
