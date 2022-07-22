# Connecting a Secondary Control Terminal

## Introduction

The DeltaQuad Controller provides an RTSP based video stream, and a secondary telemetry link. The Secondary Control Terminal will connect to the DeltaQuad Controller, not directly to the UAV. This is to prevent the UAV from having to use double the amount of bandwidth. It also enables connecting a Secondary Control Terminal over LTE, even when the UAV is flying outside of LTE range, as long as the DeltaQuad Controller is connected to the LTE network.

The Secondary Control Terminal can control the vehicle in the same way the DetaQuad Controller can, with the exception of the joystick and button functions. The UAV will always follow the last command received, regardless of the source (Controller or Secondary Control Terminal).\
\
The video feed displayed on the Secondary Control Terminal is the video feed that has been activated by the pilot.

## Using a WiFi hotspot

If your controller is connected to a 5ghz WiFi hotspot, a second device can connect to the same hotspot. For information on how to connect the DeltaQuad Controller to a WiFi hotspot, please see the [DeltaQuad Controller section](../deltaquad-pro-view/deltaquad-controller.md).

Once connected you will need to determine the IP address that was assigned to the controller by the WiFi hotspot. To do this you can open the Settings app, scroll down and select About Phone, and tap on Status. Here you will find the item "IP address" which shows the values for the IP addresses assigned by the hotspot. The value required is the sequence of 4 numbers separated by a dot. For example 192.168.43.124

The DeltaQuad Controller can also be used to host a WiFi hotspot. To enable the WiFi hotspot on the DeltaQuad Controller, enter the Android settings and activate the Mobile Hotspot. When the DeltaQuad Controller is hosting a mobile hotspot it will have no internet connectivity and LTE modes will be disabled.

Using the IP Address from the DeltaQuad Controller you can now add a TCP based connection from QGroundControl on the Secondary Control Terminal to the Controller. To do this use the following steps:

1. In QGroundControl on the Secondary Control Terminal click on the Q icon
2. Click on Application Settings
3. Select "Comm links"
4. Click on "Add"
5. Select type "TCP"
6. In "Host Address" enter the IP address of the DeltaQuad Controller
7. Leave the TCP port on 5760
8. Click OK
9. Click CONNECT

![](../.gitbook/assets/Selection\_437.jpg)

## Remotely using the mobile network

You can attach your Secondary Control Terminal to a DeltaQuad Controller using the mobile network. When your vehicle is shipped you will receive an email with account information that contains the VPN profile for your second screen. To use this VPN profile you will need to download and install the [OpenVPN client](https://openvpn.net/vpn-client/).

When the VPN Client is installed, click on the VPN icon in the bottom right section of your taskbar. That will open the VPN client interface to import the VPN profile that was sent to you.

Once connected to the VPN network for your controller, you can use the IP address 100.96.1.34 and follow the steps listed in [Using a WiFi Hotspot](connecting-a-secondary-control-terminal.md#using-a-wifi-hotspot) above.

## Using Screen Casting

Screen Casting can be used to replicate the display on the DeltaQuad Controller. The DeltaQuad Controller comes pre-installed with a Cast app on the home screen. When launching the Cast app, you will see a list of devices that support casting. Select the intended device and follow the instructions to enable casting to your remote screen.

Casting is based on Miracast, and is supported on Windows, Mac, and certain Smart TV systems. To cast to a second screen, the second screen will need to be attached to the same WiFi network as the DeltaQuad Controller, or connected to the VPN network as described above.

On Windows 10 or later, you will need to enable the Wireless Display option. To do this, open the Windows settings and search for "projector settings". Follow the steps indicated to enable "Projecting to this PC". Once these steps have been completed, the Windows system will show in the Cast list of the DeltaQuad Controller.

