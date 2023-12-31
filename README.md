
# LED blink

  
  
  

## Install the prerequisites
**Step1:-** Open the WSL terminal and enter the following commands

**Step2:-**  Following commands will install gcc-arm-none-eabi
sudo apt update
sudo apt install cmake gcc-arm-none-eabi libnewlib-arm-none-eabi build-essential git

  **Step3:-**  It will clone the pico sdk and pico examples. 
git clone https://github.com/raspberrypi/pico-sdk.git
git clone https://github.com/raspberrypi/pico-examples.git

  **Step4:-**  Set the PICO_SDK_PATH Environment Variable. Enter your pico sdk path in place of path_to_pico-sdk in the below command. 
export PICO_SDK_PATH=path_to_pico-sdk

 **Step5:-**  Navigate to pico-examples path and intialize submodules by entering following commands. 
 git submodule init
git submodule update

 **Step6:-**  Navigate to pico-sdk/lib/cyw43-driver and checkout the following command. It will update cyw43-driver, lwip, tinyusb to enable network-related and usb-related functionality.
git submodule update --init


## Build Project
 **Step1:-**  Navigate to pico-examples path and enter following commands. 
mkdir build
cd build
cmake ..

 **Step2:-**  compile the project by entering following command. 
 make