# Yuzu (Unofficial) Install Script(s) for Linux RetroPie

yuzu.sh will integrate into the Retropie Setup as an additional entry for installation. The official way to integrate external emulators and scripts got to the following folder: *~/RetroPie-Setup/ext*
This is to make sure that we do not interfere with the normal scriptmodules provided by Retropie.

### Requirements
wget, jq, git

### Install the script to Retropie-Setup

1) Git clone this repository to *~/RetroPie-Setup/ext* folder inside retropie setup:
 
```
git clone https://github.com/parasven/retropie_yuzu.git ~/RetroPie-Setup/ext/retropie_yuzu
```

2) Next, edit `~/RetroPie-Setup/platforms.cfg` and add:

```
switch_exts=".NSI .XCI"
switch_fullname="Nintendo Switch"
```


### Using the Script

Using this script is simple, just launch RetroPie and go to 'RetroPie Setup,' or in a terminal type `sudo ~/RetroPie-Setup/retropie_setup.sh`, update the Script and then install Yuzu (Pre-Compiled Binary) from `Packages > EXP > Yuzu`

This method script also works for Updating the emulator from the menu as well and should not require any additional configuration after installing for the first time. In RetroPie-Setup go to `Packages > EXP > Yuzu` and choose `Update (from Pre-Compiled Binary)` after it has been installed for the first time

Cheers

***Shoutout***
If you are viewing this page, you may also be interested in checking out this script for adding RPCS3 to the RetroPie menu

https://github.com/raelgc/retropie_rpcs3


Please note about the RPCS3 script: Modern installations of RetroPie no longer store `platforms.cfg` in `/opt/retropie/configs/all/` please instead repeat step 3 on *THIS PAGE* for RPCS3 to add Fullname and EXTS to the correct plaforms.cfg file. 


If you do NOT do this step either for RPCS3 or Yuzu, every time you update the emulator through RetroPie-Setup you will have to add the Fullname and supported file extenstions (exts) to `/etc/emulationstation/es_systems.cfg`
