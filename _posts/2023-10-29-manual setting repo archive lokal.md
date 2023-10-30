nemu di forum katanya kalo pake repo lokal keuntunganNya mempercepat download dari perintah apt.
ini cara manual setting, agak ribet, tapi lebih rinci.

>Adapun repository sendiri adalah kumpulan software-software yang dibuat khusus untuk suatu distribusi (distro Linux)

saya memakai archive package dari domainesia

<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/repolokal.png" />

edit file source.list, kalau di distro ubuntu berada di dir "/etc/apt/"

```
tama@tamagochi:/etc/apt$ sudo nano sources.list
```



lakukan update

```
tama@tamagochi:/etc/apt$ sudo apt update
```

```
tama@tamagochi:/etc/apt$ sudo apt update
Get:1 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy InRelease [270 kB]
Get:2 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates InRelease [119 kB]
Get:3 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security InRelease [110 kB]
Get:4 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports InRelease [109 kB]
Get:5 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed InRelease [270 kB]
Hit:6 https://repo.radeon.com/amdgpu/23.20/amdgpu/ubuntu jammy InRelease
Get:7 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/main Sources [1.340 kB]
Hit:8 https://repo.radeon.com/amdgpu/23.20/rocm/apt/5.7 jammy InRelease
Get:9 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/main amd64 Packages [1.395 kB]
Get:10 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/main i386 Packages [1.040 kB]
Get:11 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/main Translation-en [510 kB]
Get:12 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/main amd64 DEP-11 Metadata [423 kB]
Get:13 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/main DEP-11 48x48 Icons [100,0 kB]
Get:14 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/main DEP-11 64x64 Icons [148 kB]
Get:15 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/main DEP-11 64x64@2 Icons [15,8 kB]
Get:16 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/main amd64 c-n-f Metadata [30,3 kB]
Get:17 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/restricted i386 Packages [30,4 kB]
Get:18 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/restricted amd64 Packages [129 kB]
Get:19 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/restricted Translation-en [18,6 kB]
Get:20 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/restricted amd64 c-n-f Metadata [488 B]
Get:21 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/universe amd64 Packages [14,1 MB]
Get:22 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/universe i386 Packages [7.474 kB]                          
Get:23 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/universe Translation-en [5.652 kB]                         
Get:24 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/universe amd64 DEP-11 Metadata [3.559 kB]                  
Get:25 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/universe DEP-11 48x48 Icons [3.447 kB]                     
Get:26 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/universe DEP-11 64x64 Icons [7.609 kB]                     
Get:27 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/universe DEP-11 64x64@2 Icons [69,3 kB]                    
Get:28 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/universe amd64 c-n-f Metadata [286 kB]                     
Get:29 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/multiverse i386 Packages [112 kB]                          
Get:30 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/multiverse amd64 Packages [217 kB]                         
Get:31 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/multiverse Translation-en [112 kB]                         
Get:32 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/multiverse amd64 DEP-11 Metadata [42,1 kB]                 
Get:33 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/multiverse DEP-11 48x48 Icons [42,7 kB]                    
Get:34 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/multiverse DEP-11 64x64 Icons [193 kB]                     
Get:35 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/multiverse DEP-11 64x64@2 Icons [214 B]                    
Get:36 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy/multiverse amd64 c-n-f Metadata [8.372 B]                  
Get:37 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/main i386 Packages [516 kB]                        
Get:38 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/main amd64 Packages [1.104 kB]                     
Get:39 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/main Translation-en [240 kB]                       
Get:40 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/main amd64 DEP-11 Metadata [101 kB]                
Get:41 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/main DEP-11 48x48 Icons [36,1 kB]                  
Get:42 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/main DEP-11 64x64 Icons [55,1 kB]                  
Get:43 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/main DEP-11 64x64@2 Icons [29 B]                   
Get:44 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/main amd64 c-n-f Metadata [16,1 kB]                
Get:45 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/restricted i386 Packages [32,4 kB]                 
Get:46 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/restricted amd64 Packages [1.036 kB]               
Get:47 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/restricted Translation-en [167 kB]                 
Get:48 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/restricted amd64 c-n-f Metadata [536 B]            
Get:49 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/universe amd64 Packages [995 kB]                   
Get:50 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/universe i386 Packages [660 kB]                    
Get:51 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/universe Translation-en [218 kB]                   
Get:52 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/universe amd64 DEP-11 Metadata [305 kB]            
Get:53 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/universe DEP-11 48x48 Icons [205 kB]               
Get:54 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/universe DEP-11 64x64 Icons [311 kB]               
Get:55 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/universe DEP-11 64x64@2 Icons [29 B]               
Get:56 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/universe amd64 c-n-f Metadata [22,0 kB]            
Get:57 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/multiverse amd64 Packages [41,6 kB]                
Get:58 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/multiverse i386 Packages [3.888 B]                 
Get:59 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/multiverse Translation-en [9.768 B]                
Get:60 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/multiverse amd64 DEP-11 Metadata [940 B]           
Get:61 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/multiverse DEP-11 48x48 Icons [1.867 B]            
Get:62 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/multiverse DEP-11 64x64 Icons [2.497 B]            
Get:63 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/multiverse DEP-11 64x64@2 Icons [29 B]             
Get:64 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-updates/multiverse amd64 c-n-f Metadata [472 B]            
Get:65 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/main i386 Packages [353 kB]                       
Get:66 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/main amd64 Packages [896 kB]                      
Get:67 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/main Translation-en [180 kB]                      
Get:68 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/main amd64 DEP-11 Metadata [43,0 kB]              
Get:69 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/main DEP-11 48x48 Icons [16,9 kB]                 
Get:70 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/main DEP-11 64x64 Icons [26,5 kB]                 
Get:71 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/main DEP-11 64x64@2 Icons [29 B]                  
Get:72 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/main amd64 c-n-f Metadata [11,4 kB]               
Get:73 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/restricted amd64 Packages [1.016 kB]              
Get:74 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/restricted i386 Packages [32,0 kB]                
Get:75 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/restricted Translation-en [164 kB]                
Get:76 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/restricted amd64 c-n-f Metadata [536 B]           
Get:77 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/universe amd64 Packages [793 kB]                  
Get:78 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/universe i386 Packages [562 kB]                   
Get:79 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/universe Translation-en [145 kB]                  
Get:80 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/universe amd64 DEP-11 Metadata [55,0 kB]          
Get:81 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/universe DEP-11 48x48 Icons [22,0 kB]             
Get:82 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/universe DEP-11 64x64 Icons [34,6 kB]             
Get:83 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/universe DEP-11 64x64@2 Icons [29 B]              
Get:84 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/universe amd64 c-n-f Metadata [16,7 kB]           
Get:85 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/multiverse i386 Packages [1.032 B]                
Get:86 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/multiverse amd64 Packages [36,5 kB]               
Get:87 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/multiverse Translation-en [7.060 B]               
Get:88 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-security/multiverse amd64 c-n-f Metadata [260 B]           
Get:89 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports/main i386 Packages [56,3 kB]                     
Get:90 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports/main amd64 Packages [64,2 kB]                    
Get:91 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports/main Translation-en [10,5 kB]                    
Get:92 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports/main amd64 DEP-11 Metadata [4.920 B]             
Get:93 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports/main DEP-11 48x48 Icons [16,1 kB]                
Get:94 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports/main DEP-11 64x64 Icons [21,3 kB]                
Get:95 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports/main DEP-11 64x64@2 Icons [29 B]                 
Get:96 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports/main amd64 c-n-f Metadata [388 B]                
Get:97 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports/restricted amd64 c-n-f Metadata [116 B]          
Get:98 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports/universe amd64 Packages [27,8 kB]                
Get:99 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports/universe i386 Packages [16,9 kB]                 
Get:100 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports/universe Translation-en [16,4 kB]               
Get:101 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports/universe amd64 DEP-11 Metadata [17,9 kB]        
Get:102 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports/universe DEP-11 48x48 Icons [15,7 kB]           
Get:103 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports/universe DEP-11 64x64 Icons [25,6 kB]           
Get:104 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports/universe DEP-11 64x64@2 Icons [29 B]            
Get:105 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports/universe amd64 c-n-f Metadata [644 B]           
Get:106 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-backports/multiverse amd64 c-n-f Metadata [116 B]         
Get:107 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/main amd64 Packages [213 kB]                     
Get:108 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/main i386 Packages [53,9 kB]                     
Get:109 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/main Translation-en [46,2 kB]                    
Get:110 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/main amd64 DEP-11 Metadata [11,5 kB]             
Get:111 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/main DEP-11 48x48 Icons [7.911 B]                
Get:112 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/main DEP-11 64x64 Icons [12,3 kB]                
Get:113 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/main DEP-11 64x64@2 Icons [29 B]                 
Get:114 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/main amd64 c-n-f Metadata [2.768 B]              
Get:115 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/restricted amd64 Packages [296 kB]               
Get:116 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/restricted i386 Packages [1.332 B]               
Get:117 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/restricted Translation-en [48,8 kB]              
Get:118 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/restricted amd64 c-n-f Metadata [116 B]          
Get:119 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/universe i386 Packages [30,8 kB]                 
Get:120 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/universe amd64 Packages [60,9 kB]                
Get:121 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/universe Translation-en [27,3 kB]                
Get:122 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/universe amd64 DEP-11 Metadata [1.448 B]         
Get:123 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/universe DEP-11 48x48 Icons [4.982 B]            
Get:124 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/universe DEP-11 64x64 Icons [8.742 B]            
Get:125 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/universe DEP-11 64x64@2 Icons [29 B]             
Get:126 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/universe amd64 c-n-f Metadata [1.448 B]          
Get:127 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/multiverse amd64 Packages [23,4 kB]              
Get:128 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/multiverse i386 Packages [7.776 B]               
Get:129 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/multiverse Translation-en [7.968 B]              
Get:130 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/multiverse amd64 DEP-11 Metadata [212 B]         
Get:131 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/multiverse DEP-11 48x48 Icons [29 B]             
Get:132 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/multiverse DEP-11 64x64 Icons [29 B]             
Get:133 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/multiverse DEP-11 64x64@2 Icons [29 B]           
Get:134 https://linux.domainesia.com/ubuntu/ubuntu-archive jammy-proposed/multiverse amd64 c-n-f Metadata [116 B]          
Fetched 60,6 MB in 27s (2.263 kB/s)                                                                                        
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
56 packages can be upgraded. Run 'apt list --upgradable' to see them.
```




