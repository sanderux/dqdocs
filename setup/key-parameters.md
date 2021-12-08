# Key parameters

From the Ground Control Station the vehicle parameters can be modified. Some parameters may need to be adjusted for a specific situation or payload. To access the vehicles parameters you will need to switch the vehicle on and establish a connection between the Ground Control Station and the vehicle.

## Modifying parameters

To modify parameters select the settings icon from QGroundControl and then select the Parameters tab.

![](<../assets/QGC Params.png>)

## Key parameters

The following parameters are considered safe to modify within the bounds described. To find a specific parameter the search function can be used.

### **BAT\_CAPACITY**

Min: 10000\
Max: 33000\
Default: 23000

This defines the total capacity in mAh of the battery when fully charged. The default value is set to 23000 (23 Amp/Hour). If your vehicle is equipped with a 20Ah battery set this to 20000. If you have an Auxiliary LiPo attached you can add the capacity of this LiPo to the total capacity. For example, with a 23Ah DeltaQuad LiPo and a 10Ah Auxiliary LiPo set this value to 33000.

The capacity entered in this parameter should be reduced by 10% every 75 charge cycles on a given battery.

### FW\_THR\_CRUISE

Min: 52%\
Max: 62%\
Default: 52%

This defines the cruise throttle percentage. Setting this higher than the default value will increase the cruise speed of the vehicle. Setting this lower is not recommended as the vehicle will fly less efficiently and could stall. When flying with maximum payload a value of 62 or higher is required.

### VT\_FW\_ALT\_ERR

Min: 10\
Max: 100\
Default: 12

This function also known as QuadChute, defines the maximum altitude deviation the vehicle will accept when flying in fixed wing mode. If the vehicle drops below this deviation it will automatically revert to quadcopter mode. This functionality is required to ensure safe flight. Disabling this functionality will void your warranty and introduce a serious safety hazard.

### MPC\_LAND\_SPEED

Min: 0.6\
Max: 1.2\
Default: 0.7

This parameter controls the descent speed during the final stage of landing. The vehicle will use this value as maximum speed. If wind conditions are erratic the vehicle will lower this speed automatically to remain stable. A lower value will result in more energy being required for landing.
