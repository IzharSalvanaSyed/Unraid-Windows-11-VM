# Unraid-Windows-11-VM
Install Windows 11 Virtual Machine on Unraid.  

I am writing this because I, like many others, forget how to install some Virtual Machines for certain things and need reminders, and this is the best way to do so. 

## Getting Started
1. Download Windows 11 IS0.
   - download the Windows 11 ISO from the [Windows website](https://www.microsoft.com/en-in/software-download/windows11?msockid=2e71b513fae261c01d1ba06cfbbc6035)

2. Upload Windows 11 ISO into your _isos share folder in Unraid.
   1. There are many ways to upload the ISO to the ISOS share folder.
     - If you have Folderview, it will make it easier to navigate to the isos share folder from the browser GUI.
       **OR**
    2. Shares -> Browser /mnt/user/isos -> Upload
    
3. Download the Windows VirtIO driver via Unraid
   - Settings -> VM Manager -> Default Windows VirtIO driver ISO (optional) -> Top Item/Latest
  
## Creating your Windows 11 VM in Unraid
1. VMs -> Add VM -> Windows 11
2. Things to Configure
   - I am using Default Settings, which has a couple of things that I am changing for my needs. I will highlight some areas if you want to configure them for other uses.

   1. **Autostart** - If you want the VM to start Automatically whenever Unraid starts
   2. **Logical CPUs** - Your choice of what to allocate
      - 2 Cores, 4 Threads
    3. **Initial Memory** - Default is 4GB (4096 MB)
       - 8192 MB
    4. **OS Install ISO** - This is where you choose the ISO that you uploaded into your ISOS Share folder
    5. **VirtIO Drivers ISO** - This should most likely already be selected. If not, there should be a drop-down section where you can choose which drivers you want to use.
    6. **Primary vDisk Location** - You choose where you want the VM to be installed.
       - None - If you want to pass through a Bare metal drive to install it or have Windows installed already on it.
       - Auto - Creates a vDisk folder in the Domains Share folder.
       - Other Caches or disks on the array to choose from if you want to install them using those options.
       - Manual - Create your folder location within a cache or Disk array.
    7. **Primary vDisk Size**—The default is 64G, but you can choose whatever size you need if space is available on your install disk. 
    8. **Unraid Share Mode**—This allows you to pass through Unraid Shares into the Windows 11 VM. Choose whichever you want. You can add multiple by clicking on the + icon on the left.
    9. **Graphics Card** - Default is Virtual or if you want to passthrough a GPU.
    10.  **VM Console Protocol**—I used the default VNC; I have never used SPICE, but the option is there if you need to use it.
    11. 
