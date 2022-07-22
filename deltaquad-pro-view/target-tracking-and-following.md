---
description: >-
  The DeltaQuad Pro #VIEW is capable of tracking and/or following static or
  moving objects such as cars, humans or other UAVs.
---

# Target tracking & following

![](../../.gitbook/assets/Selection\_070.png)

## Target Tracking

Target tracking is the mode where the camera will remain focused on a target. The target can be moving or static. To activate target tracking simply tap anywhere in the video feed and the camera will enter tracking mode and track the target that was tapped on. You can tap several times to fine-tune your target tracking mode.

When a target is being tracked, a white square is displayed on the object that is being tracked. By moving the camera joystick, tracking is disabled and the camera returns to the previous mode.

{% hint style="info" %}
TIP: The camera can rotate 360 degrees. To avoid reaching the maximum rotation angle it is recommended to fly towards, follow, or directly above a tracked object.&#x20;
{% endhint %}

## Target following

Target following is the mode where the vehicle actively follows a tracked target. To engage target following mode you will first need to track a target. Once a target is locked you can engage the target following switch as described in the [DeltaQuad Controller section](deltaquad-controller.md). The system will start following a target when these conditions are met:

* A target is actively being tracked
* The target is less than 2000m away from the vehicle
* The target following switch is set to active

When first entering target following mode the vehicle will switch its flight mode to "HOLD" mode. The target following system will then issue reposition commands every 1.5 seconds for as long as the target following conditions are met. If the conditions are no longer met the vehicle will remain circling the position of the last known target location. If the tracked target was lost you can re-engage target tracking by simply tapping on the object in the video feed, the system will follow any target selected while the target following switch is engaged and the conditions are met.

If the vehicle is flying above the tracked target, or if the vehicle is flying faster than the tracked target, it will circle above the target keeping the target in view at all times.

If the target following switch is disengaged the vehile will start circling its current position.

