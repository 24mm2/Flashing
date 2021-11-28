# Flashing
There is 3 methods described here to flash firmware to our cores, all available on Windows, MacOS, and Linux, including ARM versions.

1. _Easy_: Using [__Mu__](#Mu "Go to Mu instructions...")
2. _Fast_: Using Espressif's Python based [ESPtool](#ESPtool "Go to the ESPtool instructions...")
3. _Flexible_: Compile and upload the source with [__Arduino__](#Arduino  "Go to the Arduino instructions...")

If you have any issues with these, try the [Troubleshooting](#Troubleshooting  "Go to the Troubleshooting section below...") section below.

Optionally see [more techincal information here](TECHNICAL.md  "Take be to the Technical Information page...") about how the .bin files are created.

## Mu
Mu[†](#†) is a Python editor usefull with embedded solutions, such as this. Our cores are based on the Espresssif ESP32, and Mu supports programming in MicroPython on the ESP32. Mu also has a firmware flashing tool to flash MicroPython to an ESP32, but we are using this flashing tool to flash our firmware to the same core.

### Instructions
1. Download and install Mu, following the instructions here: https://codewith.mu/en/download.
2. Start Mu: It will download some more files, so it can take a bit time first time around.
3. Download the .bin file you want to flash, as instructed in the repository that led you here.
4. Assemble and insert the circuit into a USB port. Click :ok:, if the message below occurs.![Detected](images/detected.png "Detected")
5. Check, in the lower right corner, that the circuit is inserted and detected by seeing this ![Inserted](images/inserted.png "Inserted") and _not_ this ![Not Inserted](images/not-inserted.png "Not Inserted")
6. Click on the gear ![Gear](images/gear.png "Gear") to get to the flashing menu.
7. Flashing:![M flashing](images/mu-flashing.png "Mu flashing")
   1. Choose the second tab `ESP Firmware flasher`.
   2. Select `ESP32` in the dropdown menu.
   3. `Browse` to your .bin file.
   4. Click on `Erase & write firmware`.

> This method is easy, but a slow way to flash firmware if you have several cores to flash. Below using [ESPtool](#ESPtool "Goto ESPtool instructions") you can flash much faster, but it is more complicated.

## ESPtool
This is a command line tool, which means you have to use the terminal application to execute the flashing commands. It is assumed you are familiar with the terminal application on your platform. This tool uses Python version 3 and Pip to install ESPtool. Some operating systems comes with Python installed by default, and the latest version of Python has Pip installed by default. It is beyond the scope of this help page to assist you installing Python and/or Pip, so it will be assumed this is already installed.

### Instructions
1. Open your Terminal application.
2. Install ESPtool: `pip3 install esptool`.
3. Download the __fastflash__ script.
4. Download the .bin file you want to flash, as instructed in the repository that led you here.
5. Assemble and insert the circuit into a USB port. You can limit that to the Core and the Interface, for faster turnaround.
6. Optionally erase the core: ``
7. 

## Arduino

### Instructions


# Troubleshooting

Below is a number of steps you can try if you have problems with any of the above:

## Installation
- For Mu: Make sure you read the installation instruction. There is a button next to the download button for each of the supported operating systems.
- For Mu and MacOS: Maybe you have security issues, try see if this page will help you: [Fix application from internet gatekeeper](https://www.idownloadblog.com/2017/04/20/fix-application-from-internet-gatekeeper/)
- For ESPtool and MacOS: If you don't have Pip installed, try this:
  ```
  curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py && python3 get-pip.py
  rm get-pip.py
  ```

- - - -
## † 
Mu is the pronounciation of the greek letter μ, which is the SI prefix for micro, here referring to micro controllers.
