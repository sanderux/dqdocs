# Firmware upgrade

When purchasing a DeltaQuad you will be notified of relevant firmware upgrades for your vehicle via email. The email will contain a link to the relevant firmware upgrade page and can contain specific instructions. You should only perform firmware upgrades when instructed to do so by your supplier. Under no circumstances should you reset your parameters to default.

If you are in need of assistance to perform the upgrade please contact [support@verticaltechnologies.com](mailto:support@verticaltechnologies.com)

## Preparing an upgrade

A firmware upgrade can only be performed using QGroundControl from a Windows or MacOS computer and requires a standard micro-usb cable. It can not be performed from an Android or IOS device.

A firmware upgrade generally consists of one binary file and one parameter file. The binary file has a _.px4_ extension and the parameter file has a _.params_ extension. You should download both files to your computer.

Make sure you can safely position your vehicle close to your computer and do not attach the flight battery.

## Performing the upgrade

To perform a firmware upgrade please follow the steps below;

1. Download and install [QGroundControl](http://qgroundcontrol.com/downloads/) on your computer.
2. Download the firmware binary and the parameter file to your computer. These files will be available on the link sent to you via email.
3. Insert A USB type C cable in the flight controllers USB port which is located near the serial number sticker in your UAV (do not attach it to your computer yet)
4. Start QgroundControl
5. Click on the settings button (cogwheel icon on top)
6. Click on 'Firmware'
7. Attach the USB cable to your computer, when properly connected this will be indicated on QGroundControl.
8. Make sure the PX4 firmware option is selected, check 'Advanced' and choose 'Custom' from the drop-down list, then click OK.
9. A file select dialog should appear, select the correct .px4 file. The upgrade process should now start and will inform you when it has finished. If the upgrade fails you can try again or use a different (thicker) USB cable.
10. Proceed to load the new parameter file as described below

## Loading the new parameters

Most firmware upgrades come with a parameter file. It is important to install the new parameters as they can contain crucial settings for the new firmware.

To load the parameters please use the following steps;

1. While the USB cable is connected, start QgroundControl and wait for the vehicle to connect
2. Click on the settings button (cogwheel icon on top)
3. Click on 'Parameters'
4. Click on the 'Tools' drop-down  on the right side of the screen
5. Select 'Load from file'
6. Select the correct parameter file from your computer and click "open"
7. Leave the USB cable connected for at least 10 seconds after selecting the parameter file.&#x20;
8. Perform any additional tasks as described in&#x20;
9. Remove the USB cable.&#x20;

## Post-upgrade steps

The email instructions for your firmware upgrade will include a method of validating the upgrade. Please make sure you validate the upgrade before flight.

Sometimes it will be required to perform a new sensor calibration after upgrading. This will be indicated with the firmware upgrade. When indicated, please follow the steps on the [sensor calibration](https://docs.verticaltechnologies.com/maintenance/sensor-calibration.html) page. Do not calibrate the sensors with the USB cable attached. Use your standard ground control station and telemetry unit for this.
