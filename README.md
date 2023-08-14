# Setup Proxmox On Debian 12

# IP Setting:

Step 1 : Get IP With Command `ip` Example : 
```bash
ip -br a
```

![image](https://github.com/RadinPirouz/Proxmox-Setup/assets/75082987/c36de353-0db3-4a64-aa39-c2b5033f3dbb)

Step 2 : Get Your HostName With Command 
```bash
hostname
```

![image](https://github.com/RadinPirouz/Proxmox-Setup/assets/75082987/59b3b1ea-0ac9-4950-8bf3-e71d2c5d6c10)

Step 3 : Add IP And HostName To `/ets/hosts` With Format `[Your IP] [Your Host Name].proxmox.com [Your Host Name]` Example : 
```bash
192.168.2.113 debian.proxmox.com debian
```

![image](https://github.com/RadinPirouz/Proxmox-Setup/assets/75082987/719ce3c8-6695-45aa-8538-50a9da8d124a)

Step 4 : For Final Check Use 
```bash
hostname --ip-address
``` 

![image](https://github.com/RadinPirouz/Proxmox-Setup/assets/75082987/309f2cc0-8136-4283-9781-30b553966cea)

# Add The Proxmox VE Repository

Step 1 : Run This Command To Add Repository To /etc/apt/sources.list.d 
```bash
echo "deb [arch=amd64] http://download.proxmox.com/debian/pve bookworm pve-no-subscription" > /etc/apt/sources.list.d/pve-install-repo.list
``` 

![image](https://github.com/RadinPirouz/Proxmox-Setup/assets/75082987/9adf307b-2318-4664-9c60-f3f5ff6b8a09)

Step 2 : Add Repository Key :
```bash
wget https://enterprise.proxmox.com/debian/proxmox-release-bookworm.gpg -O /etc/apt/trusted.gpg.d/proxmox-release-bookworm.gpg 
sha512sum /etc/apt/trusted.gpg.d/proxmox-release-bookworm.gpg 
7da6fe34168adc6e479327ba517796d4702fa2f8b4f0a9833f5ea6e6b48f6507a6da403a274fe201595edc86a84463d50383d07f64bdde2e3658108db7d6dc87 /etc/apt/trusted.gpg.d/proxmox-release-bookworm.gpg
```

![image](https://github.com/RadinPirouz/Proxmox-Setup/assets/75082987/e74f30a2-6a9b-4500-a3eb-e9e40e918cef)

# Install ProxMox Kernel And Libs

Step 1 : Install Kernel `apt install pve-kernel-5.15` (If You In Iran I Suggest Use VPN :) )

![image](https://github.com/RadinPirouz/Proxmox-Setup/assets/75082987/d8f9ea1c-e96f-4138-937a-0fe9db3332c1)


Step 2 : Install Libs `apt install proxmox-ve postfix open-iscsi` 

![image](https://github.com/RadinPirouz/Proxmox-Setup/assets/75082987/e9882b34-557b-4421-82ef-930be2d3bc71)



Done Your Proxmox Is Ready :)))

```bash
[Your IP]:8006
```

![image](https://github.com/RadinPirouz/Proxmox-Setup/assets/75082987/4476ae0b-4592-4566-91f8-95cb52e07c5d)

