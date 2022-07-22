# DeltaQuad Controller

## Introduction

Your DeltaQuad Pro #VIEW comes with the DeltaQuad Controller. The DeltaQuad controller provides the communication link between your UAV and the ground systems.

![](../../.gitbook/assets/DQNAV-e1617791913153.png)

## Getting started

To connect your UAV to the DeltaQuad controller simply switch on the UAV and press and hold the POWER button on the controller for 3 seconds. Once the controller is booted up, the main menu will display.

![](../../.gitbook/assets/vlcsnap-2021-04-16-17h37m56s783.png)

Before launching your flight control system it is recommended to connect the controller to a mobile hotspot or wifi network, The controller uses internet connectivity to load satellite maps and for LTE connectivity to the UAV. The DeltaQuad controller needs to be connected to a 5Ghz mobile hotspot or WiFi network. As the main communication link for the controller is based on 2.4Ghz, these networks will not be displayed. When using a mobile phone hotspot please make sure you configure the hotspot for 5Ghz.

In the top of the screen you will find the data link bar.

![](../../.gitbook/assets/Selection\_318.jpg)

The data link bar will always remain visible and allows you to control the type of transmission and select the active camera feed. The available modes will display in white, and the currently active mode will display in green.

* MODES:
  * RADIO: This mode uses the internal radio system. The radio system is capable of transmission ranges up to 30KM, or up to 50KM when your system is equipped with the booster package.
  * LTE: This mode uses mobile network over a VPN secured data link. To use LTE mode the following needs to be activated:
    * A sim card needs to be installed inside the UAV. The LTE dongle is located in the nose section of the vehicle and can be accessed when the battery is disconnected. Make sure the sim card has sufficient data available and that it is not secured with a pin-code. To test the connectivity of your LTE dongle with your sim card you can insert the dongle into a windows based laptop. After approximately 1 minute a webpage will open with the dongle settings and status.
    * The DeltaQuad controller needs to be connected to a WiFi network or mobile hotspot.
* VIDEO FEEDS:
  * GIMBAL: This is the Nighthawk2 camera gimbal feed. Activate this feed when deploying the Nighthawk2 Camera gimbal.
  * FPV: This is the static nose camera feed. While the gimbal is retracted it is recommended to use this feed.
  * OFF: This disables both feeds and stops any data consumption. If the data link becomes intermittent it is recommended to disable the video feeds to remain connected to your UAV.

For more information please refer to the [Transmission Modes & Stream Rates section](transmission-modes-and-stream-rates.md)

## Starting the UAV control system

{% hint style="info" %}
Before takeoff, always center all switches, and turn all dials to the left.
{% endhint %}

From the main menu launch the CCA3 app. This application, based on QGroundControl, is specifically designed for compatibility with your Nighthawk2 camera system.

From the CCA3 app you will be able to plan your initial mission. Missions are always planned to ensure the vehicle has a predefined takeoff and landing pattern. Even when you intend to manually control the UAV or control the UAV using reposition or target following commands, it is recommended to plan a mission for takeoff and landing.

Please review the [mission planning section](../../flight/planning-a-mission.md) for detailed information on how to plan a mission.

## Overview of the buttons

![](../../.gitbook/assets/dqnav-layout.png)

| Number | Type                                                              | Function                                                                                                                                                                                                                                                                                                                                             |
| ------ | ----------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1      | <p>3 position switch</p><p><strong>FLIGHT MODE</strong></p>       | <p>UP: Position flight mode</p><p>CENTER: neutral - no function</p><p>DOWN: Mission flight mode</p>                                                                                                                                                                                                                                                  |
| 2      | <p>3 position switch</p><p><strong>RETURN</strong> </p>           | <p>UP: Return flight mode</p><p>CENTER: neutral - no function</p><p>DOWN: neutral - no function</p>                                                                                                                                                                                                                                                  |
| 3      | <p>Dial</p><p><strong>FLIGHT SPEED</strong></p>                   | <p>Left: minimum flight speed</p><p>Right: maximum flight speed</p>                                                                                                                                                                                                                                                                                  |
| 4      | Dial                                                              | Not assigned                                                                                                                                                                                                                                                                                                                                         |
| 5      | 3 position switch                                                 | Not assigned                                                                                                                                                                                                                                                                                                                                         |
| 6      | <p>3 position switch</p><p><strong>FOLLOW</strong></p>            | <p>UP: Activate object following</p><p>CENTER: deactivate object following</p><p>DOWN: deactivate object following</p>                                                                                                                                                                                                                               |
| 7      | Joystick                                                          | <p><strong>In hover mode</strong></p><p>Stick up: move forward</p><p>Stick down: move backward</p><p>Stick left: move left</p><p>Stick right: move right</p><p></p><p><strong>In fixed-wing mode</strong></p><p>Stick up: descend (nose down)</p><p>Stick down: climb (nose up)</p><p>Stick left: bank left</p><p>Stick right: bank right</p><p></p> |
| 8      | <p>Push button</p><p><strong>RETRACT/ DEPLOY CAMERA</strong></p>  | <p>Not active (light off): retract camera gimbal</p><p>Active (light on): deploy camera gimbal (when armed)<br>Press and hold (light blinking): force deploy</p><p><em>RETRACT BEFORE LANDING</em></p>                                                                                                                                               |
| 9      | <p>A to F push buttons</p><p><strong>LTE STREAM RATE</strong></p> | <p>LTE stream rate control</p><p><a href="transmission-modes-and-stream-rates.md">More information</a></p>                                                                                                                                                                                                                                           |
| 10     | <p>Push button</p><p><strong>POWER</strong></p>                   | <p>Press and hold: power on/off</p><p>Press: screen on/off</p>                                                                                                                                                                                                                                                                                       |
| 11     | <p>Joystick</p><p><strong>ZOOM</strong></p>                       | <p>UP: Zoom in</p><p>DOWN: Zoom out</p>                                                                                                                                                                                                                                                                                                              |
| 12     | Joystick                                                          | <p><strong>In hover mode</strong></p><p>Stick up: climb</p><p>Stick down: descend</p><p>Stick left: yaw left</p><p>Stick right: yaw right</p><p></p><p><strong>In fixed-wing mode</strong></p><p>Stick up: gimbal up</p><p>Stick down: gimbal down</p><p>Stick left: gimbal left</p><p>Stick right: gimbal right</p>                                 |

## Shutting down & charging the controller

The DeltaQuad Controller can operate continuously for approximately 6 hours. If more operation time is required, the controller can be charged during operation.

To charge the controller, open the rubber cover between the antennas and attach the provided USB charger to the USB-C port. The controller requires high-voltage charging. Standard USB chargers or USB sockets from laptops are not always capable of providing high voltage, but they will extend the battery life of the controller.

To shut down the controller, press and hold the power button until the shutdown menu appears. Select "Power off" to shut down the controller.