upgrade

```
tama@tamagochi:/etc/apt$ apt list --upgradeable
Listing... Done
apparmor/jammy-proposed 3.0.4-2ubuntu2.3 amd64 [upgradable from: 3.0.4-2ubuntu2.2]
apt-utils/jammy-proposed 2.4.11 amd64 [upgradable from: 2.4.10]
apt/jammy-proposed 2.4.11 amd64 [upgradable from: 2.4.10]
bsdextrautils/jammy-proposed 2.37.2-4ubuntu3.1 amd64 [upgradable from: 2.37.2-4ubuntu3]
bsdutils/jammy-proposed 1:2.37.2-4ubuntu3.1 amd64 [upgradable from: 1:2.37.2-4ubuntu3]
eject/jammy-proposed 2.37.2-4ubuntu3.1 amd64 [upgradable from: 2.37.2-4ubuntu3]
fdisk/jammy-proposed 2.37.2-4ubuntu3.1 amd64 [upgradable from: 2.37.2-4ubuntu3]
firmware-sof-signed/jammy-proposed,jammy-proposed 2.0-1ubuntu4.2 all [upgradable from: 2.0-1ubuntu4.1]
gjs/jammy-updates 1.72.4-0ubuntu0.22.04.1 amd64 [upgradable from: 1.72.0-1]
gnome-remote-desktop/jammy-proposed 42.9-0ubuntu0.22.04.2 amd64 [upgradable from: 42.9-0ubuntu0.22.04.1]
libapparmor1/jammy-proposed 3.0.4-2ubuntu2.3 amd64 [upgradable from: 3.0.4-2ubuntu2.2]
libapparmor1/jammy-proposed 3.0.4-2ubuntu2.3 i386 [upgradable from: 3.0.4-2ubuntu2.2]
libapt-pkg6.0/jammy-proposed 2.4.11 amd64 [upgradable from: 2.4.10]
libblkid1/jammy-proposed 2.37.2-4ubuntu3.1 amd64 [upgradable from: 2.37.2-4ubuntu3]
libblkid1/jammy-proposed 2.37.2-4ubuntu3.1 i386 [upgradable from: 2.37.2-4ubuntu3]
libcryptsetup12/jammy-proposed 2:2.4.3-1ubuntu1.2 amd64 [upgradable from: 2:2.4.3-1ubuntu1.1]
libfdisk1/jammy-proposed 2.37.2-4ubuntu3.1 amd64 [upgradable from: 2.37.2-4ubuntu3]
libgjs0g/jammy-updates 1.72.4-0ubuntu0.22.04.1 amd64 [upgradable from: 1.72.0-1]
libgpgme11/jammy-proposed 1.16.0-1.2ubuntu4.2 amd64 [upgradable from: 1.16.0-1.2ubuntu4.1]
libgpgmepp6/jammy-proposed 1.16.0-1.2ubuntu4.2 amd64 [upgradable from: 1.16.0-1.2ubuntu4.1]
libicu70/jammy-proposed 70.1-2ubuntu1 amd64 [upgradable from: 70.1-2]
libicu70/jammy-proposed 70.1-2ubuntu1 i386 [upgradable from: 70.1-2]
libmount1/jammy-proposed 2.37.2-4ubuntu3.1 amd64 [upgradable from: 2.37.2-4ubuntu3]
libmount1/jammy-proposed 2.37.2-4ubuntu3.1 i386 [upgradable from: 2.37.2-4ubuntu3]
libsmartcols1/jammy-proposed 2.37.2-4ubuntu3.1 amd64 [upgradable from: 2.37.2-4ubuntu3]
libuuid1/jammy-proposed 2.37.2-4ubuntu3.1 amd64 [upgradable from: 2.37.2-4ubuntu3]
libuuid1/jammy-proposed 2.37.2-4ubuntu3.1 i386 [upgradable from: 2.37.2-4ubuntu3]
libxmlb2/jammy-proposed 0.3.6-2ubuntu0.1 amd64 [upgradable from: 0.3.6-2build1]
linux-firmware/jammy-proposed,jammy-proposed 20220329.git681281e4-0ubuntu3.22 all [upgradable from: 20220329.git681281e4-0ubuntu3.21]
linux-generic-hwe-22.04/jammy-proposed 6.2.0.36.37~22.04.14 amd64 [upgradable from: 6.2.0.35.35~22.04.13]
linux-headers-generic-hwe-22.04/jammy-proposed 6.2.0.36.37~22.04.14 amd64 [upgradable from: 6.2.0.35.35~22.04.13]
linux-image-generic-hwe-22.04/jammy-proposed 6.2.0.36.37~22.04.14 amd64 [upgradable from: 6.2.0.35.35~22.04.13]
linux-libc-dev/jammy-proposed 5.15.0-88.98 amd64 [upgradable from: 5.15.0-87.97]
mount/jammy-proposed 2.37.2-4ubuntu3.1 amd64 [upgradable from: 2.37.2-4ubuntu3]
openvpn/jammy-proposed 2.5.8-0ubuntu0.22.04.1 amd64 [upgradable from: 2.5.5-1ubuntu3.1]
python3-cupshelpers/jammy-proposed,jammy-proposed 1.5.16-0ubuntu3.1 all [upgradable from: 1.5.16-0ubuntu3]
python3-distupgrade/jammy-proposed,jammy-proposed 1:22.04.18 all [upgradable from: 1:22.04.17]
python3-software-properties/jammy-proposed,jammy-proposed 0.99.22.8 all [upgradable from: 0.99.22.7]
python3-update-manager/jammy-proposed,jammy-proposed 1:22.04.16 all [upgradable from: 1:22.04.10]
rfkill/jammy-proposed 2.37.2-4ubuntu3.1 amd64 [upgradable from: 2.37.2-4ubuntu3]
software-properties-common/jammy-proposed,jammy-proposed 0.99.22.8 all [upgradable from: 0.99.22.7]
software-properties-gtk/jammy-proposed,jammy-proposed 0.99.22.8 all [upgradable from: 0.99.22.7]
system-config-printer-common/jammy-proposed,jammy-proposed 1.5.16-0ubuntu3.1 all [upgradable from: 1.5.16-0ubuntu3]
system-config-printer-udev/jammy-proposed 1.5.16-0ubuntu3.1 amd64 [upgradable from: 1.5.16-0ubuntu3]
system-config-printer/jammy-proposed,jammy-proposed 1.5.16-0ubuntu3.1 all [upgradable from: 1.5.16-0ubuntu3]
ubuntu-desktop-minimal/jammy-proposed 1.481.2 amd64 [upgradable from: 1.481.1]
ubuntu-desktop/jammy-proposed 1.481.2 amd64 [upgradable from: 1.481.1]
ubuntu-drivers-common/jammy-proposed 1:0.9.6.2~0.22.04.6 amd64 [upgradable from: 1:0.9.6.2~0.22.04.4]
ubuntu-minimal/jammy-proposed 1.481.2 amd64 [upgradable from: 1.481.1]
ubuntu-release-upgrader-core/jammy-proposed,jammy-proposed 1:22.04.18 all [upgradable from: 1:22.04.17]
ubuntu-release-upgrader-gtk/jammy-proposed,jammy-proposed 1:22.04.18 all [upgradable from: 1:22.04.17]
ubuntu-standard/jammy-proposed 1.481.2 amd64 [upgradable from: 1.481.1]
update-manager-core/jammy-proposed,jammy-proposed 1:22.04.16 all [upgradable from: 1:22.04.10]
update-manager/jammy-proposed,jammy-proposed 1:22.04.16 all [upgradable from: 1:22.04.10]
util-linux/jammy-proposed 2.37.2-4ubuntu3.1 amd64 [upgradable from: 2.37.2-4ubuntu3]
uuid-runtime/jammy-proposed 2.37.2-4ubuntu3.1 amd64 [upgradable from: 2.37.2-4ubuntu3]
```

