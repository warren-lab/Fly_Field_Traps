# Image Acquisition

It is important to remeber that if the NOIR camera is being used then you will need to utilize the NOIR hue script and implement that into the associated script. There is a script where this is already implemented under NOIR_CAM_EXP. If the HQ camera is being used then use the HQ_CAM_EXP.

Before starting either experiment it is important that the user first start by setting the control file. This is done by using the "Set_Control.py" script. This will allow the user to set the frame rate, start time, duration and other parameters on the devices (ex: brightness, contrast....). After this has been performed then the new script can be copied to each device (do this over ssh, server, usb, on the pi, or manually change). This work that needs to be done is somewhat time consuming in order to get all of the pis ready; however, this will allow all of the pis to be essentially in sync with their start times appropriately set.

The image acquisition script will read in the json file first and convert it into a dictionary in order to parse through the parameters and assign them where appropriate.

The script "picam_NOIR.py" is referenced from the NOIR HUE FIX, and is as such so that the picamera package can be called by referencing that script.