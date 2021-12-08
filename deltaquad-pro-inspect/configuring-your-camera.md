# Configuring your camera

Your Ground Control Station comes equipped with the [Flir UAS](https://www.flir.com/support-center/oem/uas-download/download-duo-pro-r-firmware--software/) app. This app uses Bluetooth to communicate with your Flir Duo Pro R. To connect to your camera make sure you are close to your UAV as the Bluetooth connection has limited range.

When first powering on the UAV, the camera will enable Bluetooth for approximately 1 minute. It will indicate this by a blue light. If the blue light is not solid or blinking, press the Bluetooth button on your camera. The app should automatically detect the camera.

The Flir Duo Pro is not triggered by the flight controller, it needs to be programmed for either distance or time interval triggering. If you wish to perform radiometric mapping with the Flir Duo Pro you will need to take the following steps:

1. Launch the Flir UAS app
2. Select the multi-image capture mode with an interval of 1 second
3. In the settings screen, make sure the function of PWM 3 is set to "start/stop recording"
4. Start the trigger process by clicking the big blue record button. When using the DeltaQuad Controller, this can be performed in flight by activating the trigger by switching button 8 as described in the [DeltaQuad Controller](deltaquad-controller.md) section.

![Flir UAS app](../.gitbook/assets/Selection\_073.png)

For more information on configuring your Flir Duo Pro R for the correct scene and thermal functions, please refer to the [Flir Duo Pro Quick Start Guide](https://flir.netx.net/file/asset/12933/original/attachment) or the [Flir Duo Pro R manual](https://www.flir.com/globalassets/imported-assets/document/duo-pro-r-user-guide-v1.0.pdf).