```
tama@tamagochi:/etc/apt$ lsb_release -a
No LSB modules are available.
Distributor ID:	Ubuntu
Description:	Ubuntu 22.04.3 LTS
Release:	22.04
Codename:	jammy
```

```
tama@tamagochi:/etc/apt$ uname -a
Linux tamagochi 6.2.0-35-generic #35~22.04.1-Ubuntu SMP PREEMPT_DYNAMIC Fri Oct  6 10:23:26 UTC 2 x86_64 x86_64 x86_64 GNU/Linux
```

```
tama@tamagochi:/etc/apt$ sudo apt upgrade
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
Calculating upgrade... Done
Get more security updates through Ubuntu Pro with 'esm-apps' enabled:
  vlc-plugin-qt libvlc5 vlc-data libvlccore9 vlc vlc-bin vlc-l10n
  libpostproc55 vlc-plugin-samba libavcodec58 vlc-plugin-notify libavutil56
  libswscale5 vlc-plugin-access-extra vlc-plugin-skins2
  vlc-plugin-video-splitter libswresample3 vlc-plugin-video-output
  libavformat58 libvlc-bin vlc-plugin-base vlc-plugin-visualization
Learn more about Ubuntu Pro at https://ubuntu.com/pro
#
# Canonical released microcode updates for both Intel (CVE-2022-40982) and AMD
# (CVE-2023-20593). ‘Unattended upgrades’ provide security updates by default.
# Ensure it remains enabled to always get all updates as they become available.
#
The following NEW packages will be installed:
  linux-headers-6.2.0-36-generic linux-hwe-6.2-headers-6.2.0-36 linux-image-6.2.0-36-generic linux-modules-6.2.0-36-generic linux-modules-extra-6.2.0-36-generic
The following packages have been kept back:
  gjs libgjs0g
The following packages will be upgraded:
  apparmor apt apt-utils bsdextrautils bsdutils eject fdisk firmware-sof-signed gnome-remote-desktop libapparmor1 libapparmor1:i386 libapt-pkg6.0 libblkid1 libblkid1:i386 libcryptsetup12 libfdisk1 libgpgme11 libgpgmepp6 libicu70
  libicu70:i386 libmount1 libmount1:i386 libsmartcols1 libuuid1 libuuid1:i386 libxmlb2 linux-firmware linux-generic-hwe-22.04 linux-headers-generic-hwe-22.04 linux-image-generic-hwe-22.04 linux-libc-dev mount openvpn
  python3-cupshelpers python3-distupgrade python3-software-properties python3-update-manager rfkill software-properties-common software-properties-gtk system-config-printer system-config-printer-common system-config-printer-udev
  ubuntu-desktop ubuntu-desktop-minimal ubuntu-drivers-common ubuntu-minimal ubuntu-release-upgrader-core ubuntu-release-upgrader-gtk ubuntu-standard update-manager update-manager-core util-linux uuid-runtime
54 upgraded, 5 newly installed, 0 to remove and 2 not upgraded.
Need to get 419 MB of archives.
After this operation, 708 MB of additional disk space will be used.
Do you want to continue? [Y/n]
```



sekalian upgrade kernel, setelah done baru reboot pc

```
tama@tamagochi:/etc/apt$ reboot
```



cek kernel

```
tama@tamagochi:~$ uname -a
Linux tamagochi 6.2.0-36-generic #37~22.04.1-Ubuntu SMP PREEMPT_DYNAMIC Mon Oct  9 15:34:04 UTC 2 x86_64 x86_64 x86_64 GNU/Linux
```
<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/repolokal1.png" />

sudah di versi terbaru dari sumber mirror.
saya rasa cukup unutk catatan kali ini.

Sekian.
