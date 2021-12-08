# Safety features

This section covers the flight controller's safety features. To access the safety features configuration screen you will need to switch the vehicle on and establish a [connection](ground-control-station.md) between the Ground Control Station and the vehicle.

## Modifying the safety features

To modify parameters select the settings icon from QGroundControl and then select the Safety tab.

![](<../assets/QGC Safety.png>)

## Safety features

### Low Battery Failsafe Trigger

Default: Return at critical level, land at emergency level

Default Warn level: 10%

Default Failsafe level: 7%

Default Emergency level: 5%

These parameters define what the vehicle does when reaching low battery levels.

**Note: The levels are those estimated to be reached when having flown to the landing site. This means that the further the vehicle is from its intended landing location, the sooner these actions will be taken. The vehicle will attempt to maintain these values when landed.**

Warn level: The percentage where the vehicle will give a visible and audible warning to the Ground Control Station

Failsafe level: The level at which the vehicle initiates the critical battery action. (return)

Emergency level: The level at which the vehicle initiates the emergency battery action. (land)

### RC Loss Failsafe trigger

Default: Disabled

The DeltaQuad does not come with a traditional radio remote control. If such a transmitter/receiver is added this setting defines the behavior when the signal from this transmitter is lost. The DeltaQuad Controller will have both RC and DataLink functionality, but as these signals are sent over the same link it is recommended that you leave this setting disabled.

### Data Link Loss Failsafe Trigger

Default: Disabled

Default timeout: 100s

This controls the behavior of the vehicle when the telemetry link is lost. When flying fully autonomous missions where the loss of telemetry is allowed or expected, this parameter should be set to Disabled.&#x20;

Some local laws require this value to be set to "Return to Land".

The Settings of the Data Link Loss Failsafe Trigger should be checked before pausing the vehicle mid-flight.\
\
If the trigger is disabled and the Data Link is lost after the vehicle is paused and in Hold Mode, the pilot has no possibility of giving a new pilot command. Until the Data Link is regained the DeltaQuad will remain in Hold mode. If the Data Link can't be re-established the vehicle will remain in Hold Mode until the Low Battery Failsafe Trigger will be activated.

### Geofence Failsafe Trigger

Default action: Warning&#x20;

Default max radius: Disabled&#x20;

Default max altitude: Disabled

The geofence failsafe trigger can be set to limit the vehicle's radius and/or altitude. When settings these parameters the vehicle will perform the defined action upon breaching any of these.

### Return Home Settings

Default climb: 60m

Default home action: Land immediately

These settings define how the vehicle behaves when it engages the Return to Land function. The Climb altitude is the minimum altitude relative to home the vehicle will maintain for its return path.&#x20;

If the altitude of the DeltaQuad is lower than the Default climb value, in this case, 60 meters, the UAV will ascend to that Default climb altitude of 60 meters.

If the vehicle is higher at the point where the Return to Land is triggered it will maintain that altitude to return.

The DeltaQuad can perform an autonomous Return to Land when instructed from the Ground Control Station, when instructed from a mission, or when triggered by a failsafe event.&#x20;

If the DeltaQuad is in Fixed-wing mode when the Return to Land event is triggered the UAV will make use of the Landing Pattern from the planned mission.&#x20;

The DeltaQuad will return in Fixed-wing mode to the Loiter waypoint of the Landing pattern in a straight line at the altitude the UAV is at when the RTL was initiated.

If the altitude of the DeltaQuad is higher than the Default climb value the UAV will stay at its altitude and return to the Loiter Waypoint.

When reaching the "Loiter" waypoint the DeltaQuad will loiter and descend to the set Approach Altitude. In the final approach towards the Land item, the DeltaQuad will perform a transition to Multirotor mode and land as planned in the mission.&#x20;

Be aware that if your planned Land item is not at the same location as your Launch item, the DeltaQuad will land in a different location rather than your Home Position.

If the DeltaQuad is in Multirotor mode when the Return To Land event is triggered the UAV will return to the Land item in a straight line at the altitude it is at when the RTL was initiated.&#x20;

Because the DeltaQuad is in Multirotor mode it will not make use of the Loiter waypoint and the Landing Pattern but head directly for the Land item.

If the altitude of the DeltaQuad is lower than the Default climb value (60m) the UAV will ascend to that Default climb altitude (60m) whilst heading for the Landing item.

If the altitude of the DeltaQuad is higher than the Default climb value the UAV will stay at its altitude and return to the Landing Pattern.

When reaching the Land item the DeltaQuad will descend in Multirotor mode and touchdown at the Land location.

Be aware that if your planned Land item is not at the same location as your Launch item, the DeltaQuad will land in a different location rather than your home location.

### Land Mode Settings

Default Descent Rate: 1,2m/s

Disarm after: 5s

This controls the landing behavior. The default descent rate is the maximum speed the DeltaQuad descends in Multirotor during a landing.

In windy conditions, the vehicle will correct itself by applying a lower descent rate and the indicated descent rate might not be achieved. The DeltaQuad will brake and slow down its descent from approximately 8 meters above the Home Position to guarantee a soft landing.&#x20;

The default value of the Descent Rate can be left at 1,2m/s. Nevertheless, if it needs to be changed it should not be increased above 1.5m/s.

The disarm time is the time the vehicle waits before disarming (stopping the motors) after it has detected a landing. The value should not be set lower than 5 seconds.&#x20;
