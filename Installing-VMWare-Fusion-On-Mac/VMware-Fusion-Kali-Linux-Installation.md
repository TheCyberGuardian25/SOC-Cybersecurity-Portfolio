# Step-by-Step Kali Linux Installation in VMware Fusion
## ⬇️ Download the Kali Linux ISO
* Go to the official Kali Linux [website](https://www.kali.org/get-kali/)
* Click the "Installer Images"

<img width="1444" height="900" alt="Screenshot 2025-11-11 at 10 56 10" src="https://github.com/user-attachments/assets/a06d49ba-1e4b-496d-b645-50d3e0a85b0c" />

* Select the "Apple Silicon (ARM 64)" if you are using an M1 or M2 Mac.
* Use the full ISO installer instead of the netinstaller for simplicity.

<img width="1444" height="900" alt="Screenshot 2025-11-11 at 10 58 50" src="https://github.com/user-attachments/assets/c9897ca7-165d-47ee-b17f-8c7cbb881d3a" />


## ➕ Create a New Virtual Machine 


* Open VMware Fusion → File → New → Create a new VM.

  <img width="238" height="181" alt="Screenshot 2025-11-11 at 13 32 16" src="https://github.com/user-attachments/assets/15bc1e8b-bb33-4a07-996a-563894f86b10" />

* Choose Install from disc or image → select the Kali ISO you downloaded.
    
<img width="636" height="527" alt="1" src="https://github.com/user-attachments/assets/f46430d8-01e9-4111-8682-7e92b1d66bbb" />

* Click the Use another disc or disc image...

  <img width="636" height="527" alt="2" src="https://github.com/user-attachments/assets/b631cb31-df99-40d3-8da6-3b8b2bd5e8e5" />

* Select the kali-linux-2025.3-installer-arm64.iso you just downloaded
  
  <img width="636" height="261" alt="3" src="https://github.com/user-attachments/assets/2d5ff404-297a-4d67-9168-91b238245f88" />

* Click continue.

<img width="636" height="525" alt="4" src="https://github.com/user-attachments/assets/882ed3c1-0949-4769-971f-739c1cb1591e" />

* Rename the VM according to your preference.

<img width="753" height="438" alt="5" src="https://github.com/user-attachments/assets/2c05d2ab-26f8-4901-867e-f37f383c96ed" />

* Choose Operating System → Linux → Debian 12.x 64-bit ARM.

<img width="635" height="521" alt="6" src="https://github.com/user-attachments/assets/9fff467a-f23c-440d-8f7b-5894bdb0774a" />


## ⚙️ Allocate VM Resources

#### Do not start the VM yet. Go to Settings to allocate the resources you need.

<img width="635" height="377" alt="Screenshot 2025-11-11 at 11 18 53" src="https://github.com/user-attachments/assets/2cffae17-e270-4e5f-963c-953f1a03d7ca" />

* CPU cores: 2 (safe for multiple VMs; but if you have extra cores, assigning 4 cores can improve performance)
* RAM: 4 GB (4096 MB) (The minimum RAM is 2 GB, but you can increase it depending on your host machine’s available memory)

<img width="635" height="333" alt="Screenshot 2025-11-11 at 11 35 00" src="https://github.com/user-attachments/assets/588e5977-87c9-4c17-b9df-19bd9e3f3824" />

###### Note: Don’t allocate all CPU cores or RAM to VMs; leave resources for your host machine.

* Disk: 25 GB virtual disk minimum (Enter the disk size you want to allocate to your VM)

<img width="635" height="171" alt="Screenshot 2025-11-11 at 11 36 32" src="https://github.com/user-attachments/assets/6b1e2ef9-95b1-46a5-8cd8-2c1eafca25c5" />

* Network: NAT (Choose NAT to reduce the VM’s exposure to external attacks)

<img width="635" height="376" alt="Screenshot 2025-11-11 at 11 38 48" src="https://github.com/user-attachments/assets/642d7d72-d6b0-4a32-89b7-fda7e77dbaa7" />

###### After allocating resources to your VM, start configuring it.

<img width="635" height="616" alt="Screenshot 2025-11-11 at 11 39 00" src="https://github.com/user-attachments/assets/8ce2b1a0-b760-4f45-ab12-a73ba39055c0" />

* Select 'Graphical Install' using the drop-down arrow if you want to use the GUI for configuration. Otherwise, for a terminal-based installation, choose 'Install'. 

<img width="784" height="546" alt="Screenshot 2025-11-11 at 11 39 23" src="https://github.com/user-attachments/assets/60a5a2ce-44c2-43f3-a126-a297ed3e1b26" />

* Choose the language 

* <img width="784" height="546" alt="Screenshot 2025-11-11 at 11 39 58" src="https://github.com/user-attachments/assets/08290ba0-ae9d-45eb-a71c-b1b1b7a8f504" />

* Then choose the country

<img width="1218" height="620" alt="Screenshot 2025-11-11 at 11 40 13" src="https://github.com/user-attachments/assets/56d9a90d-999a-4684-a10d-361e88dcb589" />

* Select the keyboard layout

<img width="1218" height="871" alt="Screenshot 2025-11-11 at 11 40 29" src="https://github.com/user-attachments/assets/62a7942c-82fa-44e5-91de-2f7acc1b94d3" />

* You can skip network setup for offline setup, or connect if you want updates.

<img width="1181" height="256" alt="Screenshot 2025-11-11 at 11 44 34" src="https://github.com/user-attachments/assets/8af0f1ad-faa0-48e9-bb03-3c051fa76b20" />

###### Enter a hostname for your VM. This helps identify the VM in your lab/network.

* Enter your preferred username

<img width="1181" height="269" alt="Screenshot 2025-11-11 at 11 44 59" src="https://github.com/user-attachments/assets/5a39407c-fe25-42e8-865f-6a333d14e04d" />

* Enter your preferred password

<img width="646" height="256" alt="Screenshot 2025-11-11 at 11 46 17" src="https://github.com/user-attachments/assets/bfb101c5-6e45-42d3-bf20-30505cf7045f" />

* Partitioning method: Guided - use entire disk.

<img width="1212" height="324" alt="Screenshot 2025-11-11 at 11 48 54" src="https://github.com/user-attachments/assets/cc25827d-dd44-45b1-a858-e008d1cee6b1" />

* Press "Enter" to proceed.

<img width="1212" height="244" alt="Screenshot 2025-11-11 at 11 49 51" src="https://github.com/user-attachments/assets/0d028045-1b9b-42f7-8fe5-de17220a0d8b" />

<img width="1212" height="496" alt="Screenshot 2025-11-11 at 11 51 10" src="https://github.com/user-attachments/assets/eb669cff-b04a-47ad-bb50-f629356a5791" />

* Click Yes to write changes to disk.

<img width="1181" height="355" alt="Screenshot 2025-11-11 at 11 51 59" src="https://github.com/user-attachments/assets/397b894a-7a5d-416b-a7a3-7e56020831bd" />

* Wait for the installation to finish.

<img width="1181" height="355" alt="Screenshot 2025-11-11 at 11 52 04" src="https://github.com/user-attachments/assets/ada45203-5afc-4363-84b6-98da38935837" />

* Click 'Finish' to complete the installation.

<img width="1202" height="214" alt="Screenshot 2025-11-11 at 12 07 27" src="https://github.com/user-attachments/assets/3aa9a6d0-b7bc-4c28-a972-c8d1a7c5e8cf" />

* Enter the username and password you created.

<img width="1202" height="617" alt="Screenshot 2025-11-11 at 12 08 06" src="https://github.com/user-attachments/assets/b46891bc-3f2b-44e7-b235-7eb85a38f3c6" />

#### Done! ✅ Kali Linux VM has been successfully installed on VMware Fusion.

<img width="1509" height="778" alt="Screenshot 2025-11-11 at 12 08 48" src="https://github.com/user-attachments/assets/b99c077e-1ad2-4c1f-a023-b894494ccd40" />
