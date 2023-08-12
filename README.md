# Setup Proxmox On Debian 12

# IP Setting:

Step 1 : Get IP With Command `ip` Example : `ip -br a`

![image](https://github.com/RadinPirouz/Proxmox-Setup/assets/75082987/33f3e384-9d1a-4ad0-9ed7-40fb212f6f9c)

Step 2 : Get Your HostName With Command `hostname`

![image](https://github.com/RadinPirouz/Proxmox-Setup/assets/75082987/e8ab960a-99d7-4534-85ca-97da1dfd0a5f)

Step 3 : Add IP And HostName To `/ets/hosts` With Format `[Your IP] [Your Host Name].proxmox.com [Your Host Name]` Example : `192.168.2.113 debian.proxmox.com debian`

![image](https://github.com/RadinPirouz/Proxmox-Setup/assets/75082987/f0960c81-f728-448c-b5cf-5d4104dac112)

Step 4 : For Final Check Use `hostname --ip-address` To Check Is IP Added

![image](https://github.com/RadinPirouz/Proxmox-Setup/assets/75082987/e026ea0b-2180-41a4-bda4-ce3f661c7638)

# Add The Proxmox VE Repository

Step 1 : Run `echo "deb [arch=amd64] http://download.proxmox.com/debian/pve bookworm pve-no-subscription" > /etc/apt/sources.list.d/pve-install-repo.list` To Add Repository To /etc/apt/sources.list.d 

![image](https://github.com/RadinPirouz/Proxmox-Setup/assets/75082987/e19865a0-d5f2-45d8-84a1-e48ca7983073)

Step 2 : Add Repository Key 
`wget https://enterprise.proxmox.com/debian/proxmox-release-bookworm.gpg -O /etc/apt/trusted.gpg.d/proxmox-release-bookworm.gpg 
sha512sum /etc/apt/trusted.gpg.d/proxmox-release-bookworm.gpg 
7da6fe34168adc6e479327ba517796d4702fa2f8b4f0a9833f5ea6e6b48f6507a6da403a274fe201595edc86a84463d50383d07f64bdde2e3658108db7d6dc87 /etc/apt/trusted.gpg.d/proxmox-release-bookworm.gpg`

![image](https://github.com/RadinPirouz/Proxmox-Setup/assets/75082987/4d0eef2c-8ec1-42a1-a9b6-b117a0976417)

# Install ProxMox Kernel And Libs

Step 1 : Install Kernel `apt install pve-kernel-5.15` (If You In Iran I Suggest Use VPN :) )

![image](https://github.com/RadinPirouz/Proxmox-Setup/assets/75082987/3df8c09f-7b2a-4eef-97a3-d1c3bc92954e)

Step 2 : Install Libs `apt install proxmox-ve postfix open-iscsi` 

![image](https://github.com/RadinPirouz/Proxmox-Setup/assets/75082987/205a700d-da1d-4bac-b895-026db7732323)



Done Your Proxmox Is Ready :)))

