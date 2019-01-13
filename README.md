Synaptics Touch Controller Driver for Lumias
======================

This Synaptics Touch (KMDF) driver is modified from the deleted one in Windows Driver Samples.

It demonstrates how to write a HID miniport driver for the Synaptics 3200 touch controller.

lumia1520 & 930 tested。


# [INSTALLTION]
replace the stock one which on the \windows\system32\drivers 
import the reg file.

# Lumia930

Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\RTSYSTEM\TOUCH\SCREENPROPERTIES]
"DisplayViewableHeight"=dword:00000598
"DisplayViewableWidth"=dword:00000a49

# Lumia1520

Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\RTSYSTEM\TOUCH\SCREENPROPERTIES]
"DisplayViewableHeight"=dword:00000595
"DisplayViewableWidth"=dword:00000a54


# Notice: For other lumias you should  calc the adjust value by yourself.

DisplayViewableWidth = RESOLUTION_X / 816 *  RESOLUTION_X

DisplayViewableHeight = RESOLUTION_Y / 1394 *  RESOLUTION_Y

816/1394 is the value which was founded in stock driver. 
seem all the same.
