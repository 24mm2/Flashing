# Technical Information

## The makings of our .bin files
Because the .bin files have to be compatible with the upload mechanisme of Mu, the bin files are generated slightly different that normal .bin files.

###Method:
1. Using Arduino we `Export compiled Binary` from the `Sketch`
2. Compile with verbose settings on, so you can see the link to the temporary boot- and partition files.
3. We have installed __esptool__, see main page in this repository
4. We then merge the .bin files together with `python3 -mesptool --chip esp32 merge_bin --output output.bin 0x0 bootfile.bin 0x7000 partitionfile.bin 0xF000 input.bin`
