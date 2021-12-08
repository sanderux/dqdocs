# Integrating payloads

The DeltaQuad has been optimized for payload integration. The payload integration features consist of the following;

* Large payload bay located directly on the CG, this allows live swapping of payloads without having to re-balance the vehicle.
* Expandable blind mate connectors to allow electronics integration in the VTOL modules and wings
* Open source flight control with Mavlink compatibility
* Fully accessible secondary on-board computer for software integration

## Payload specifications

| Name                                      | Value                                                   |
| ----------------------------------------- | ------------------------------------------------------- |
| Maximum payload weight (without Aux LiPo) | 1.2Kg                                                   |
| Maximum payload weight (with Aux LiPo)    | 400g                                                    |
| Payload bay height:                       | 80mm minimum (oval shaped)                              |
| Payload bay length:                       | 120mm                                                   |
| Payload bay width:                        | 200mm minimum (oval shaped)                             |
| VTOL module to fuselage connector         | 2 x power + 5 x signal + 5 x signal positions available |
| VTOL module to wing connector             | 3 x signal + 3 x signal positions available             |

## Payload integration best practices

When integrating your payload it is recommended to stay within the payload bay, and as much as possible inside the fuselage. The DeltaQuads EPO foam is easy to modify and is also easy to glue. When installing a device that needs to sit outside of the vehicle (such as a camera gimbal) it is recommended to stay inside the fuselage as much as possible. External objects can cause drag and will make the vehicle perform less efficiently.

It is recommended to [increase the cruise speed](key-parameters.md) after installing an external object by a few percent, and slowly decrease the value based on the vehicles performance. The vehicle should fly at an average pitch angle between 3 and 8 degrees when flying level.

If the payload requires power it is recommended to install additional BEC units and not draw power from the primary avionics. An additional BEC can be installed by soldering it onto the wires that also power the avionics BEC.

If the payload consumes significant power the [BAT\_CAPACITY](key-parameters.md) parameter should be reduced by the amount of energy the payload is estimated to consume over the course of an entire LiPo discharge.

It is recommended to perform a [sensor calibration](../maintenance/sensor-calibration.md) when integrating any additional payload containing any electric or metallic components.

## Onboard computer integration

The onboard computer exposes mavlink locally and over the 4G VPN network on UDP port 14550. If integrating additional applications on the secondary computer, make sure your application does not flood the onboard computers CPU, this could result in loss of Telemetry.

##
