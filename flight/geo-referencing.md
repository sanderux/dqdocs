# Geo-referencing

If your DeltaQuad is equipped with a mapping payload you might need to post process the images to add the geographic coordinates. This is called geo-referencing (or geotagging). The following mapping payloads require post processing:

* Sony A7R
* Sony RX1R
* Sony A6000
* Agrowing multispectral

All other camera payloads perform their own geo-referencing.

## When using the Emlid Reach system

To post process your images using an Emlid Reach PPK/RTK system, we recommend using [RedToolBox](https://www.redcatch.at/en/redtoolbox/). You also need the Emlid ReachView app on your tablet or mobile phone.

Before you can use your Emlid Reach system you will need to perform the initial setup procedure as described here: [https://docs.emlid.com/reach/before-you-start/first-setup](https://docs.emlid.com/reach/before-you-start/first-setup)

After completing a survey mission flight please complete the following steps:

Step 1: Power off and on your base station and browse to the address as shown in the ReachView app.\
Step 2: Download the UBX file corresponding to your flight, call this file "base.zip"

![](../.gitbook/assets/Selection\_429.jpg)

\
Step 3: Power on your UAV and browse to the address as shown in the ReachView app.\
Step 4: Download the UBX file corresponding to your flight.call this file "rover.zip"\
Step 5: Extract both base and rover files in a separate folder.

Next you can process the data inside RedToolBox

Step 1: Open RedToolBox by running the RedToolBox-V2.exe file\
Step 2: Choose Device: When using the Emlid Reach M+/RS+ please select "Emlid Reach M/M+". When using the Emlid Reach M2/RS2, please select "Ublox ZED9F".\
Step 3: Select the desired output for your post-processing option. Note that EXIF will work for virtually any platform but it is a slow process. For Agisoft or Pix4D we recommend using the designated outputs.\


![](../.gitbook/assets/Selection\_427.jpg)

\
Step 4: Open the Import tab and select all pictures from your mapping mission.\
Step 5: Click on the "Import Rinex ..." button under the GNSS section and select your rover UBX file\
Step 6: Click on the "Import Rinex ..." button under the BASE section and select your base UBX file

![](<../.gitbook/assets/Selection\_430 (1).jpg>)

\
Step 7: click "Run mapping"

For more information on RedToolBox please see the [RedToolBox User Manual](https://www.redcatch.at/downloads\_all/REDtoolbox\_manual\_EN.pdf)

## When using onboard log files

The following procedure should only be used when not using a PPK solution.

To Georeference the images you can remove the sd-card from the flight controller to copy the logfile from the flight. The logfile will be stored in the 'logs' subfolder under the date & time of the flight.&#x20;

Download the DeltaTag application (Windows or Linux) here: [https://drive.google.com/drive/folders/1WkI42DHv62ShBsdqhzm9Sjsh\_Zq2FG5S?usp=sharing](https://drive.google.com/drive/folders/1WkI42DHv62ShBsdqhzm9Sjsh\_Zq2FG5S?usp=sharing)

Step 1: Select the flight log by clicking on "Log file"\
Step 2: Select the images folder by clicking on "Image folder"\
Step 3: Click on "RUN"

The meta information of your images (EXIF information) will now be updated to include the geo-coordinates of the vehicle at the time the trigger was sent.

{% hint style="info" %}
NOTE: The DeltaTag application uses the LAST image in your folder to calibrate the timestamps of your images with the triggers in your logfile. It is important not to include any images that were not taking from the survey mission. (test images, manual shots, etc)
{% endhint %}

You can verify the geotagging using an online service like [Pic2Map](https://www.pic2map.com).\
[Pix4D](https://pix4d.com) can be used for 3D reconstruction.
