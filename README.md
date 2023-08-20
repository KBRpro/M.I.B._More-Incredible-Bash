# M.I.B. - More Incredible Bash

![GEM](https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/blob/main/GEM.png)

# All bastards who stolen and selling this should be fucked🖕
## NOT FOR COMMERCIAL USE - IF YOU BOUGHT THIS YOU GOT RIPPED OFF!

M.I.B. is distributed under the GNU General Public License v2.0. See [LICENSE](https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/blob/main/LICENSE) for more information.

**Check https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki for even more details about M.I.B and your MHIG/MHI2/MHI2Q unit.**

## NOTE:
- M.I.B. is running on Harman MHIG (MIB1 High) and MHI2/MHI2Q (MIB2 High) units only.
- Minimum requirement to run M.I.B. in GEM is GEM version 4.1+.
- Old GEM of most units with old FW versions will automatically be updated to GEM 4.12 during M.I.B installation.

- Make sure, that you always run latest M.I.B version --> https://mib.mibsolution.one & https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash
- For additional Information check https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki & https://mibwiki.one

## CAUTION:
- Ensure that a external power is connected to the car during any flash or programming process!
- It is not recommended to flash with running engine!
- Power failure during flashing/programming will brick your unit.
- All you do and use at your own risk!

## M.I.B Functions:
- [Go here for a full overview of all GEM functions](https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki/M.I.B-MENU-STRUCTURE)
- [Patch ifs-root](https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki/Prepare-M.I.B-SD-card-&-install-M.I.B#3-do-stuff-smirk)
- [SVM fix](https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki/M.I.B-functions#svm-fix)
- [POG11 AndroidAuto button fix](https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki/Porsche-POG11-AndroidAuto-button-fix)
- [POG24 & BYG24 AndroidAuto & CarPlay Widescreen Patch](https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki/POG24-&-BYG24---AndroidAuto-&-CarPlay-Widescreen-Patch)

## [Prepare SD card](https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki/Prepare-M.I.B-SD-card-&-install-M.I.B#i---prepare-mib-sd-card):
- Extract all files of the M.I.B. to the root folder of a clean FAT32 formatted SD card
- Make sure that your SD card is not write protected.
- Patched IFS-stage2 images have to be placed on the SD card in the folder /patches
- Pre-patched (CP, FEC and EL) ifs-root-stage2 images can be found for all recent MHI2 FW versions here: https://mib.mibsolution.one
- You only have to copy the folder(s) you need for your car(s) - e.g. /patches/MHI2_ER_SKGxx_Pxxxx_MUxxxx_PATCH  
- They are already prepared in the right way, so that the tool can use them right away

There is also a example video guide available now:<br />
[![image](http://img.youtube.com/vi/eAQgzYlnSrA/0.jpg)](https://www.youtube.com/watch?v=eAQgzYlnSrA&t=110s)

### FEC Generator:
- M.I.B is generating custom FecContainer.fec files based on existing FecContainer.fec and addfec.txt in patch folder.
- addfec.txt can be edited with any ASCII editor (Notepad++). DO NOT change EOL. Only not yet existing FECs will be added to container during the process.
- Do NOT change FECContainer.fec with WhatTheFec tool, it will break file signature. M.I.B method will keep original FECs intact.

### Editing Patches to make Maps work for MSA(ROW Maps)
- Open the patches file on M.I.B folder, they can be downloaded from here: [Firmware Patches for MIB](https://mibsolution.one/index.php/f/179383)
- Copy your SW-train patch to the patches file
- Open the SW patch file compatible with your train and go to the AddFec folder
- Open the addFecs.txt file
- Edit the fec that starts with 023*****(like 023000EE) to 023D00ee
- In the navigation option of the M.I.B go to check navigation codes
- change the last two options to MSA or any RoW region that you need

### [ExceptionList BUG](https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki/ExceptionList-BUG)
- If your unit was patched with M.I.B before April 2021 run "Add new Fecs to FecContainer.fec" script in M.I.B -> PATCH.
- This will switch over to FecContainer.fec based patch and avoid EL BUG - unit will get stuck during boot.
 
### [M.I.B. in Green Engineering Menu - GEM](https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki/Prepare-M.I.B-SD-card-&-install-M.I.B#iii---enter-green-engineering-menu-gem-to-run-mib):
- After M.I.B SD card is prepared
- Insert the SD card into slot SD1 of your unit.
- Enter Engineering/Red Menu to start SW Update. Select UPDATE, select SD card, select "FREE for all - M.I.B. Launcher V1.2", START update.
- Installation of M.I.B. on your Unit will start. The unit will restart three time until update process is finished.
- GEM will be activated as part of the installation.
- SVM error has to be cleared via M.I.B. function in GEM after installation
- Enter GEM on your unit
- Select ==>>m.i.b<<== in GEM and have FUN!
  
### IMPORTANT! SD card must be presented in SD slot 1 (SD1) to enable M.I.B. in GEM. --> no SD no M.I.B.
- GEM screen layout is designed for 9.2'' screens but should work OK on 8'' just some text lines may look cut

### [Update to new M.I.B. version](https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki/Update-&-Uninstall-M.I.B):
- No need to reinstall M.I.B if you want to use a new version.
- Just create a fresh SD with latest M.I.B. version and insert into unit.

----------------------------------------------------------------------------------------------------------------------------------------

## [Old way, D-Link Method: Connect to MHI2 and start M.I.B.](https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki/About-M.I.B#mib-classic---putty-interface-not-maintained):
- This method is still available in M.I.B, but no longer fully supported.
- Basic functions are still available - Full functionallity is only given via GEM
-  D-Link - e.g. DUB-E100 HW rev. D1 - USB-Ethernet adapter is required to connect to your MHI2 unit.
-  Use Putty/Kitty to connect via UART or Telnet (MIB IP:172.16.250.248) and login into RCC (recommended: port:123) or MMX (port:23).
-  Login and password for your units SW train has to be known.
- Check your SW-train, a pre-patched ifs-root-stage2 has to be present within the folder /patches
- Insert the SD card into slot SD1 of your MHI2 unit and login to the RCC shell:
#### Mount SD card in slot SD1
- mount -uw /net/mmx/fs/sda0/
#### Start M.I.B by typing
- /net/mmx/fs/sda0/start

- Default screen size of Putty/Kitty is often too small to display the M.I.B. menu in full.
- Increase the window size manually.

### CONTACT:
- GITHUB: https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash
- Telegram Channel: https://t.me/joinchat/EHt4RRksHcMQk6Xi6tFaBw
- Wiki: https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki & https://mibwiki.one
- Get in contact with us to get support and provide feedback about M.I.B.

### Supporting Documents:
https://mibsolution.one

user and pass: guest
