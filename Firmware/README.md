# Writing bootloader for E3EZ
1. Download the [bootloader.bin](./E3EZ_bootloader.bin) file to CB1/CM4.
2. Press and hold the boot button of E3EZ and then click the reset button to make E3EZ goto DFU mode.
3. Run the following command on the Terminal of CB1/CM4 to write the bootloader
    ```
    sudo dfu-util -d ,0483:df11 -R -a 0 -s 0x8000000:leave -D ./E3EZ_bootloader.bin
    ```
    `0483:df11` is the DFU ID of M8P (We can get it by running `lsusb` command)</br>
    `./E3EZ_bootloader.bin` is the Path of bootloader file.
