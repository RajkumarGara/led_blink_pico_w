
  

# LED blink
This project will blink the pico-w on board led for every 200 msec. 
  
  

## Installation of prerequisites and build process

**Step1:-** Open the WSL terminal and enter the following commands

**Step2:-** Following commands will install gcc-arm-none-eabi. <br>
`sudo apt update` <br>
`sudo apt install cmake gcc-arm-none-eabi libnewlib-arm-none-eabi build-essential git`
  
**Step3:-** It will clone the pico sdk.<br>
`git clone https://github.com/raspberrypi/pico-sdk.git --branch master`<br>
`cd pico-sdk`<br>
`git submodule update --init`

**Step4:-** Navigate to pico-sdk/lib/cyw43-driver and checkout the following command. It will update cyw43-driver, lwip, tinyusb to enable network-related and usb-related functionality.<br>
`cd lib/cyw43-driver`<br>
`git submodule update --init`

**Step5:-** checkout https://github.com/RajkumarGara/led_blink_pico_w/tree/master/picow_blink. Navigate to picow_blink folder. Then enter the following commands<br>
`mkdir build`<br>
`cd build`

**Step6:-** Set the PICO_SDK_PATH Environment Variable with following command. Enter your pico sdk path in place of path_to_pico-sdk in the below command. <br>
`export PICO_SDK_PATH=path_to_pico-sdk`

**Step7:-** In the below command update your wifi ssid and password and build the project.<br>
`cmake -DPICO_BOARD=pico_w -DWIFI_SSID="Babbayaga" -DWIFI_PASSWORD="9254776877" ..`

**Step8:-** compile the project by entering following command.<br>
`make`


## Connections

connect pico w to laptop through usb.
```
![connections](https://github.com//RajkumarGara/led_blink_pico_w/picow_blink/images/connections.jpg)
```
```
![connections](https://github.com//RajkumarGara/led_blink_pico_w/picow_blink/images/pico_w.jpg)
```
