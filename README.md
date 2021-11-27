# Flashing
There is 3 methods described here to flash firmware to our cores, all available on Windows, MacOS, and Linux, including ARM versions.

1. Using the Mu editor
2. Using Espressif's Python based `esptool`
3. Compile and upload the source with Arduino

## Mu editor
The Mu editor is a Python editor especially usefull with embedded solutions, such as this. Our cores are based on the Espresssif ESP32, and the Mu edior supports programming in MicroPython on the ESP32. The Mu editor also has a firmware flashing tool to flash MicroPython to an ESP32, but we are using this flashing tool to also flash our firmware to the same core.

### Instructions
1. Download and install the Mu editor, following the instructions here: https://codewith.mu/en/download
2. Start the Mu editor: It will download some more files, so it can take a bit time first time around.
3. Download the .bin file you want to flash, as instructed in the repository that led you here.
4. Assemble and insert the circuit into a USB port.
5. Check 
