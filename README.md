<p align="center"><img src="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fjfj1178%2FKali-Linux-Termux&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false">

<img width="1100" height="500" src="https://github.com/xiv3r/Kali-Linux-Termux/blob/main/kali_nethunter/vnc.jpg">

# <h1 align="center"> Kali Nethunter Termux </h1>
 
<p align="center">Kali Linux NetHunter on Termux is a powerful tool for security professionals and enthusiasts. It allows users to perform a variety of security assessments on their Android devices without rooting them.</p>

<br></br>

<h1 align="center">
Download 
 
| [Termux](https://play.google.com/store/apps/details?id=com.termux)
|
| [RealVNC App](https://play.google.com/store/apps/details?id=com.realvnc.viewer.android)
|
</h1>

<br>

# Auto Install
```sh
apt update && apt install neofetch wget bsdtar axel proot pulseaudio -y && clear && wget -qO- https://raw.githubusercontent.com/xiv3r/Kali-Linux-Termux/refs/heads/main/kali_nethunter/kali-full | sh && clear && kali
```
> [!Note]
> - Login for User:`kali`
> - Login for Root:`kali -r`

> - ( to configure your vnc password )
```
kali vnc password 
```        
> - ( to run vnc service )
> - 127.0.0.1:5901
```
kali vnc &
```
> - [Next Open the VNC and place `kali` as username and your vnc `password`](https://play.google.com/store/apps/details?id=com.realvnc.viewer.android)

## Set custom terminal name
> Change `xiv3r` to your name
```
sed -i 's/user=kali/user=xiv3r/' /root/.bashrc
sed -i 's/user=kali/user=xiv3r/' /root/.zshrc
sed -i 's/user=kali/user=xiv3r/' /home/kali/.bashrc
sed -i 's/user=kali/user=xiv3r/' /home/kali/.zshrc
```
 <details><summary>
  
 <div align="center">
  
 # Prevent Termux VNC service from being Killed
 </div>
  
 <p align="center">" Process completed (signal 9) - press Enter "</p>

 </summary>

## Download & Install
- `Shizuku` and `Ashell` then enable wireless debugging through shizuku
- permit ashell from shizuku
- paste the adb commands below on ashell

- Execute the commands below, These commands will disable the phantom process killer:
```sh
adb shell /system/bin/device_config set_sync_disabled_for_tests persistent

adb shell /system/bin/device_config put activity_manager max_phantom_processes 2147483647

adb shell settings put global settings_enable_monitor_phantom_procs false
```
- To verify:
```sh
adb shell /system/bin/dumpsys activity settings | grep max_phantom_processes

adb shell /system/bin/device_config get activity_manager max_phantom_processes
```

</details>


