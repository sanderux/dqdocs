# Geo-referencing

If your DeltaQuad is equipped with a mapping payload you will need to post-process the images to add the geographic coordinates. This is called geo-referencing (or geotagging). Some camera systems have a built-in GPS solution, these include the Micasense, Flir, and Workswell sensors. Other systems such as the Sony or Agrowing cameras require post-processing for geo-referencing.

Post-processing can be performed on 2 methods:

1. Using the onboard flight logs. For this step please skip to the section "When using onboard log files". This provides an easy, but relatively low accuracy method of georeferencing pictures.
2. If your DeltaQuad was equipped with an Emlid Reach PPK/RTK solution you can georeference using the Emlid Reach method. This provides highly accurate georeferencing of your images.

Once your images have been geo-referenced, you can import them into stitching software to reconstruct a 2D and/or 3D model of the surveyed area. Examples of stitching software are Pix4D and Agisoft.

## When using the Emlid Reach system

{% hint style="info" %}
NOTE: The Emlid Reach solution requires an initial setup process. Make sure this process was executed before executing your first mapping mission.
{% endhint %}

{% hint style="info" %}
TIP: If you are experiencing problems connecting to the Emlid Reach over WiFi, you can connect a micro-USB cable to the emlid Reach, wait 60 seconds and then browse to [http://192.168.2.15/](http://192.168.2.15). This will allow you to perform the initial setup and/or download the UBX files.
{% endhint %}

Before you can use your Emlid Reach system you will need to perform the initial setup procedure as described here: [https://docs.emlid.com/reach/before-you-start/first-setup](https://docs.emlid.com/reach/before-you-start/first-setup)

When following this procedure you will have installed the ReachView app which will be required for the next steps.

After completing a mapping mission flight please complete the following steps:

Step 1: Power off and on your base station and browse to the address as shown in the ReachView app.\
Step 2: Download the UBX file corresponding to your flight, call this file "base.zip"

![](../.gitbook/assets/Selection\_429.jpg)

\
Step 3: Power on your UAV and browse to the address as shown in the ReachView app.\
Step 4: Download the UBX file corresponding to your flight. Call this file "rover.zip"\
Step 5: Extract both base and rover files in a separate folder.

### Using Emlid Studio

The recommended method of geo-referencing your images is by using [Emlid Studio](https://docs.emlid.com/emlid-studio/). Emlid Studio is available for Windows and Mac based operating systems. It allows you to geotag photos obtained during the flight for further mapping in photogrammetry software.

To process your data using Emlid Studio please use the following steps;

1. Download and install the Emlid Studio application from: [https://docs.emlid.com/emlid-studio/](https://docs.emlid.com/emlid-studio/)
2. In the top-right corner click on the word PPK, and change the mode to "Droned data PPK"
3. Click on the "Drone" box and select the file with the .UBX extention from the rover folder. If your dataset consists of multiple flights, you can add multiple UBX files.
4. Click on the "Base" box and select the UBX file from the base folder.
5. Click on "Process" and wait for the files to be processed.
6. Click on the "Folder with photos" box, this will indicate how many photos are expected. This should match the number of pictures on the sd-card from your camera. It is recommended to move the pictures from the sd-card to a hard drive before processing.
7. It is recommended to switch "Update original photos" on, as this will prevent the system from duplicating the photos and will increase processing speed.
8. Click on "Tag photos" and wait for the process to finish

The photos will now contain the PPK corrected geographic information. You can now use them for processing in your stitching software such as Pix4DMapper or AgiSoft Metashape.

A full and in-depth explanation of the usage and options in Emlid Studio can be found [here](https://docs.emlid.com/emlid-studio/drone-data-ppk).



### Using RedToolBox

Alternatively you may use RedToolBox, this application is capable of de with situations where the number of pictures does not match the number of recorded trigger events.

RedToolBox can be downloaded from here: [https://www.redcatch.at/redtoolbox/](https://www.redcatch.at/redtoolbox/)

Step 1: Open RedToolBox by running the RedToolBox-V2.exe file\
Step 2: Choose Device: When using the Emlid Reach M+/RS+ please select "Emlid Reach M/M+". When using the Emlid Reach M2/RS2, please select "Ublox ZED9F". \
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
[Pix4D](https://pix4d.com) Mapper or Agisoft Metashape can be used for 3D reconstruction.
