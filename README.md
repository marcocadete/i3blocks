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
<br />


## Date
<br />

## Weather
<br />

## Network
<br />

## IP
<br />

## Quote
<br />
