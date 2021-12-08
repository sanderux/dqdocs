# Telemetry & Ground Control

In this section we cover the setup of your Ground Control Station, Video and Telemetry links. For information on using the ground control station please refer to the [Flight](../flight/) sections in this manual.

## Installing QGroundControl

The DeltaQuad uses QGroundControl as its primary Ground Control Station.

If you have ordered a Ground Control Station with your DeltaQuad it will have been installed and tested before it was shipped to you. You may skip this section and proceed to the installation of your telemetry link.

To install QGroundControl on your device please refer to the [QGroundControl Installation Manual](https://docs.qgroundcontrol.com/en/getting\_started/download\_and\_install.html)

## Activating 4G VPN Telemetry

If your DeltaQuad has been equipped with 4G telemetry, you will need to insert a suitable sim-card in the USB 4G dongle which is located in the nose of the vehicle. To insert the sim card, remove the USB dongle, slide the top part of the housing down and insert the sim-card in the sim card placeholder. To test and optionally configure your 4G dongle, you can attach the dongle to your computer. After approximately 30 seconds it should be activated and you can check the status of your connection by opening a browser and navigating to [http://192.168.100.1](http://192.168.100.1)

If your Ground Control Station came with your vehicle it will have been pre-installed, but will still require an Internet connection. This connection can be established by inserting a micro-sim-card into the device. It can also be established by activating a wifi hotspot on a secondary device and connecting the ground control station to this WiFi network. At startup the Ground Control Station will connect to the VPN network after approximately 30 seconds.

If you chose to install your own ground control station, or if you wish to install additional ground control stations, please refer to the ZeroTier installation guide for additional setup steps. This guide will have been made available to you via e-mail. This will also contain the settings required to activate the video stream.

When inserting the USB dongle in the vehicle and switching the vehicle on by connecting the LiPo battery, the USB dongle should start blinking (first green, then white). After approximately 30 seconds it should go to solid white. At this point the vehicle has an active internet connection. It will take another 20 seconds for the vehicle to connect to the VPN network and your ground control station.

## Activating Radio Telemetry

If your vehicle is equipped with radio telemetry, no setup is required on the vehicle side. To activate radio telemetry on the ground control station simply attach the receiving unit of the radio telemetry system to the ground control station. If the vehicle does not automatically connect, add a new link manually to QGroundControl by clicking on Settings -> Comm Links -> Add, and selecting the proper serial device. This varies by system.
