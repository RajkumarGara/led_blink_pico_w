
# LED blink

  
  
  

## Install the prerequisites
**Step1:-** Open the WSL terminal and enter the following commands

**Step2:-**  Following commands will install gcc-arm-none-eabi. <br>
sudo apt update <br>
sudo apt install cmake gcc-arm-none-eabi libnewlib-arm-none-eabi build-essential git

  **Step3:-**  It will clone the pico sdk and pico examples. <br>
git clone https://github.com/raspberrypi/pico-sdk.git <br>
git clone https://github.com/raspberrypi/pico-examples.git

  **Step4:-**  Set the PICO_SDK_PATH Environment Variable. Enter your pico sdk path in place of path_to_pico-sdk in the below command. <br>
export PICO_SDK_PATH=path_to_pico-sdk

 **Step5:-**  Navigate to pico-examples path and intialize submodules by entering following commands. <br>
 git submodule init <br>
git submodule update

 **Step6:-**  Navigate to pico-sdk/lib/cyw43-driver and checkout the following command. It will update cyw43-driver, lwip, tinyusb to enable network-related and usb-related functionality.<br>
git submodule update --init


## Build Project
 **Step1:-**  Navigate to pico-examples path and enter following commands. <br>
mkdir build <br>
cd build <br>
cmake ..

 **Step2:-**  compile the project by entering following command.  <br>
 make