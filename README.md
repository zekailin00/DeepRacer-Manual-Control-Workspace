# DeepRacer-Manual-Control-Workspace

## Use Xbox controller 
1. `sudo bash -c "echo Y > /sys/module/bluetooth/parameters/disable_ertm"` 
2. `bluetoothctl`
3. `scan on` and `scan off` to get the MAC address of the controller 
4. `pair [MAC address]`
5. `connect [MAC address]`
6. `quit` 
## Launch Instruction

```
$ git clone git@github.com:zekailin00/DeepRacer-Manual-Control-Workspace.git
$ cd DeepRacer-Manual-Control-Workspace
$ git submodule update --init
$ sudo su
$ systemctl stop deepracer-core
$ source /opt/ros/foxy/setup.bash
$ colcon build
$ . install/setup.bash
$ ros2 launch manual_launcher manual_launcher.py
```
