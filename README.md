# Blackview A60 Pro

AOSP/GSI works perfectly well

Get an image from https://github.com/phhusson/treble_experimentations/releases (arm64_ab)

# stock image files
https://drive.google.com/file/d/1Ezci2vXa0fLOsOwB8SnXp0zV8f6Fuypu/view

# Unlock bootloader

1. Enable developer mode 
2. OEM unlock
3. `fastboot flashing unlock`

# Good tutorials and files
All credits for the files and tutorials to : https://www.youtube.com/user/vivalaJamie01/videos

- fix hard bricked device : https://www.youtube.com/watch?v=tbWXPfd4olQ
- fix imei : https://www.youtube.com/watch?v=ebAF79ZltcE (unfortunately this only works on windows)
- install twrp and magisk : https://www.youtube.com/watch?v=Q0mvdF3qeR0
- root : https://www.youtube.com/watch?v=m6lvYCMflX8

# This phone has a faulty usb charging port
- fix guide : https://www.youtube.com/watch?v=CewzzDd9Itw


# Fastboot usage
## Check if you can detect the device in fastboot mode
`fastboot devices # check if the device is detected`

## bootloader unlock
do not do this if you have unlocked the bootloader in the past

`fastboot flashing unlock`

## To do each time you want to flash something
`fastboot --disable-verification flash vbmeta vbmeta.img`

## How to flash partitions
- recovery
`fastboot flash recovery recovery.img`
- system
`fastboot flash system system.img`
- boot
`fastboot flash boot boot.img`


# Fix magisk after upgrading the system
If magisk doesn't find itself after upgrading the system partition or it conflicts with superuser, flash boot.img and reinstall magisk with superuser permission again

