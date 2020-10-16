# i3blocks blocklets
This repository contains a set of scripts (a.k.a. blocklets) for [i3blocks](https://github.com/vivien/i3blocks)
##### Table of Contents  
[Battery](#battery)
<br />
[CPU and Memory](#cpu)
<br />
[Disk](#disk)
<br />
[Date, time and Calendar](#date)
<br />
[Weather](#weather)
<br />
[Network](#network)
<br />
[IP](#ip)
<br />
[Quote](#quote)
<br />


## Battery  

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


## Cpu  

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
<br />

## Quote
<br />
