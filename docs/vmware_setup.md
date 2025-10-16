# VMWare Fusion

[Download here](https://www.vmware.com/products/desktop-hypervisor/workstation-and-fusion)

[Download the ISO for Ubuntu 22.04 Desktop ARM](https://drive.google.com/file/d/1c0qq2Zf095nTrmpyWammegNd-Tp92S4Y/view?usp=share_link)

## Setup Instructions
1. In the upper right hand corner click: `+` -> `New...`.

2. Drag in the ISO file download and click through the instructions, no need to configure anything beyond the defaults.

3. If the machine doesn't start automatically, double click the machine name in the sidebar of vmware fusion. Click `Enter` for `Try or Install Ubuntu` and wait.

4. Once the desktop loads, you should see an executable called `Install Ubuntu 22.04 LTS` in the bottom right corner of the desktop. Double click on it.

5. Select `English`, `Normal Installation`, and then `Erase disk and install Ubuntu`. Don't worry this won't erase your main disk, just the file the emulator storage is on. Finish through the onscreen instructions and click install.

6. Once the installation has finished, it will ask you to restart. However upon restart you may get errors related to the mounted iso image. You must first shutdown the virtual machine by clicking `Virtual Machine` -> `Shut Down` in the mac menu bar.

7. Now that the machine is shut down, with the virtual machine selected, click on the wrench icon in the top right corner of the vmware fusion window to open the settings.

8. In the settings, click on CD/DVD Drive, then **uncheck** `Connect CD/DVD Drive`

9. Then start the virtual machine back up by double clicking on the machine name in the left sidebar of vmware fusion.

10. You should be able to log in to your Ubuntu machine. You can click the mac `command` key and search for apps like `Terminal` where much of your work will be done.

## Setup VSCode
1. Go to this website to download the `.deb` file https://code.visualstudio.com/Download

2. Under `.deb` click `Arm64`

3. Once the binary downloads open the terminal app

4. Run `cd ~/Downloads` to get into your downloads folder

5. Run `sudo apt install ./<file>.deb` with `<file>` replace by the downloaded vscode file name. Note you can click `tab` after typing `sudo apt install ./` to autocomplete.

6. You should be prompted to accept the signing key, make sure to select `Yes` and hit `Enter`

7. VSCode should now be installed and you can view it in your apps

## Resize Volume
1. Make sure you machine is shut down

2. Open up the machine settings by clicking on the wrench in the upper right corner of vmware fusion.

3. Click `Hard Drive` and resize to at least 40 GB

4. Start up the machine by double clicking on the machine name

5. Once you log in open the `Disks` app

6. Click Filesystem Partition 2 which should be ~20 GB for the default, you should also see some `Free Space` in a seperate partition area.

7. Click the gear icon under volumes and click `resize`

8. Drag the slider to take up the extra free space and clicke `Resize`

9. All Done your system should now have more storage space
