# i3blocks blocklets  
![i3 Window Manager block](https://res.cloudinary.com/dttanwhco/image/upload/v1603038642/github/i3bar_fqkrfm.png)
 
This repository contains a set of scripts (a.k.a. blocklets) for [i3blocks](https://github.com/vivien/i3blocks)
##### Table of Contents  
[Battery](#battery)
<br />
[CPU and Memory](#cpu)
<br />
[Disk](#disk)
<br />
[Date, Time and Calendar](#date)
<br />
[Weather](#weather)
<br />
[Network](#network)
<br />
[IP](#ip)
<br />
[Quote](#quote)
<br />
[Volume](#volume)
<br />
[Backlight](#backlight)
<br />


## Battery  
![Battery blocklet](https://res.cloudinary.com/dttanwhco/image/upload/v1603038517/github/i3bar_battery_sv558o.png)  

This script will display the batteries charge percentage.  

### Dependencies
* acpi
* font awesome

### Installation  
* Copy the battery script into your directory of choice, e.g. ~/.config/i3blocks/
* Give it execution permission (`chmod +x battery`)
* Add the following blocket to your i3blocks config file:  
```ini
[battery]  
command=$SCRIPT_DIR/battery  
interval=5  
markup=pango  
```  


## CPU  
![CPU blocklet](https://res.cloudinary.com/dttanwhco/image/upload/v1603038517/github/i3bar_cpu_mem_s7m7do.png)  

This script will display the CPU and RAM memory usage.  

### Dependencies
* python
* psutil
* a task manager e.g xfce4-taskmanager
* font awesome

### Installation  
* Copy the cpu_mem script into your directory of choice, e.g. ~/.config/i3blocks/
* Give it execution permission (`chmod +x cpu_mem`)
* Add the following blocket to your i3blocks config file:  
```ini
[cpu_mem]  
full_text=click  
command=$SCRIPT_DIR/cpu_mem  
interval=1  
markup=pango  
color=#91E78B
```
* Replace ```subprocess.call("xfce4-taskmanager")```  
with a task manager of your choice.    

## Disk  
![Disk blocklet](https://res.cloudinary.com/dttanwhco/image/upload/v1603038517/github/i3bar_disk_pn3ki7.png)  

This script will display the disk usage e.g How much disk space is left and the percentage used.  

### Dependencies
* font awesome

### Installation  
* Copy the disk script into your directory of choice, e.g. ~/.config/i3blocks/
* Give it execution permission (`chmod +x disk`)
* Add the following blocket to your i3blocks config file:  
```ini
[disk]    
command=$SCRIPT_DIR/disk  
interval=600    
color=#ff7df4
```
* Replace ```'/dev/mapper/cryptroot'```  
with the disk that you want to monitor.


## Date  
![Date blocklet](https://res.cloudinary.com/dttanwhco/image/upload/v1603038517/github/i3bar_time_date_jg6pes.png)  

This script will display the time and date, with an option to open and close a calendar.  

### Dependencies
* font awesome
* orage calendar, or a calendar of your choice.

### Installation  
* Copy the time_date script into your directory of choice, e.g. ~/.config/i3blocks/
* Give it execution permission (`chmod +x time_date`)
* Add the following blocket to your i3blocks config file:  
```ini
[time_date]   
full_text=
command=$SCRIPT_DIR/time_date  
interval=5    
```
* Replace ```'orage --toggle' and 'orage'```  
with a calendar of your choice.

## Weather  
![Weather blocklet](https://res.cloudinary.com/dttanwhco/image/upload/v1603038518/github/i3bar_weather_lzvtsz.png)  

This script will contact the wttr.in api and display the weather, with an option to open a terminal to display detailed weather information.  

### Dependencies
* curl
* xfce4-terminal or other

### Installation  
* Copy the weather script into your directory of choice, e.g. ~/.config/i3blocks/
* Give it execution permission (`chmod +x weather`)
* Add the following blocket to your i3blocks config file:  
```ini
[weather]   
full_text=
command=$SCRIPT_DIR/weather  
interval=3600
color=#ebe310
```
* Replace ```'xfce4-terminal'```  
with a terminal of your choice.

## Network  
![Network blocklet](https://res.cloudinary.com/dttanwhco/image/upload/v1603038517/github/i3bar_network_zhuacl.png)  

This script will display the download and upload traffic on your network.  

### Dependencies
* vnstat
* font awesome

### Installation  
* Copy the network script into your directory of choice, e.g. ~/.config/i3blocks/
* Give it execution permission (`chmod +x network`)
* Add the following blocket to your i3blocks config file:  
```ini
[network]   
full_text=
command=$SCRIPT_DIR/network  
interval=2
markup=pango
```

## IP  
![IP blocklet](https://res.cloudinary.com/dttanwhco/image/upload/v1603038517/github/i3bar_check_my_ip_hstpot.png)  

This script will contact NordVPN's api and inform you if your ip is protected or not.
For example, if you're on a VPN or not.  

### Dependencies
* curl

### Installation  
* Copy the ip script into your directory of choice, e.g. ~/.config/i3blocks/
* Give it execution permission (`chmod +x ip`)
* Add the following blocket to your i3blocks config file:  
```ini
[ip]   
command=$SCRIPT_DIR/ip  
interval=60
markup=pango  
color=#91E78B
```

## Quote  
![Quote blocklet](https://res.cloudinary.com/dttanwhco/image/upload/v1603039224/github/i3bar_quotes_lualdl.png)  

This script will select a random quote from an api server and display it for you.  

### Dependencies
* python

### Installation  
* Copy the quotes script into your directory of choice, e.g. ~/.config/i3blocks/
* Give it execution permission (`chmod +x quotes`)
* Add the following blocket to your i3blocks config file:  
```ini
[quotes]   
command=$SCRIPT_DIR/quotes  
interval=21600
markup=pango
```   
## Volume    
![Volume blocklet](https://res.cloudinary.com/dttanwhco/image/upload/v1603038518/github/i3bar_volume_de9j0n.png)  

This script will display the volume with options to mute/unmute and also open a volume control application.  

### Dependencies
* pulsemixer
* pavucontrol or other volume control application
* font awesome

### Installation  
* Copy the volume script into your directory of choice, e.g. ~/.config/i3blocks/
* Give it execution permission (`chmod +x volume`)
* Add the following blocket to your i3blocks config file:  
```ini
[volume]   
full_text=click
command=$SCRIPT_DIR/volume  
interval=once
signal=10
color=#eb9234
```   
* Add these to your i3wm config file e.g ~/.config/i3/config   
```
## i3block audio volume·
bindsym --release XF86AudioRaiseVolume exec pkill -SIGRTMIN+10 i3blocks
bindsym --release XF86AudioLowerVolume exec pkill -SIGRTMIN+10 i3blocks
bindsym --release XF86AudioMute exec pkill -SIGRTMIN+10 i3blocks
```  
## Backlight    
![Backlight blocklet](https://res.cloudinary.com/dttanwhco/image/upload/v1603038517/github/i3bar_backlight_gtpqmo.png)  

This script will display the brightness of your screen.  

### Dependencies
* ![light](https://github.com/haikarainen/light)
* font awesome

### Installation  
* Copy the backlight script into your directory of choice, e.g. ~/.config/i3blocks/
* Give it execution permission (`chmod +x backlight`)
* Add the following blocket to your i3blocks config file:  
```ini
[backlight]   
command=$SCRIPT_DIR/backlight  
interval=once
signal=9
color=#f7f374
```   
* Add these to your i3wm config file e.g ~/.config/i3/config   
```
## i3block screen brightness·
bindsym --release XF86MonBrightnessUp exec pkill -SIGRTMIN+9 i3blocks           
bindsym --release XF86MonBrightnessDown exec pkill -SIGRTMIN+9 i3blocks
```
