
# Building PX4 Software
## Clone
```
 git clone https://github.com/PX4/Firmware.git 
 git clone https://github.com/PX4/Bootloader.git
```
you can select specail version 
```
 git tag -l
 git checkout ${version}
```

update submoduel
```
git submodule update --init --recursive
```

## Build simulator
```
 make posix jmavsim
```
**The compiler of arm-none-eabi-gcc must be v7 on linux** 

## Build for Borads
| Borad                           |                   command                    |
| :----------------------------- | :------------------------------------------: |
| Pixhawk 4                       |           make px4fmu-v5_default            |
| Pixracer                        |           make px4fmu-v4_default            |
| Pixhawk 3 Pro                  |          make px4fmu-v4pro_default           |
| Pixhawk Mini                   |           make px4fmu-v3_default            |
| Pixhawk 2                       |           make px4fmu-v3_default            |
| mRo Pixhawk                    | make px4fmu-v3_default (supports 2MB Flash) |
| HKPilot32                       |           make px4fmu-v2_default            |
| Pixfalcon                       |           make px4fmu-v2_default            |
| Dropix                          |           make px4fmu-v2_default            |
| MindPX/MindRacer               |            make mindpx-v2_default            |
| mRo X-2.1                       |            make auav-x21_default             |
| Crazyflie 2.0                  |           make crazyflie_default            |
| Intel® Aero Ready to Fly Drone |           make aerofc-v1_default            |
| Pixhawk 1                       |           make px4fmu-v2_default            |