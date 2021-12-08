---
description: >-
  This section describes how to connect a second screen to your DeltaQuad
  Controller
---

# Connecting a second screen

## Introduction

The second screen functions can be used to stream video to a local or even remote device. There are several methods of streaming the video feeds to a second screen which are described below.&#x20;

The DeltaQuad Controller provides an RTSP based video stream, and a secondary telemetry link. The second screen will connect to the DeltaQuad Controller, not directly to the UAV. This is to prevent the UAV from having to use double the amount of bandwidth. It also enables screen sharing over LTE, even when the UAV is flying outside of LTE range, as long as the DeltaQuad Controller is connected to the LTE network.

The video feed displayed on the second screen is the video feed that has been activated by the pilot.

## Using a WiFi hotspot

If your controller is connected to a 5ghz WiFi hotspot, a second device can connect to the same hotspot. For information on how to connect the DeltaQuad Controller to a WiFi hotspot, please see the [DeltaQuad Controller section](deltaquad-controller.md).

Once connected you will need to determine the IP address that was assigned to the controller by the WiFi hotspot. To do this you can open the Settings app, scroll down and select About Phone, and tap on Status. Here you will find the item "IP address" which shows the values for the IP addresses assigned by the hotspot. The value required is the sequence of 4 numbers separated by a dot. For example 192.168.43.124

The DeltaQuad Controller can also be used to host a WiFi hotspot. To enable the WiFi hotspot on the DeltaQuad Controller, enter the Android settings and activate the Mobile Hotspot. When the DeltaQuad Controller is hosting a mobile hotspot it will have no internet connectivity and LTE modes will be disabled.

The second device can be a Windows, Mac or Linux based laptop or tablet. The recommended software for viewing the video stream is [VLC Media Player](https://www.videolan.org). To open the video stream launch VLC Media Player and select "media" -> "open network stream". In the "network URL" field enter the following address:

```
rtsp://[IP-ADDRESS]:8554/video
```

For example: rtsp://192.168.43.124:8554/video

Select the checkbox  "Show more settings"

Change "Caching" to 100 ms

Click "Play"

![](../../.gitbook/assets/Selection\_321.jpg)

## Remotely using the mobile network

You can attach your second screen to a DeltaQuad Controller using the mobile network. When your vehicle is shipped you will receive an email with account information that contains the VPN profile for your second screen. To use this VPN profile you will need to download and install the [OpenVPN client](https://openvpn.net/vpn-client/).

When the VPN Client is installed, click on the VPN icon in the bottom right section of your taskbar. That will open the VPN client interface to import the VPN profile that was sent to you.

Once connected to the VPN network for your controller, you can retrieve the camera feed on your second device.

The second device can be a Windows, Mac or Linux based laptop or tablet. The recommended software for viewing the video stream is [VLC Media Player](https://www.videolan.org). To open the video stream over VPN, launch VLC Media Player and select "media" -> "open network stream". In the "network URL" field enter any of the following addresses:

#### The active feed of the DeltaQuad Controller (recommended)

```
rtsp://100.96.1.34:8554/video
```

#### Directly to the UAV Camera Gimbal

```
rtsp://100.96.1.18:8554/cam1
```

#### Directly to the UAV FPV nose camera

```
rtsp://100.96.1.18:8554/cam3
```

Select the checkbox  "Show more settings"\
Change "Caching" to 100 ms\
Click "Play"

{% hint style="info" %}
TIP: _It is recommended to connect to the active feed for the DeltaQuad Controller. This will prevent the mobile connection for the UAV to stream multiple video feeds and thus use double the bandwidth. It also allows the UAV to fly outside of mobile network range while the DeltaQuad Controller is connected to the UAV using RADIO mode. The DeltaQuad Controller can still provide VPN based video streams to the second device in this mode._
{% endhint %}

## Using Screen Casting

Screen Casting can be used to replicate the display on the DeltaQuad Controller. The DeltaQuad Controller comes pre-installed with a Cast app on the home screen. When launching the Cast app, you will see a list of devices that support casting. Select the intended device and follow the instructions to enable casting to your remote screen.

Casting is based on Miracast, and is supported on Windows, Mac, and certain Smart TV systems. To cast to a second screen, the second screen will need to be attached to the same WiFi network as the DeltaQuad Controller, or connected to the VPN network as described above.

On Windows 10 or later, you will need to enable the Wireless Display option. To do this, open the Windows settings and search for "projector settings". Follow the steps indicated to enable "Projecting to this PC". Once these steps have been completed, the Windows system will show in the Cast list of the DeltaQuad Controller.

## Using the Camera Control Laptop

If you have purchased a Camera Control Laptop, you will be able to run the CCA3 application for both video, and camera control on the Camera Control Laptop. This system comes with a joystick for camera control, and offers touch-screen for mission planning, UAV control, and Camera control.

After booting up the laptop you may choose to connect the laptop to the same WiFi hotspot as the DeltaQuad Controller, or connect it to the Internet to enable VPN based LTE connectivity to the DeltaQuad Controller.

From the home screen of the laptop you launch the Connection Manager to choose a Local or VPN based connection. After that you can launch CCA3 to view and/or control the UAV and/or Camera Gimbal.
