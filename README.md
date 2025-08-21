## Kernel Modder
Normally the Linux kernel version string (shown in `uname -r` or `dmesg`) is set at compile time inside the kernel source. But if you don’t want to rebuild the entire kernel, you can patch the binary kernel image after unpacking your boot.img.

## Clone repo
```
git clone https://github.com/Jonjeexe/Kernel_Modder && cd Kernel_Modder && bash Setup.sh
```

## Now Start Modding
Enter Workplace folder
```
cd WORKPLACE && ls
```

## Unpack boot.img
Make sure your `boot.img` should be in internal storage but don't put in any folder that should be out of folders
and Termux has storage permission of do `termux-setup-storage`
```
chmod +x Tool
```
```
./Tool unpack /sdcard/boot.img
```
`Output`
![Image](https://github.com/user-attachments/assets/023df087-fd8d-40ea-82bc-8d43473c768a)

After unpack boot.img you will see.
- `kernel (the kernel binary)`
- `ramdisk.cpio (ramdisk)`
- `dtb (device tree, if present)`

Now we need `Kernel` file which is generated after unpack the boot.img
so we will search `Kernel version` 
## Find Kernel Version
```
strings kernel | grep "Linux version"
```
