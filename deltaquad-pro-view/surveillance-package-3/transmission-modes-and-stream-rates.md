---
description: >-
  This section describes how the transmission modes and stream rates are
  controlled.
---

# Transmission modes and stream rates

## Transmission mode

Controlling the active transmission mode is done by using the data link bar. The data link bar is displayed in the top of the screen and will always remain visible.

![](../../.gitbook/assets/Selection\_318.jpg)

&#x20;The available modes will display in white, and the currently active mode will display in green.

* MODES:
  * RADIO: This mode uses the internal radio system. The radio system is capable of transmission ranges up to 30KM, or up to 50KM when your system is equipped with the booster package.
  * LTE: This mode uses the mobile network over a VPN secured data link. To use LTE mode the following needs to be activated:
    * A sim card needs to be installed inside the UAV. The LTE dongle is located in the nose section of the vehicle and can be accessed when the battery is disconnected. Make sure the sim card has sufficient data available and that it is not secured with a pin-code. To test the connectivity of your LTE dongle with your sim card you can insert the dongle into a windows based laptop. After approximately 1 minute a webpage will open with the dongle settings and status.
    * The DeltaQuad controller needs to be connected to a WiFi network or mobile hotspot.
* VIDEO FEEDS:
  * GIMBAL: This is the Nighthawk2 camera gimbal feed. Activate this feed when deploying the Nighthawk2 Camera gimbal.
  * FPV: This is the static nose camera feed. While the gimbal is retracted it is recommended to use this feed.
  * OFF: This disables both feeds and stops any data consumption. If the data link becomes intermittent it is recommended to disable the video feeds to remain connected to your UAV.

## Stream rates

The DeltaQuad can control the stream rate of the Nighthawk2 camera gimbal. A high stream rate provides high quality video and a low stream rate provides lower quality video.&#x20;

### In RADIO mode

When the transmission mode is set to Radio, the system constantly monitors the available bandwidth and automatically tunes the camera stream to provide the best possible quality given the available bandwidth. This process is automatic and no manual input is required to tune the stream rate.

### In LTE mode

When the transmission mode is set to LTE, the system can not automatically determine the available bandwidth. For LTE-based transmission, both the vehicle and the DeltaQuad Controller require an internet connection. The available bandwidth in LTE mode depends on several factors such as:

* Distance from the cell tower
* Flight altitude
* Mobile network capabilities (3G/4G/LTE)
* VPN server proximity
* Network limitation

The DeltaQuad controller offers buttons that can control the stream rate while the vehicle is in LTE transmission mode. Stream rate control is only available for the Nighthawk2 Camera gimbal, it will not change the stream rate for the FPV nose camera.

![](<../../.gitbook/assets/dqnav-layout-view3 (1).png>)

The LTE stream rate buttons (9) are labeled A to F. When a button from this section is pressed, it will light up to indicate the currently active mode. The stream rate is adjusted according to the selected button. Button A is the default mode and provides the highest stream rate. The following table provides approximate data rates for each of the buttons:

| Button | Data rate |
| ------ | --------- |
| A      | 960 KB/s  |
| B      | 800 KB/s  |
| C      | 640 KB/s  |
| D      | 480 KB/s  |
| E      | 310 KB/s  |
| F      | 150 KB/s  |

When flying on LTE-based transmission, and your data rate exceeds your available bandwidth, the video feed will become unstable or delayed. If this happens, you can lower the stream rate until the video feed is stable. You may also choose to lower the stream rate to save data.
