# Sensor calibration

The DeltaQuad requires a compass calibration in the following conditions:

* When indicated by events described in this manual.
* When the telemetry readings are inconsistent with reality.

The DeltaQuad requires a gyro calibration in the following conditions:

* When indicated by the UAV

The DeltaQuad requires an accelerometer calibration in the following conditions:

* When indicated by the UAV

The DeltaQuad requires a level horizon in the following conditions:

* When indicated pitch or roll does not match reality
* When indicated by the supplier

## Accessing the calibration screen

Sensor calibration is performed in QGroundControl. To access the sensor calibration, you will need to switch the vehicle on and establish a connection between the Ground Control Station and the vehicle. Navigate to the settings view and select the Sensors tab.![](<../assets/Sensor calib.jpg>)

QGroundControl will issue a warning about sensor calibration over a WiFi connection. This can safely be ignored by clicking OK.

The following sensor calibrations should be performed:

* Compass
* Gyroscope
* Accelerometer
* Level Horizon

All calibrations should be performed with the VTOL modules attached, and any additional payload installed and powered on.&#x20;

After every calibration step, the autopilot must reboot. The autopilot can be rebooted quickly from the parameters tab under the tools button.

## Compass calibration

A compass calibration is best performed outside, away from metallic objects, electrical or magnetic interference. To start the compass calibration, click the compass button and follow the instructions on the screen. The calibration process starts when clicking OK. The autopilot orientation parameter in the GCS should remain unchanged. A compass calibration involves rotating the vehicle 3 times over all axis. This calibration step can be performed by hand. The canopy should be closed and the LiPo battery and any additional payload should be inserted and securely fastened.

Perform the calibration as indicated by the images on the ground station. When all axis are finished (images turn green) click OK, leaving the external magnetometer orientation unchanged. Then reboot the vehicle.

After the compass calibration ALWAYS verify the compass is reading correctly by pointing the vehicle north, east, south and west and at every turn verify that the vehicle icon on the ground station is pointing in the correct direction, and remains pointed in that direction for at least 30 seconds. if the compass is not reading correctly by more than 8 degrees, please retry the calibration. If the problem persists please contact Vertical Technologies.

## Gyroscope calibration

The gyroscope calibration is best performed indoors. It requires the vehicle to sit level based on the VTOL arms. To level the vehicle based on the VTOL arms it is recommended to find a level surface (a table) and place 4 objects of equal height under the quadcopter motors. For example soda cans. The foam underside of the vehicle should be free from the table and the carbon VTOL arms should sit level horizontally.

When the vehicle is sitting level, press OK to start the calibration. This will complete in about 20 seconds. The vehicle should not be touched or moved during the calibration process. Then reboot the vehicle. If, for any reason, the vehicle is moved during the calibration process then repeat the process from the beginning.

## Accelerometer calibration

To start the accelerometer calibration, click the accelerometer button and follow the instructions on the screen. The calibration process starts when clicking OK. The autopilot orientation parameter in the GCS should remain unchanged. An accelerometer calibration involves positioning the vehicle on all axis. This calibration step can be performed by hand. The canopy should be closed and the LiPo battery should be inserted and securely fastened.

Perform the calibration as indicated by the images on the Ground Control Station, ensuring the vehicle is motionless at each point in the calibration process. Then reboot the vehicle.

## Level horizon

{% hint style="warning" %}
WARNING: This calibration is rarely needed outside of the factory. Performing this calibration incorrectly can cause the vehicle to become unstable or crash.
{% endhint %}

Before levelling the horizon all other calibrations, except compass calibration, must have been completed.

The Level Horizon calibration is best performed indoors. It requires the vehicle to sit level based on the VTOL arms. To level the vehicle based on the VTOL arms it is recommended to find a level surface (a table) and place 4 objects of equal height, such as soda cans or soup tins, under the quadcopter motors. The foam underside of the vehicle should be free from the table and the carbon VTOL arms should sit level horizontally.

When the vehicle is sitting level, press OK to start the calibration. This will complete in about 20 seconds. The vehicle should not be touched or moved during the calibration process. Then reboot the vehicle. If, for any reason, the vehicle is moved during this calibration process then repeat the process from the beginning.
