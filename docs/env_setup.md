# Environment setup

## Select your emulator
First follow through the instructions to get a linux environment ready.

[VMWare Fusion](vmware_setup.md) - MacOS

[WSL](wsl_setup.md) - Windows

## Setup SITL Simulator
Note: Install the following on your virtual machine.

1. Make a forge directory
```bash
mkdir ~/forge
cd ~/forge
```

2. Install GUI tools
```bash
sudo apt-get update
sudo apt-get install git
sudo apt-get install gitk git-gui
```

3. Clone the ArduPilot repo
```bash
git clone --recurse-submodules https://github.com/ArduPilot/ardupilot
cd ardupilot
```

4. Configure repo
```bash
Tools/environment_install/install-prereqs-ubuntu.sh -y
. ~/.profile
```

5. Restart your virtual machine

6. Build repo
```bash
cd ~/forge/ardupilot
./waf configure --board MatekH743
./waf copter
```

7. All done! Test with the following command
```bash
sim_vehicle.py -v copter --console --map -w -l 33.642871,-117.826633,0.0,0.0
```

## Setup Team Repo
1. Clone repo
```bash
cd ~/forge
git clone https://github.com/...
```

2. Create virtual environment
```bash
cd ~/forge/uavf26
python3 -m venv venv
source venv/bin/activate
pip install -e .
```

## Setup NoMachine
Note: Install the following on your main machine not a virtual machine.

Please download and install NoMachine [here](https://download.nomachine.com/everybody/)

NoMachine allows you to remote into a desktop with the GUI. Note that only 1 person can be NoMachine'd to a single machine at once.

## Setup tailscale
Note: Install the following on your main machine not a virtual machine.

1. Download and install tailscale [here](https://tailscale.com/download/)

3. Please create an account and sign in to tailscale (it will create your own tailnet)

4. You can use tailcale to connect to the labpc anywhere as long as you have internet. Once logged in, use your labpc tailscale share link to add the labpc to your tailnet