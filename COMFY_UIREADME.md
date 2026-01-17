Step #1: Installing WSL and Ubuntu
The following steps will show how to install ROCm on WSL with Ubuntu 24.04. Begin by opening Windows PowerShell or Command Prompt in administrator mode, and type the following:

wsl --install -d
Ubuntu-24.04



Step #2: Install AMD Unified Driver Package Repositories and Installer Script
Once you have Ubuntu installed, input the following commands one line at a time to install the installer script for Ubuntu 24.04 (see figure 3, below).

sudo apt update
sudo wget https://repo.radeon.com/amdgpu-install/6.4.2.1/ubuntu/noble/amdgpu-install_6.4.60402-1_all.deb
sudo apt install ./amdgpu-install_6.4.60402-1_all.deb
